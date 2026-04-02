---
created: 2026-04-01
author: Christopher Allen
citation_slug: miller-tulloh-shapiro-2005-structure-of-authority
publication_year: 2005
canonical: https://papers.agoric.com/assets/pdf/papers/the-structure-of-authority-why-security-is-not-a-separable-concern.pdf
brief_summary: "Miller, Tulloh, and Shapiro argue that security cannot be added to software architectures after the fact because the amount of authority any component requires is determined by how designation works — a structural choice made long before any security analysis. The object-capability model resolves this by making reference graphs identical to access graphs, and by applying the Principle of Least Authority fractally across four levels of system organization. 19 pages, published in MOZ 2004 proceedings."
tagline: "Authority structure must be woven in — security bolted on cannot compute least authority"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Mark S. Miller]]

# Miller, Tulloh & Shapiro (2005) The Structure of Authority

## Bibliographic Entry

* _**The Structure of Authority: Why Security Is Not a Separable Concern**_ (2005). [conference paper]. _Miller, Mark S.; Tulloh, Bill; Shapiro, Jonathan S._ In: Van Roy, Peter (ed.), _MOZ 2004: Multiparadigm Programming in Mozart/Oz_, Lecture Notes in Artificial Intelligence, Vol. 3389, pp. 2–20. Springer-Verlag Berlin Heidelberg, 2005. Retrieved 2026-04-01 from: <https://papers.agoric.com/assets/pdf/papers/the-structure-of-authority-why-security-is-not-a-separable-concern.pdf>

## Summary

Common programming practice grants applications excess authority for the sake of convenience — every app a user runs gets the user's full filesystem, email, and network access. The paper argues this is not a lapse in discipline but a structural consequence of how existing systems handle designation. Only at request time, when a user picks a file or one object invokes another, do we know what authority is actually adequate. Security added as a separate concern operates without this information. The object-capability model resolves this by making authority an inherent property of reference passing: a reference is simultaneously designation, access path, and right. Applied fractally across organizational, application, module, and object levels, POLA produces multiplicative reductions in attack surface.

## Key Points

**The designation-authority coupling problem.** Two Unix commands that copy files — `cp` (passing filenames) and `cat` (passing file descriptors) — require vastly different minimum authority for the same task. `cp` must already hold authority to the user's entire filesystem namespace to interpret path arguments. `cat` needs only the two specific files the shell resolved and passed to it. How designation works determines what authority a component requires. This is an architectural fact, not a security oversight.

**Security cannot be added as a separate concern.** A security module bolted onto a system does not know what each component will be asked to do. Without knowing the full set of requests in advance, it must either pre-compute a permission set large enough to cover any possible request (producing excess authority) or query at runtime in ways that break usability. The paper: "treating security as a separate concern has not succeeded in bridging the gap between principle and practice, because it operates without knowledge of what constitutes least authority."

**Object-capability model: reference graph as access graph.** In the object-capability model, a reference indivisibly combines designation of an object, a communication path to it, and the right to use it. Objects interact only through references they hold. No separate permission check is needed because the reference is the permission. The topology of who can affect whom is determined entirely by the reference graph — which the programmer builds for functional reasons (modularity, abstraction, separation of concerns).

**Connectivity begets connectivity only.** New authority can enter a capability system only through four mechanisms: introduction (an object passes a reference it holds to another object), parenthood (a creator holds the only initial reference to what it creates), endowment (a creator gives a new object references from its own set), and initial conditions. Two objects with no reference path between them cannot affect each other. This invariant makes security analysis tractable.

**Four levels of POLA: multiplicative reduction.** The Principle of Least Authority applies consistently at organizational, application, module, and object levels. Effects at each level multiply: a 90% attack surface reduction at the application level combined with a 90% reduction at the module level produces a 99% combined reduction. The paper illustrates this with CapDesk (a capability-secure desktop in the E language) and Polaris (a wrapper that applies least authority to legacy Windows applications through designation-at-open-time).

**Capability discipline is extreme good software engineering.** The paper's Table 1 maps software engineering practices to their capability analogues: information hiding maps to POLA; omit needless coupling maps to omit needless vulnerability; responsibility-driven design maps to authority-driven design. The claim: capability security is what modular design produces when its logic is traced through to the access dimension. Security is not a separate module; it is a quality of the design.

