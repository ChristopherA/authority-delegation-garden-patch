---
created: 2026-04-01
part_of: "[[Miller, Tulloh & Shapiro (2005) The Structure of Authority]]"
---

# Miller, Tulloh & Shapiro (2005) The Structure of Authority — Analysis

## Core Thesis

The paper argues that security cannot be added to a software system after the fact because the authority structure of a system — how much access each component has to each resource — is determined by architectural choices that precede any security analysis. The central formulation: "treating security as a separate concern has not succeeded in bridging the gap between principle and practice, because it operates without knowledge of what constitutes least authority."

The problem is epistemic. A security module bolted onto a system does not know what any given component needs to do, so it cannot compute the minimum authority that component requires. Only at request time — when a user designates a file in an open dialog, when one object passes a reference to another — does the information exist to determine what authority is adequate. A static security layer operating on pre-computed permission sets cannot respond to this dynamic information.

The practical consequence: conventional systems grant applications the user's full authority as a simplifying assumption. A Solitaire game runs with the authority to delete any of the user's files, scan email, and install back doors — not because it needs this authority, but because the architecture provides no mechanism to give it less.

## The Logic of Designation

The paper's cleanest illustration of its thesis is the `cp` versus `cat` example. Both Unix commands copy a file. `cp` receives file paths as strings; `cat` receives open file descriptors. The difference is not cosmetic.

When `cp` receives strings, it must already hold the authority to interpret those strings — to look up the named files in the filesystem namespace. Its least authority includes the user's entire filesystem access. When `cat` receives descriptors, the shell has already resolved the designation; `cat` needs only the authority to read one specific file and write another. The strings were evaluated in the shell's namespace before being passed to `cat`, so `cat` never acquires namespace authority.

This is the paper's central insight about architecture: how designation works determines what authority a component requires. Systems that pass names (strings, paths, symbolic identifiers) push namespace authority down to the components that receive them. Systems that pass resolved references (capabilities, descriptors, object references) let the caller retain namespace authority and hand only the necessary access to the callee.

ACL-based security cannot fix this problem because it operates at a level above the designation logic. The ACL checks whether a process may access a resource; it cannot change whether the process needed global namespace authority to compute its request.

## The Object-Capability Model

The paper introduces the object-capability model as the design pattern that resolves the designation problem at the programming language level. In the object model, objects collaborate by holding references to each other and passing messages along those references. The capability model adds one key constraint: a reference indivisibly combines designation (which object), access (a communication path), and right (permission to use that path). There is no separate permission check because the reference is the permission.

This means the reference graph is the access graph. An object that does not hold a reference to another object cannot affect it, period. The topology of who can affect whom is determined entirely by who holds references to whom. Security is not a separate concern because it is already expressed by the reference structure — the same structure the programmer builds for functional reasons.

The paper makes an important claim: "Computer scientists, usually without any consideration for security, seeking only support for the division and composition of knowledge by abstraction and modularity, have recapitulated the logic of the object-capability model of secure computation." The capability model is not a security add-on. It is what modular design produces when you trace its logic to the access level.

### Connectivity Rules

The paper specifies how a new reference (and therefore new authority) can come into existence in an object-capability system:

1. **By introduction**: An object A that already knows both B and C can introduce C to B — passing a reference to C as an argument to B.
2. **By parenthood**: When B creates C, B holds the only initial reference to C.
3. **By endowment**: When A creates B, A can endow B with references A already holds.
4. **By initial conditions**: Some references exist at system initialization.

These four rules collectively express: "only connectivity begets connectivity." Two objects that have no path of references between them cannot affect each other. This is the invariant that makes capability systems analyzable — you can trace the authority a component can acquire by tracing the reference graph forward from its initial endowment.

## Fractal POLA: Four Levels of Composition

The paper's distinctive contribution is showing how the Principle of Least Authority (POLA) applies consistently across four levels of system organization, and how the effects at each level multiply:

**Level 1: Human granularity in an organization.** Different employees hold different authorities based on their responsibilities. Barb's compromise exposes only what Barb was trusted with. This is standard separation of duties; the paper uses it as the baseline to show the same logic applies at smaller scales.

**Level 2: Application granularity on a desktop.** Conventional systems grant every application the user's full authority — the simplifying assumption the paper critiques. CapDesk and Polaris demonstrate an alternative: applications receive only the authority the user grants through explicit designation. When Doug double-clicks a file, Polaris grants Excel authority to access that one file. Excel never acquires Doug's full filesystem authority.

**Level 3: Module granularity within an application.** An email client (CapMail in the paper's example) imports multiple libraries, including a crypto library and an address book module. The crypto library should not receive authority to read the address book; the smtp module should not receive authority to access the PGP keyring. Module-level POLA requires a startup module (the application's "main()") that parcels out initial authority to each imported module according to that module's functional role. This startup module is the application's TCB — the minimal base everything else depends on.

**Level 4: Object granularity within a module.** Individual objects receive only the references they need to do their job. The math library's `sqrt` function should not be able to overwrite a file — not because a policy check prevents it, but because it holds no reference to any file.

