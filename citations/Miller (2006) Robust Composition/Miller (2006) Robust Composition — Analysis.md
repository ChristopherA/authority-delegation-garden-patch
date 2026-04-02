---
created: 2026-04-01
part_of: "[[Miller (2006) Robust Composition]]"
role: analysis
---

part_of::[[Miller (2006) Robust Composition]]

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]

# Analysis: Miller (2006) Robust Composition

## The Unification Claim

Miller's central thesis is architecturally audacious: access control and concurrency control, treated for decades as separate engineering concerns, are actually the same problem in different clothing. The unification claim rests on a structural observation. Concurrent systems require that components communicate without sharing mutable state — otherwise race conditions and deadlocks follow. Object-capability systems require that authority travel with capability references, not be accessible as ambient state — otherwise the confused deputy and privilege escalation follow. The structural requirement is identical in both cases: no ambient shared state.

This means a system designed correctly for concurrent safety is also designed correctly for access control, and vice versa. The capability model is not a security overlay on top of a concurrency model — it is the same model serving both purposes simultaneously. Miller's contribution is formalizing this equivalence and showing that existing security and concurrency research had been producing convergent results from opposite directions.

## The Capability Model

The object-capability model rests on three axioms for how authority may be acquired:

**Parenthood**: a component that creates an object gains a capability to it. The creator has authority over what it creates.

**Endowment**: when creating a component, its creator may give it capabilities as initial endowments. The parent controls what the child starts with.

**Introduction**: a component may pass a capability it holds to another component. Authority spreads only through deliberate introduction — there is no ambient authority to inherit.

These three rules are exhaustive. Any capability not acquired through one of these three mechanisms cannot exist in a sound capability system. This exhaustiveness is what makes the capability model provably secure: authority can be traced through a graph of capability references, and any authority a component holds can be traced to an explicit chain of creation, endowment, and introduction decisions.

The contrast with Access Control List (ACL) systems is sharp. In ACL systems, authority is checked at the point of resource access: does this principal have permission for this resource? The check is contextual — it looks at the current execution context (user identity, role, group membership) and the resource's ACL. Authority is not carried with designations; it is computed from ambient context at access time.

This contextual authority check is the source of the confused deputy problem. When a trusted program is invoked by an untrusted caller, the program's authority — not the caller's — governs what resources can be accessed. The caller passes a filename; the program opens the file using its own elevated permissions. The program has been confused into acting as the caller's deputy for resources the caller couldn't access directly.

In capability systems, this is structurally impossible: you can only designate objects you have a capability to, and the capability carries the authority. If the untrusted caller lacks a capability to the sensitive file, they cannot pass a designation of it to the trusted program.

## Chapter 8: The Principle of Least Authority

Chapter 8 provides the dissertation's most directly applicable contribution to system design. Miller formalizes POLA as an extension of Saltzer and Schroeder's Principle of Least Privilege (1975). The extension matters and is often missed in popular treatments.

**Least Privilege** addresses individual permission grants: give each program only the specific permissions it needs. This is stated in terms of individual access checks — which files, which system calls, which resources.

**Least Authority** addresses effective authority in a system where authority is transitive. A component that has permission to invoke a utility that has permission to write to a directory has effective authority over that directory. The permission check on the component may show only "invoke utility" — the directory authority is indirect, acquired through the delegation chain. Least privilege analysis, which looks at direct permissions, misses this. Least authority analysis requires mapping the entire reachable authority graph from each component.

This transitivity observation has significant practical consequences. Systems designed for least privilege often contain hidden authority amplification paths — components that, through chains of legitimate invocations, can acquire authority their designers never intended them to have. The confused deputy is the most visible manifestation, but the general problem is wider: any ambient authority that becomes accessible through any invocation chain is a POLA violation.

The capability model makes POLA analysis tractable because capabilities are explicit and traceable. The authority graph is just the capability reference graph: nodes are components, edges are capability references. Least authority requires that each component's reachable authority — the authority accessible by following all capability reference paths from that component — is no more than necessary for its function. In ACL systems, the authority graph is computed from contextual permission checks and is not directly visible in code or data structures. In capability systems, it is the capability reference structure itself.

## The Robust Composition Framework

"Robust composition" names the design goal: independently developed components should be composable without requiring mutual trust, and the composition should not create security properties neither component had individually.

The dissertation identifies three failure modes for non-robust composition:

**Privilege escalation through combination**: Component A has permission P1; Component B has permission P2; their combination acquires authority over resource R that neither A nor B could access independently. This requires that authority flows through composition in ways the designers did not anticipate.