**TCBs are nested, not monolithic.** The Trusted Computing Base at each level is the entity that manages authority delegation to the level below. CapDesk is in Doug's TCB; the applications CapDesk launches are not. Compromise at one level exposes only that level's authority. This nesting is why fractal POLA compounds: each layer that practices POLA limits what a compromise at that layer can access.

## Key Quotes

> "Common programming practice grants excess authority for the sake of functionality; programming principles require least authority for the sake of security. If we practice our principles, we could have both security and functionality."

> "Only when requests are made — whether by humans acting through a user interface, or by one object invoking another — can we determine how much authority is adequate. Without this knowledge, we must provide programs with enough authority to do anything they might be requested to do."

> "In the object-capability model references indivisibly combine the designation of a particular object, the means to access the object, and the right to access the object. By requiring that objects interact only by sending messages on references, the reference graph becomes the access graph."

> "The object-capability model does not treat access control as a separate concern; rather it is a model of modular computation with no separate access control mechanisms."

> "Parnas' principle of information hiding in effect says our abstractions should hand out information only on a need to know basis. POLA simply adds that authority should be handed out only on a need to do basis. Modularity and security each require both."

> "Of the people who have learned capability discipline, several have independently noticed that they find themselves following capability discipline even when writing programs for which security is of no concern. We find that it consistently leads to more modular, more maintainable code."

## Influence

The paper is the most accessible presentation of the object-capability model's relationship to general software engineering practice. Miller went on to co-found Agoric and develop the E programming language and its descendant proposals; Shapiro's work on the EROS capability operating system and later Coyotos extended these ideas into OS design. The argument that security is a structural property rather than a separable module influenced subsequent capability-based systems including Google's Caja, the Waterken server, and the design of JavaScript's strict mode. The paper's treatment of the `cp`/`cat` example became a widely-cited illustration of why ambient authority (filesystem-wide permissions) differs from object authority (per-object references).

## Sources

- Primary: Miller, Tulloh, Shapiro. "The Structure of Authority: Why Security Is Not a Separable Concern." MOZ 2004, LNAI 3389, pp. 2–20. Springer-Verlag, 2005. <https://papers.agoric.com/assets/pdf/papers/the-structure-of-authority-why-security-is-not-a-separable-concern.pdf>
- Companion analysis and insights: [[Miller, Tulloh & Shapiro (2005) The Structure of Authority — Analysis]], [[Miller, Tulloh & Shapiro (2005) The Structure of Authority — Insights]]

## Relations

- relates_to::[[Human Authority Over Augmentation Systems]]
  - The paper operationalizes what "boundary-setting" means at the code level: the user's designation act is the authority grant, and the capability model enforces that act structurally

- relates_to::[[Authority Flows from the Person]]
  - "Only connectivity begets connectivity" — authority cannot be exercised except through reference paths the human principal established, expressing at the code level what this principle states at the design level

- relates_to::[[Orchestrator-Worker Separation in Personal Multi-Agent Systems]]
  - The TCB nesting insight directly informs how to scope orchestrator authority in multi-agent systems; the orchestrator is in the worker's TCB, the human in the orchestrator's TCB

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
  - Allen's "least and necessary" design criteria for SSI apply the same authority-minimization logic to identity architecture that Miller et al. apply to software architecture

- relates_to::[[Allen (2021) Principal Authority]]
  - Principal authority in agency law (the principal retains authority; agents act within delegated scope) maps onto the capability model's reference-as-permission: delegation is scoped, revocable, and does not transfer ultimate authority

- relates_to::[[Values Precede Technical Decisions]]
  - The paper argues that capability security follows from taking modularity values seriously — security is not a separate value added later but an implication of the values already present in good software design

- relates_to::[[Mark S. Miller]]
  - Primary author; developer of the E language, Agoric smart contracts, and the object-capability security model

- relates_to::[[Principle of Least Authority]]
  - The paper is the most thorough available account of how POLA applies across levels of system composition and why it requires capability architecture rather than ACL bolting