The multiplicative reduction claim: if POLA at Level 2 reduces an attacker's surface by 90%, and POLA at Level 3 reduces the remaining surface by 90%, the combined effect is 99% reduction. This framing suggests that POLA applied at multiple independent levels produces security gains that compound rather than simply adding.

## The TCB Structure

The paper introduces a refined understanding of the Trusted Computing Base. In conventional security analysis, the TCB is the minimal set of components whose correct operation is necessary for the system's security properties to hold. The paper extends this: every component that holds all the authority of a system is in that system's TCB, because compromising that component exposes the entire authority.

The key observation is that TCBs are nested. CapDesk is in Doug's TCB because it manages his application authority. But the applications CapDesk launches are not in Doug's TCB — they hold only what CapDesk granted them. The TCB structure follows the spawning tree: each parent that creates and endows children is in the TCB of those children's scope.

This nesting is why fractal POLA produces multiplicative rather than additive security gains. A successful attack that compromises one module gets only that module's authority, not the application's authority, not the user's authority.

## Legacy Integration

The paper addresses the practical problem of existing codebases. Legacy components — applications and libraries not written for capability systems — cannot practice POLA internally. The paper's answer is two-directional:

**External containment**: Polaris runs legacy applications in separate accounts with minimal initial authority. When the user designates a file, Polaris grants that application access to the specific file. The legacy application cannot ask for more than Polaris grants, even if it tries.

**"Taming"**: For legacy modules imported into capability-secure applications, the paper describes a methodology for wrapping them such that they cannot exceed their designated authority, even though their internal structure does not follow capability discipline.

Neither approach is perfect — a compromised legacy component still has whatever authority it was granted. But containment and taming enable incremental adoption: a system can move toward capability security without requiring a complete rewrite.

## Security as Extreme Modularity

The paper concludes with a table (Table 1) that maps conventional software engineering practices to their capability-discipline analogues:

| Software Engineering | Capability Discipline |
|---------------------|----------------------|
| Responsibility-driven design | Authority-driven design |
| Omit needless coupling | Omit needless vulnerability |
| Information hiding | Principle of Least Authority |
| Designation, need to know | Permission, need to do |
| Avoid global variables | Forbid mutable static state |

The argument embedded in this table: capability discipline is not a departure from good software engineering. It is good software engineering traced to its logical conclusion in the access domain. Engineers who practice modular design, information hiding, and responsibility-driven decomposition have already recapitulated most of what capability security requires. The remaining step is to make authority as sparse as knowledge.

## Relationship to Access Control Lists

The paper does not attack ACLs as technically incorrect. It identifies a structural limitation: ACLs check permissions at access time, but they operate on a permission state that was computed without knowledge of what any particular invocation would require. Static policy files and ACL configurations encode anticipated authority, not adequate authority. This is the gap between principle and practice: we know programs should have least authority, but without knowing what a program will be asked to do, we cannot know what least authority is.

Object-capability systems close this gap by making authority dynamic and tightly coupled to designation. Authority flows with reference passing, which flows with the program's functional logic. The programmer who passes a reference to a specific file as part of a request has already specified what authority the callee needs for that request. No separate policy computation is required.

## Evaluation

The paper's core argument holds at the level of design principle, but several limitations constrain its applicability:

**Proof-of-concept, not deployment**: CapDesk and Polaris are prototypes. The paper describes what is possible; it does not address the organizational and ecosystem obstacles to capability-secure system deployment at scale.

**TCB escape**: The paper acknowledges that if the underlying operating system does not provide per-account protection, CapDesk's protections are nullified. Capability security at the application level depends on foundational OS-level isolation. The paper defers this problem rather than resolving it.

**Name-passing systems**: Large parts of existing software infrastructure — filesystems, databases, network services — are fundamentally name-passing. The paper shows how name-passing and capability-passing can coexist (the user's shell resolves names and passes descriptors to `cat`), but the practical work of restructuring name-passing APIs is not addressed.

**Quantification**: The multiplicative reduction claim is qualitative. The paper explicitly acknowledges it cannot quantify the attack surface reductions described. This is an honest limitation, but it makes empirical comparison with ACL-based approaches difficult.

## Connections to the Garden

The paper provides the clearest available articulation of why authority structure must be designed in, not added on — a claim that applies directly to the agentic systems the garden is building toward. The insight that "only at request time can we determine how much authority is adequate" maps directly to the question of how to scope agent permissions in a personal knowledge estate. An agent system designed with static permission configurations faces the same problem as Polaris-less Excel: it holds excess authority because its designers could not anticipate the exact requests it would receive.

The connectivity rules (introduction, parenthood, endowment, initial conditions) describe how authority propagates in any system where agents pass references or delegate access. These rules are relevant to [[Human Authority Over Augmentation Systems]] — the principle that the vault owner retains legibility, boundary-setting, and override capability at every level. The capability model operationalizes what "boundary-setting" means at the code level: the owner's act of designation is the authority grant.
