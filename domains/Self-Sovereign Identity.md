---
created: 2026-03-06
author: Christopher Allen
brief_summary: "Domain index for Self-Sovereign Identity in the garden — 4 nodes covering the principal authority framework from agency law. Self-Sovereign Identity provides the first non-Deep Context Architecture domain content, bridging identity principles to the vault's augmented knowledge architecture."
tagline: "Identity owned by the individual — the first non-Deep Context Architecture domain in the garden"
formatted: "2026-03-14"
---

- is_a::[[Domain Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Garden Precinct]]
- in_precinct::[[Garden Precinct]]

# Self-Sovereign Identity

Self-sovereign identity is the principle that individuals should own and control their digital identity without depending on any external authority. Christopher Allen's 2016 articulation of the 10 Principles of Self-Sovereign Identity established the framework. In this garden, self-sovereign identity nodes focus on the principal authority framework from agency law — how identity rights are delegated, enforced, and protected.

## Scope

**Covers**: The principal authority model (agency law applied to digital identity), authority delegation patterns, enforcement mechanisms, and the bridge between self-sovereign identity principles and the vault's augmented knowledge architecture.

**Does not cover**: Technical standards implementation (DIDs, Verifiable Credentials, DIDComm) — those belong in a future technical self-sovereign identity domain or in [[Digital Identity]]. Also excludes the broader digital identity landscape beyond self-sovereign identity.

## Key Forms

### Principal Authority Framework

- [[Principal Authority as Agency Law for Digital Identity]] — gloss: self-sovereign identity duties and definitions through agency law lens
- [[Authority Conferral Chain]] — model: three delegation types (Type A: full, Type B: constrained, Type C: revocable)
- [[Authority Flows from the Person]] — principle: authority is delegable but not alienable
- [[Three-Part Enforcement Stack]] — pattern: three layers of enforcement (technical, legal, social)

All 4 nodes draw on Christopher Allen's self-sovereign identity article (2016), BCR-2026-xxx spec drafts, and Blockchain Commons discussions.

## Candidate Forms

Potential forms identified from [Blockchain Commons Values & Design Principles](https://www.blockchaincommons.com/musings/ValuesDesign/) — not yet extracted:

### Convictions

- Digital Rights as Fundamental Human Rights — digital rights deserve the same standing as other human rights; not a policy preference but a claim about what rights are

### Principles

- Privacy by Design as Standing Constraint — embed privacy protections into every system as default practice, not as an add-on feature
- Resilience Against Exploitation — architect systems to withstand adversarial threats; autonomy must remain intact under pressure
- Revocable Permissions as Agency Preservation — users retain ongoing control over delegated information; relationships change, permissions must follow
- Data Minimization as Default Practice — minimize data collected; reduces vulnerability surface and respects dignity

### Patterns

- Selective Disclosure and Elision — choices for redaction and elision to control what individuals share; prevents reduction to digital records
- Progressive Trust as Relationship Evolution — systems that reflect the natural evolution of trust, enabling selective disclosure incrementally (bridges [[Synpraxis]])

### Models

- Membrane Analogy for Identity Boundaries — digital identity as a selective boundary (from Living Systems Theory): enabling both individual autonomy and collective participation, like cell membranes that filter while remaining part of a larger ecosystem

## Open Questions

- What additional self-sovereign identity nodes should be extracted? The 10 Principles alone could yield 10 principle nodes.
- How does self-sovereign identity relate to the [[Delegated Decision Authority Spectrum]] boundary? (Currently the spectrum is tagged Deep Context Architecture; the authority concepts bridge both shared language communities.) See [[Domains as Shared Language Communities]].
- Should technical self-sovereign identity standards (DIDs, VCs) be a sub-domain (dialect) or a separate domain page? See [[Domain Vocabulary Evolution]].

## Sources

- Allen, Christopher. "The Path to Self-Sovereign Identity." (2016)
- BCR-2026-xxx spec drafts (Blockchain Commons)
- [[Digital Identity]] — parent map of content in Categories/

## Relations

- relates_to::[[Deep Context Architecture]] — Self-sovereign identity agency law concepts inform the vault's principal authority model
- relates_to::[[Digital Identity]] — Self-sovereign identity is a subset of the broader digital identity field
- relates_to::[[Domains as Shared Language Communities]] — this domain is a shared language community where "principal authority," "LESS Identity," and "trust minimized" carry compressed meaning
- relates_to::[[Domain Vocabulary Evolution]] — open inquiry about sub-domains and cross-domain nodes