**Confused deputy attacks**: Component A is trusted with permissions; Component B lacks those permissions; B can invoke A to exercise A's authority on resources B designates. The combination produces a permission B does not independently hold.

**Unexpected concurrency interactions**: Components designed for single-threaded use acquire race conditions when combined in concurrent environments, producing security or correctness failures that neither component has individually.

All three failure modes have a common structure: the combination produces security properties not present in either component alone because the composition creates paths for authority to flow that the designers did not trace. The capability model prevents all three by making authority paths explicit and by eliminating ambient authority as a source of unexpected escalation.

## E and CapDesk: Theory Grounded in Implementation

The dissertation's theoretical contributions are backed by working implementations, which distinguishes it from purely formal capability-security research.

**E** (Electonic language) is a distributed, secure, persistent programming language in the Java tradition. E's design enforces capability discipline at the language level: there is no ambient authority available to E programs; all authority is passed explicitly as objects; the language runtime prevents capability forging. E's key concurrency abstraction is the "promise" — a reference to a computation that may not have completed yet. Promise pipelining allows distributed systems to coordinate without blocking, composing the concurrency model with the capability model in exactly the way Miller's theory predicts.

**CapDesk** is a desktop application environment built on E. It demonstrates that everyday user software — file managers, email clients, applications — can be built to run without virus-level authority by construction. In CapDesk, each application receives only capability references to the specific files and devices the user explicitly grants it access to. An application cannot read an arbitrary file by name; it can only read files it has been given capabilities to. This makes virus-like behavior architecturally impossible: malware cannot spread by exploiting ambient file system access because there is none.

CapDesk is historically significant as an existence proof that virus-safe end-user computing is achievable without requiring users to understand security — the architecture enforces it structurally.

## Relationship to Concurrency Control Theory

The formal treatment of concurrency control in the dissertation draws on the actor model and promise-based coordination. Miller demonstrates that the key security properties of capability systems — no ambient authority, explicit capability transfer, unforgeable references — correspond exactly to the key safety properties of concurrent actor systems — no shared mutable state, message-passing-only communication, deterministic reference relationships.

This isomorphism is not coincidental. Both capability security and concurrent actor models are responding to the same underlying problem: how to compose components that do not trust each other. Security composition requires that untrusted components cannot acquire unauthorized authority. Concurrent composition requires that components do not accidentally share state that produces race conditions. Both require explicit, traceable communication — which the capability model provides.

## Limits and Open Questions

**Incomplete deployment.** Despite the theoretical elegance and working implementations, capability-based operating systems and programming environments remain a minority. Most deployed software runs in ACL-based environments with substantial ambient authority. The dissertation does not address adoption barriers in depth.

**Usability of capability discipline.** E's capability discipline requires programmers to explicitly manage authority — passing capabilities as parameters, carefully scoping what gets passed where. This is correct but demanding. The CapDesk demonstrations show it is achievable, but the cognitive overhead for typical software development remains an open question.

**Verification.** The dissertation provides conditions for robust composition but does not include formal verification tools for checking whether a given system meets those conditions. Determining whether a large codebase satisfies POLA requires authority-graph analysis tools that the dissertation does not provide.

**Interoperability with ACL systems.** Most systems a capability-based component must interact with will be ACL-based. The boundary between capability-safe components and ambient-authority environments creates a trust boundary that requires careful engineering. The dissertation treats this as a problem for future work.

## Significance for Agentic Systems

Miller's dissertation was published before agentic AI systems existed, but its analysis applies directly to current agentic architectures. An AI agent running in a user's computing environment with broad ambient access to files, APIs, and services is a POLA violation by definition: the agent holds more transitive authority than any specific task requires. The confused deputy problem takes a specific form in this context: the agent can be invoked by any input (a malicious prompt, a malicious web page, a compromised tool response) and will exercise its ambient authority on behalf of that input.

Capability-safe agentic systems would give each agent only explicit capability references to the resources needed for its current task — no ambient file system access, no ambient API access, only the specific capabilities the principal has explicitly conferred for the current invocation. This is the architectural corollary of POLA applied to AI: the agent can do only what it has been explicitly authorized to do, with authority that cannot be escalated through the ambient execution context.

Allen's (2023) extension of POLA to data access and self-sovereign identity follows directly from Miller's transitivity analysis: a system that asks for more data than it needs violates least authority at the data layer, creating correlation paths that represent transitive authority over aspects of identity the user never explicitly granted.
