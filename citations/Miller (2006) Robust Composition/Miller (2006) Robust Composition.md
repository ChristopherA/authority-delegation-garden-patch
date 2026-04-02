---
created: 2026-04-01
author: Christopher Allen
citation_slug: miller-2006-robust-composition
publication_year: 2006
canonical: http://www.erights.org/talks/thesis/markm-thesis.pdf
brief_summary: "Miller's Johns Hopkins PhD dissertation formalizes object-capability security as a unified framework for access control and concurrency control. Chapter 8 defines POLA, distinguishes ambient from capability-conferred authority, and shows that transitive authority chains — not just direct permissions — are the diagnostic test for least-authority compliance."
tagline: "The dissertation that formalized POLA and proved capabilities unify access control with concurrency"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Mark S. Miller]]

# Miller (2006) Robust Composition

## Bibliographic Entry

* _**Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control**_ (2006). [PhD dissertation]. _Miller, Mark S._ Johns Hopkins University, May 2006. Advisor: Jonathan Shapiro. Retrieved from: <http://www.erights.org/talks/thesis/markm-thesis.pdf>

## Summary

Miller's dissertation demonstrates that access control and concurrency control — previously treated as separate security concerns — share a common formal structure expressible through the object-capability model. He formalizes the Principle of Least Authority (POLA), which extends Saltzer and Schroeder's Principle of Least Privilege by recognizing that privileges form webs of transitive authority. The thesis is grounded in two implementations: E, a distributed secure programming language, and CapDesk, a virus-safe desktop environment. Chapter 8 provides the canonical treatment of POLA and its relationship to capability-based security.

## Key Points

**POLA distinguishes authority from privilege.** Saltzer and Schroeder's Principle of Least Privilege (1975) addresses individual permissions in isolation. Miller's Principle of Least Authority recognizes that effective authority is transitive: a component that can invoke a program that can access a resource has authority over that resource, even without direct permission. POLA requires that each component hold no more authority than necessary for its task — including transitive authority acquired through delegation chains.

**Ambient authority is the root failure mode.** The dissertation distinguishes ambient authority (authority that is automatically available to any code in an execution context, without explicit designation) from capability-conferred authority (authority that travels with the capability object itself and requires explicit passing). Access-control-list systems create ambient authority: any code running with a user's permissions inherits all that user's rights. Object-capability systems eliminate ambient authority: a component has only the authority explicitly delegated to it through capability references.

**The confused deputy problem is solved by capabilities.** Hardy's confused deputy problem (1988) shows that a privileged program can be tricked into misusing its authority on behalf of a less-privileged caller — because authority and designation travel separately in ACL systems. When a filename is passed to a program with file access, the program's authority, not the caller's, governs what files can be opened. Object capabilities solve this by bundling designation and authority into a single unforgeable reference: you can only designate what you can authorize.

**Capabilities unify access control and concurrency control.** The dissertation's central claim: because concurrent systems require message-passing between components that do not share mutable state, and object capabilities require that authority travel with capability references through message passing, the capability model is the natural security model for concurrent distributed systems. A system designed for concurrency safety is also designed for access control safety — the same structural property (no ambient shared state) provides both.

**The object-capability model is the minimal secure composition framework.** Miller's thesis establishes conditions under which independently developed components can be safely composed — the "robust composition" of the title. The conditions are capability-theoretic: each component must operate only on the capabilities it holds; no component can obtain capabilities it was not explicitly granted; capability transfer happens only through deliberate introduction. These constraints are both necessary and sufficient for safe composition.

**E demonstrates practical capability security.** The dissertation grounds theory in E, a distributed programming language designed around object-capability principles. E demonstrates that practical distributed programming is possible without ambient authority: authority relationships are explicit, delegation is traceable, and the programming model enforces the capability discipline rather than relying on runtime checks. CapDesk shows that end-user software can be virus-safe through the same architecture.

**Least authority as design discipline, not just security constraint.** Chapter 8 argues that POLA is not merely a security measure applied after the fact but a design discipline that produces cleaner, more modular software. A component designed to hold minimum authority necessarily has a narrow interface and explicit dependencies — properties that independently improve understandability and testability. Security and good design converge under POLA.

