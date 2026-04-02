---
part_of: "[[Allen (2024) Building Trust in Gradients]]"
role: insights
created: 2026-03-28
brief_summary: "Extraction candidates from Allen (2024) on progressive trust: Trust Compression for Onboarding pattern, Trust as Selective Permeability model, the eleven-phase lifecycle as protocol specification, and connections to sovereignty membrane architecture."
---

- is_a::[[Citation Form]]
- has_status::[[Budding Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]

part_of::[[Allen (2024) Building Trust in Gradients]]

# Insights: Allen (2024) Building Trust in Gradients

## Lens Perspectives

**Why this matters for the garden:** The Progressive Trust Life Cycle is the operational protocol for the sovereignty membrane concept that runs through Allen's entire intellectual project. Where the self-sovereign identity articles define what sovereignty means and the edge identifier articles define the cryptographic substrate, this article specifies how trust actually flows through the membrane over time. Any garden model of sovereign identity needs this lifecycle as its dynamic component.

**Why this matters for estate architecture:** The estate's own trust boundaries (what passes between household and garden, between garden and commons, between estate and external agents) are instances of progressive trust. The estate does not expose all knowledge to all agents at once; it progressively discloses based on accumulated trust. The eleven-phase model could structure how new agents or new external connections gain access to estate knowledge.

## Garden Node Candidates

**Extract as Pattern:**

- [[Trust Compression for Onboarding]] — Platform business models compress graduated trust to binary (grant/deny) because graduated trust slows user acquisition. The compression is invisible to users who never experienced the alternative. Once compressed, the platform owns the trust model. Counter-pattern: progressive trust restores gradients.
  - [source: analysis — named from article's historical argument about commercialization]
  - Ghost link: [[Trust Compression for Onboarding]]

- [[Trust as Selective Permeability]] — Progressive trust operationalizes the sovereignty membrane: each lifecycle phase opens the membrane for a specific type of exchange under specific conditions. Binary trust treats the membrane as a door (open/closed). Progressive trust treats it as a cell membrane (selectively permeable based on recognition).
  - [source: analysis — synthesized from article's lifecycle + Allen's membrane metaphor from Origins of Self-Sovereign Identity]
  - Ghost link: [[Trust as Selective Permeability]]

**Extract as Model:**

- [[Progressive Trust Life Cycle]] — Eleven-phase model for graduated trust-building: Context, Introduction, Wholeness, Proofs, References, Requirements, Approval, Agreement (optional), Fulfillment, Escalation (optional), Dispute (optional). Each phase represents a distinct trust operation with specific inputs and state changes. Mirrored by both parties simultaneously.
  - [source: direct from article]
  - Ghost link: [[Progressive Trust Life Cycle]]

**Extract as Principle:**

- [[Trust Deepening Requires Bilateral State]] — Trust-building is mirrored by both parties. Neither grants trust to the other; both maintain independent assessments. This creates a peer protocol, not a client-server relationship. Any implementation must be architecturally peer-to-peer.
  - [source: analysis — derived from article's brief mention of dual-sided mirroring]
  - Ghost link: [[Trust Deepening Requires Bilateral State]]

**Extract as Inquiry:**

- [[How Does Progressive Trust Handle Adversarial Participants]] — The lifecycle assumes willing participants engaging in good faith. It has no phase for detecting adversarial intent — a party who deliberately passes early phases to exploit access gained at later phases. What adaptations are needed for adversarial digital contexts?
  - [source: analysis — second-order critique]
  - Ghost link: [[How Does Progressive Trust Handle Adversarial Participants]]

- [[Can Progressive Trust Phases Regress]] — The lifecycle's linear presentation implies forward-only progression. But real trust relationships involve regression, repair, and re-evaluation. What does mid-lifecycle regression look like? How does a relationship move from phase 6 back to phase 3?
  - [source: analysis — second-order critique]
  - Ghost link: [[Can Progressive Trust Phases Regress]]

## Ghost Links (Nodes Not Yet in Garden)

- [[Trust Compression for Onboarding]] — Pattern: platform simplification of trust for conversion
- [[Trust as Selective Permeability]] — Model: progressive trust as operational protocol for sovereignty membrane
- [[Progressive Trust Life Cycle]] — Model: eleven-phase graduated trust framework
- [[Trust Deepening Requires Bilateral State]] — Principle: peer-to-peer trust, not server-granted
- [[How Does Progressive Trust Handle Adversarial Participants]] — Inquiry: adversarial robustness gap
- [[Can Progressive Trust Phases Regress]] — Inquiry: mid-lifecycle trust regression
- [[Binary Trust as Trust Regression]] — Gloss: commercial platforms regressed trust from graduated to binary
- [[Trust Spectrum Quantification]] — Inquiry: how to measure trust levels within the lifecycle

## Connections to Existing Garden Nodes

**Connects to [[Allen (2024) Progressive Trust]]:**
The developer reference is the implementation companion to this blog post. The blog post argues why and describes the lifecycle narratively. The developer reference provides vocabulary and implementation guidance. They form a concept-specification pair, like the Exodus Protocol and Gordian Club articles.
[source: direct — article explicitly references the developer pages]

**Connects to [[Allen (2024) Edge Identifiers and Cliques]]:**
Edge identifiers create the cryptographic relationships along which progressive trust deepens. A relational edge key between two parties is the cryptographic substrate for their trust-building process. Progressive trust governs *how* trust flows along edges; edge identifiers define *what* the edges are.
[source: garden-level inference — connecting trust lifecycle with cryptographic graph model]

**Connects to [[Allen (2023) Origins of Self-Sovereign Identity]]:**
The membrane metaphor from living systems theory is the philosophical foundation for progressive trust. The membrane is selectively permeable; progressive trust defines the selection criteria at each phase. Allen's self-sovereign identity is not about walls but about controlled openness — progressive trust specifies the control mechanism.
[source: garden-level inference — article quotes the membrane passage from Origins]

**Connects to [[Allen (2025) The Exodus Protocol]]:**
Exodus Protocols protect the *infrastructure* on which trust is built. Progressive trust protects the *process* by which trust is built. If the infrastructure is captured (enshittification), the trust process collapses because parties cannot independently verify or progressively disclose. Exodus Protocols are a prerequisite for progressive trust in hostile environments.
[source: garden-level inference — infrastructure autonomy enables trust autonomy]

## Key Tensions for Garden Exploration

**Progressive trust assumes infrastructure independence.** The lifecycle requires that both parties can independently verify assertions, check references, and assess compliance. If the verification infrastructure is controlled by a single entity (a certificate authority, a platform API), the trust process is captured even if the lifecycle phases are technically followed. This connects to the Exodus Protocol requirement.

**The lifecycle may not scale to many-party trust.** The contractor scenario is dyadic (two parties). The article does not address how the lifecycle works for multi-party trust-building, such as a group forming a cooperative or a community establishing shared governance. The clique articles address the cryptographic layer of multi-party identity but the trust lifecycle for groups remains unspecified.

## Extraction Targets

1. Trust Compression for Onboarding -> [[Pattern Form]] named [[Trust Compression for Onboarding]]
2. Trust as Selective Permeability -> [[Model Form]] or [[Pattern Form]] named [[Trust as Selective Permeability]]
3. Progressive Trust Life Cycle -> [[Model Form]] named [[Progressive Trust Life Cycle]]
4. Bilateral trust state -> [[Principle Form]] named [[Trust Deepening Requires Bilateral State]]
5. Adversarial participants gap -> [[Inquiry Form]] named [[How Does Progressive Trust Handle Adversarial Participants]]
6. Trust regression question -> [[Inquiry Form]] named [[Can Progressive Trust Phases Regress]]
