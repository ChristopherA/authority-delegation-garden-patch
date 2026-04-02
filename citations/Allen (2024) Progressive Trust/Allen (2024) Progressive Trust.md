---
created: 2026-03-19
author: Christopher Allen
citation_slug: allen-2024-progressive-trust
publication_year: 2024
canonical: "https://developer.blockchaincommons.com/progressive-trust/"
brief_summary: "Christopher Allen's progressive trust framework: trust deepens through stages from initial contact to full collaboration, with each stage requiring verification before advancing. Not binary (trusted/untrusted) but a progression where disclosure, authentication, and commitment deepen together. Provides the conceptual foundation for IFP's progressive authentication and disclosure tier models."
tagline: "Trust deepens through verifiable stages, not binary trusted/untrusted switches"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Christopher Allen]]

# Allen (2024) Progressive Trust

## Bibliographic Entry

***Progressive Trust***, 2024, [developer reference], *Christopher Allen*, Blockchain Commons. Retrieved from https://developer.blockchaincommons.com/progressive-trust/

## Summary

Progressive trust rejects the binary trusted/untrusted model. Trust is a progression: initial contact → identity verification → context exchange → commitment → collaboration, with each stage requiring verification before advancing. The framework applies to both human relationships and technical systems — authentication, disclosure, and commitment deepen together rather than being set to maximum strength upfront.

## Key Points

**Trust is not binary.** Systems that model trust as trusted/untrusted miss the spectrum between first contact and deep collaboration. Progressive trust maps this spectrum explicitly.

**Verification before advancement.** Each stage of trust deepening requires some form of verification — not necessarily cryptographic, but appropriate to the stage. A shared introduction (Level 0 in IFP terms) is sufficient for initial contact; verified public keys (Level 2) are appropriate for sustained exchange.

**Disclosure deepens with trust.** What you share is proportional to how much trust has been established. This is not a privacy setting — it is a natural consequence of the relationship stage.

**Commitment deepens with trust.** Early-stage relationships involve low-commitment exchanges (gossip, context sharing). Deeper trust enables higher-commitment actions (recommendations, collaboration, shared projects).

**Applies to both human and technical systems.** The same progressive model governs how people build trust in face-to-face relationships and how agents build trust in protocol exchanges.

## Influence

Progressive trust is the conceptual foundation for two of IFP's core models: progressive authentication (IFP-5, four levels from shared secret to DID-bound identity) and disclosure tiers (IFP-12, six tiers from public to close). IFP operationalizes progressive trust for agent-to-agent communication.

## Sources

- https://developer.blockchaincommons.com/progressive-trust/

## Relations

- relates_to::[[Progressive Authentication as Trust Deepening]]
  - IFP's four authentication levels implement progressive trust for agent identity verification.

- relates_to::[[Disclosure Tier Hierarchy for Persona-Peer Relationships]]
  - IFP's disclosure tiers implement progressive trust for information sharing boundaries.

- relates_to::[[Granularity of Progressive Authentication Stages]]
  - The progressive trust framework describes a spectrum — the inquiry asks whether IFP's four discrete stages capture the right boundaries.

- relates_to::[[Progressive Disclosure Over Eager Loading]]
  - Progressive disclosure is the information-sharing expression of progressive trust.

- relates_to::[[Authority Flows from the Person]]
  - Progressive trust assumes the person controls their own trust progression — no external authority decides when to deepen.

- relates_to::[[Conversation Temperature as Protocol Cadence Spectrum]]
  - Temperature and trust deepen in parallel — cool conversations at low trust, hot collaboration at high trust

- relates_to::[[Allen (2022) Progressive Trust]]
  - The 2022 developer reference operationalizes the concepts here with implementation vocabulary and domain examples; this node provides the why, the developer reference provides the how

- relates_to::[[Allen (2023) A Laypersons Intro to Schnorr]]
  - Progressive trust architectures can use threshold signatures for escalating trust levels — requiring more signers as trust requirements increase

- relates_to::[[Allen (2023) Data Minimization and Selective Disclosure]]
  - Progressive trust requires a disclosure mechanism; this article specifies the technical requirements for selective disclosure as that mechanism

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
  - Progressive trust is the interaction model for implementing necessary access — trust and data disclosure increase incrementally based on demonstrated need

- relates_to::[[Allen (2023) Open Silicon]]
  - Hardware trust is the base layer of progressive trust: trust cannot progressively increase if the hardware foundation is unverified

- relates_to::[[Allen (2023) Problems of Cryptographic Agility]]
  - Progressive trust's verification phases depend on cryptographic operations; constrained choice simplifies verification across the lifecycle

- relates_to::[[Allen (2024) Building Trust in Gradients]]
  - The blog post operationalizes the lifecycle phases described in this developer reference; together they form a concept-specification pair

- relates_to::[[Allen (2025) Fair Witnessing in a Decentralized World]]
  - Fair witnessing provides the disclosure format that progressive trust requires; progressive trust describes the dynamics, fair witnessing provides the data structure

- relates_to::[[Allen (2025) How My Values Inform Design]]
  - Progressive Trust is developed as a values-to-design example in the appendix of the values article

- relates_to::[[Allen (2025) Interop What Is It Good For]]
  - Progressive trust operates across system boundaries; interoperability enables the trust-building interactions that progressive trust describes.
