---
created: 2026-03-29
author: Christopher Allen
citation_slug: allen-2023-least-necessary
publication_year: 2023
canonical: https://www.lifewithalacrity.com/article/musings-least-necessary/
brief_summary: "Allen presents six security design patterns in a 2x3 taxonomy: least privilege, least authority, and least access (restrictive) paired with their inside-out counterparts — necessary privilege, necessary authority, and necessary access (enabling). Traces the lineage from Saltzer/Schroeder through Miller, then extends into digital data access for self-sovereign identity and verifiable credentials."
tagline: "Six design patterns for managing permissions, authority, and data access — and their inside-out counterparts"
---

- is_a::[Citation Form](../forms/Citation%20Form.html)
- has_status::[Budding Stage](../forms/Budding%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑
- cites_work_by::[[Christopher Allen]]↑

# Allen (2023) Least and Necessary Design Patterns

## Bibliographic Entry

* _**Musings of a Trust Architect: Least & Necessary Design Patterns**_ (2023). [blog post]. _Allen, Christopher._ Life With Alacrity, September 26, 2023. Retrieved 2026-03-29 from: <https://www.lifewithalacrity.com/article/musings-least-necessary/>

## Summary

Allen traces the evolution of security design patterns from Saltzer and Schroeder's Principle of Least Privilege (1975) through Mark Miller's Principle of Least Authority (2006) to a new Principle of Least Access focused on digital data in the self-sovereign identity context. He then applies his "inside-out" methodology, inverting each restrictive pattern into an enabling counterpart: necessary privilege, necessary authority, and necessary access. The resulting 2x3 taxonomy provides both defensive (minimization) and constructive (negotiation) tools for credential system designers.

## Key Points

**Least privilege to least authority is a scope expansion.** Saltzer and Schroeder's least privilege considers individual permissions in isolation. Miller's least authority recognizes that privileges form a web of transitive authority — a user who can access a program that accesses a resource effectively has authority over that resource. Many modern discussions conflate the two, but the scope difference matters.

**Least access extends the lineage into data.** Where least privilege and least authority address permissions to do things, Allen's least access addresses permissions to see data. The extension is motivated by self-sovereign identity and verifiable credentials, where the primary concern is not system access but data exposure. Least access incorporates transitive authority's ecosystem awareness, specifically targeting correlation opportunities.

**The inside-out methodology is a general-purpose design tool.** Allen's distinctive contribution is the inversion technique: take an established restrictive pattern, flip the orientation from "what to limit" to "what to enable," and the resulting pattern reveals design insights the original framing obscured. He demonstrates the method on both the least/necessary family and on selective disclosure (which inverts to selective correlation).

**Necessary-framing resets design boundaries.** The restrictive framing forces designers to enumerate and block all possible abuses — a potentially endless task. The necessary framing asks what the user or system actually needs, making everything else excluded by default. Allen argues this produces more scalable, adaptable, and user-friendly systems.

**Necessary access creates a negotiation foundation.** In credential systems, necessary access inverts the interaction model: instead of a verifier requesting whatever data it wants (and the holder trying to minimize disclosure), the system declares its data needs upfront. The holder then has complete information for a consent decision. This is a bilateral negotiation, not a unilateral extraction.

**Selective correlation acknowledges that correlation is sometimes the objective.** The inside-out of selective disclosure asks "what data should I purposefully disclose to enable beneficial correlation?" This reframes correlation as sometimes serving the user (fraud detection, accountability, identity continuity) rather than always threatening them.

**Dignity, not asset protection, is the motivating frame.** Allen explicitly positions his approach as protecting individuals "who are uniquely due respect and dignity" rather than protecting information assets in the military tradition. This reframing changes what counts as a security failure — not just unauthorized access, but violation of autonomy, privacy, or informed consent.

**The six patterns form a clean taxonomy.** Two orientations (restrictive, enabling) across three scopes (privilege, authority, access) produce a 2x3 matrix that is compact, memorable, and extensible to future pattern families.

**Coercion resistance through architecture.** Allen argues that a datastore implementing least access can refuse to grant improper data requests, negating coercive demands. This is an architectural coercion resistance claim — the system's design prevents improper access regardless of social power dynamics.

## Key Quotes

> "In order to protect privacy, respect individual entitlements, and maintain human dignity, only the minimum amount of data access necessary to achieve a specific goal should be granted."

> "Once I discover a useful design pattern, I often find utility in turning it inside out. This results in a different mindset that can provide new insights into security design."

> "Rather than trying to tamp down all possible abuses, which is potentially an endless task, it instead concentrates a designer's attention on the positive."

> "If a user proactively has access to everything that they need, they'll never bump up against barriers in a system. This can help to reduce the risk of human error and increase user satisfaction by empowering users with the authority they need to perform their tasks effectively."

## Influence

The article synthesizes decades of security design thinking — from Saltzer/Schroeder through Miller to Allen's own extensions — into a compact taxonomy usable by credential system designers. The inside-out methodology transcends the specific patterns and provides a reusable tool for design pattern innovation. Within Allen's corpus, this article provides the design-pattern foundations that later articles on progressive trust, principal authority, and verifiable credentials build upon. The six patterns serve as a checklist for evaluating whether a self-sovereign identity system respects both security and dignity.

## Limitations

**No implementation examples.** The six patterns are described conceptually but the article provides no worked implementations. How a verifiable credential system would concretely implement "necessary access" is left as an exercise.

**Conflict between least and necessary is unaddressed.** The article presents the two pattern families as complementary, but a least-access analysis and a necessary-access analysis of the same system could produce contradictory requirements. The resolution strategy is not discussed.

**Architectural coercion resistance is overstated.** The claim that a datastore refusing improper requests "negates" coercion ignores that coercion in practice operates outside the data system — device confiscation, legal compulsion to decrypt, social pressure. Architectural resistance is one layer, not the whole solution.

## Sources

- Primary: Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." Life With Alacrity, September 26, 2023. <https://www.lifewithalacrity.com/article/musings-least-necessary/>
- Referenced: Saltzer, Jerome H. and Schroeder, Michael D. "The Protection of Information in Computer Systems." (1975)
- Referenced: Miller, Mark S. "Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control." (2006)
- Referenced: Saltzer, Jerome H. "Protection and Control of Information Sharing in Multics." (1973)
- Referenced: Allen, Christopher. "Musings of a Trust Architect: Data Minimization & Selective Disclosure." (2023)
- Referenced: IETF RFC 6973, "Privacy Considerations for Internet Protocols." (2013)
- Referenced: Szabo, Nick. "Interpreting Power: The Principle of Least Authority." (2005)

## Relations

- relates_to::[Allen (2024) Progressive Trust](../citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html)
  - Progressive trust is the interaction model for implementing necessary access — trust and data disclosure increase incrementally based on demonstrated need
- relates_to::[Allen (2021) Principal Authority](../citations/Allen%20(2021)%20Principal%20Authority/Allen%20(2021)%20Principal%20Authority.html)
  - Principal authority defines who decides about data; necessary access defines what data is needed — together they form a two-part authorization test
- relates_to::[Inside-Out Methodology as Design Pattern Innovation](../glosses/Inside-Out%20Methodology%20as%20Design%20Pattern%20Innovation.html)
  - The reusable design tool demonstrated in this article — invert restrictive patterns to discover enabling ones

- relates_to::[Dignity Not Asset Protection as Security Design Frame](../glosses/Dignity%20Not%20Asset%20Protection%20as%20Security%20Design%20Frame.html)
  - The motivating principle: security protects people with dignity, not assets with classifications

- relates_to::[[Allen (2023) Origins of Self-Sovereign Identity]]↑
  - The dignity framing connects directly to self-sovereign identity's commitment to individual autonomy over institutional control
- relates_to::[[Allen (2025) How My Values Inform Design]]↑
  - Dignity-first security is the values-level commitment; these patterns are the design-level implementation
- relates_to::[[Allen (2023) Minimum Viable Architecture]]↑
  - Minimum viable architecture applies the least/necessary logic at the system level — what is the minimum architecture necessary for a viable system?
- relates_to::[[Allen (2023) A Laypersons Intro to Schnorr]]↑
  - Both articles share the same publication period and provide foundational design-pattern knowledge for the self-sovereign identity stack
- relates_to::[[Allen (2023) Open Silicon]]↑
  - The trust stack is transitive authority: trusting an application requires trusting every layer beneath it, including the hardware that executes the cryptographic operations