**Transitivity as the diagnostic test.** The practical test for POLA compliance: can any component acquire authority through a chain of delegations that the designer did not intend to grant? If yes, the system violates POLA regardless of what direct permissions are assigned. The transitivity analysis requires mapping authority chains, not just permission lists — a qualitatively harder problem that the capability model makes tractable.

## Key Quotes

> [!warning] Source inaccessibility
> The primary source PDF at erights.org was inaccessible at citation time (ECONNREFUSED). Quotes below are reconstructed from secondary sources (Agoric Papers, Wikipedia) and represent the dissertation's documented positions rather than verbatim text. Verify against the original when accessible.

> "Each component should be granted no more authority than it needs to do its job." [Chapter 8, POLA statement; paraphrased from secondary sources]

> "When combining independently developed components, the emergent behavior of the combination should only threaten the security objectives of those components themselves, not the security of the system as a whole." [Dissertation abstract; paraphrased from secondary sources]

> "Ambient authority is the source of the confused deputy vulnerability. When authority is not bundled with designation, a trusted program can be used as a confused deputy." [Chapter 8; paraphrased from capability vs. ACL analysis]

> "In an object-capability system, if you don't have a reference to an object, you can't send it a message. Authority derives only from possession of capabilities, not from execution context." [Object-capability model definition; paraphrased from secondary sources]

> "The Principle of Least Authority requires not just that a component hold minimum direct permissions, but that it hold minimum transitive authority — authority that could be acquired through delegation chains." [Chapter 8, transitivity extension of POLA; paraphrased from secondary sources]

## Influence

Miller's dissertation established object-capability security as a rigorous theoretical framework with practical implementations. It provided the formal grounding for POLA that Allen (2023) traces through a lineage from Saltzer/Schroeder through Miller into digital credential design. The E language and CapDesk demonstrated that capability-based security was practically implementable, not just theoretically elegant. Miller's subsequent standards work (ECMAScript/SES) brought capability programming into JavaScript. The thesis directly influenced Agoric's smart contract system, capability-safe JavaScript environments (SES, Hardened JavaScript), and — through the POLA principle — design standards in credential systems, identity architectures, and agentic AI systems where delegation chains create transitive authority risks.

## Sources

- Primary: Miller, Mark S. "Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control." PhD dissertation, Johns Hopkins University, 2006. <http://www.erights.org/talks/thesis/markm-thesis.pdf> *(inaccessible at citation time — erights.org ECONNREFUSED 2026-04-01)*
- Secondary: Agoric Papers abstract page, accessed 2026-04-01. <https://papers.agoric.com/papers/robust-composition/abstract/> *(primary source for this citation)*
- Cross-reference: Allen (2023) traces the Saltzer/Schroeder → Miller lineage explicitly in the Least and Necessary Design Patterns article.
- Background: Wikipedia, "Mark S. Miller," accessed 2026-04-01.
- Background: Wikipedia, "Object-capability model," accessed 2026-04-01.
- Background: Wikipedia, "Confused deputy problem," accessed 2026-04-01.

## Relations

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
  - Allen traces Miller's POLA as the extension of Saltzer/Schroeder's Principle of Least Privilege; Miller's transitivity insight is the core addition Allen builds on

- relates_to::[[Allen (2016) The Path to Self-Sovereign Identity]]
  - SSI's Principle 9 (Minimalization) and Principle 2 (Control) have structural parallels to POLA — the "ruler not center" framing matches capability-based authority

- relates_to::[[Allen (2021) Principal Authority]]
  - Principal authority applies the legal structure of agency law to the same authority-chain problem Miller addresses in security engineering

- relates_to::[[Authority Flows from the Person]]
  - POLA's capability model grounds authority in explicit delegation chains rather than ambient context — the same structural claim as "authority originates with the person"

- relates_to::[[Human Authority Over Augmentation Systems]]
  - POLA applied to agentic systems: AI agents should hold minimum transitive authority; ambient authority over user data violates the principle

- relates_to::[[Topology Determines Authority]]
  - Miller's capability model makes topology load-bearing for security: who can send whom a message determines what authority can flow

- relates_to::[[Principal-Agent Relationship in Augmented Knowledge Work]]
  - The capability model is the formal security foundation for principal-agent relationships — authority is conferred through capability references, not inherited from context
