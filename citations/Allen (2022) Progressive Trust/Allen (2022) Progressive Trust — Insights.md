---
part_of: "[[Allen (2022) Progressive Trust]]"
role: insights
created: 2026-03-29
brief_summary: "Extraction candidates from Allen (2022) on progressive trust: Trust Begins with Context pattern, Trust Registry as Power Concentration pattern, the three-model comparison, the four required technical capabilities, and the relationship between this founding article and the 2024 lifecycle specification."
---

- is_a::[[Citation Form]]
- has_status::[[Budding Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]

part_of::[[Allen (2022) Progressive Trust]]

# Insights: Allen (2022) Progressive Trust

## Lens Perspectives

**Why this matters for the garden:** This article is the pivot point in Allen's progressive trust arc. The 2004 post introduced the concept. This 2022 article repositions it as a comprehensive alternative to trust registries and zero-trust architectures. Everything that follows -- the data minimization framework, the developer reference, the eleven-phase lifecycle -- builds on the argument established here. Any garden model of progressive trust traces back to this article as the architectural position statement.

**Why this matters for estate architecture:** The estate's own trust model is implicitly progressive. External tools, AI agents, and collaborators gain access to estate knowledge gradually based on demonstrated trustworthiness and need. The estate does not consult a "trust registry" to determine what agents can access. It builds trust through interaction: limited access first, deeper access as trust is established. The four technical capabilities Allen identifies (data minimization, elision, escrowed encryption, selective disclosure) map to estate architecture requirements for knowledge boundary management.

## Garden Node Candidates

**Extract as Pattern:**

- [[Trust Begins with Context Not Identity]] -- In progressive trust, the first operation is context assessment ("is this worth my time?"), not identity verification ("who are you?"). Systems that start with identity verification skip the most natural phase of human trust-building. Context assessment includes shared interests, shared space, shared connections -- all evaluated before identity is established.
  - [source: analysis -- named from article's conference meeting metaphor]
  - Ghost link: [[Trust Begins with Context Not Identity]]

- [[Trust Registry as Power Concentration]] -- Trust registries are framed as security infrastructure but function as governance infrastructure. Whoever controls the registry controls who is considered trustworthy. The registry operator may optimize for their own interests, focus on risks of powerful parties, and create expensive dependencies. This is not a security decision -- it is a power decision.
  - [source: direct from article, with analytical extension]
  - Ghost link: [[Trust Registry as Power Concentration]]

**Extract as Model:**

- [[Three Trust Models Compared]] -- Classical trust (static verification via passwords/certificates), zero-trust (centralized registry consultation), progressive trust (bilateral, graduated, dynamic). Classical trust is static and compromisable. Zero-trust concentrates power in the registry. Progressive trust distributes trust-building to the bilateral relationship.
  - [source: direct from article]
  - Ghost link: [[Three Trust Models Compared]]

**Extract as Principle:**

- [[Trust Gaps Are Informative]] -- Progressive trust accepts that trust is always built on incomplete information. What someone chooses not to share is itself information about their trust level. Systems should "allow for gaps" rather than flag missing information as a risk. This is the opposite of trust-completeness requirements in traditional systems.
  - [source: direct from article -- "allow for gaps" design requirement]
  - Ghost link: [[Trust Gaps Are Informative]]

- [[Technical Architecture Determines Human Rights Outcomes]] -- Trust registry architecture that can be coerced means all participants' trust decisions can be coerced. Progressive trust, by distributing trust-building, resists coercion because there is no central point to pressure. Architecture is not neutral -- it enables or prevents specific rights outcomes.
  - [source: direct from article -- human rights framing of architectural choice]
  - Ghost link: [[Technical Architecture Determines Human Rights Outcomes]]

**Extract as Inquiry:**

- [[How Does Progressive Trust Defend Against Trust Escalation Attacks]] -- A sophisticated adversary could game progressive trust by passing early phases (appearing trustworthy in low-stakes interactions) to exploit access gained at later phases. The 2022 article identifies this pattern in general ("gray areas") but does not specify defenses.
  - [source: analysis -- second-order critique, gap identification]
  - Ghost link: [[How Does Progressive Trust Defend Against Trust Escalation Attacks]]

## Ghost Links (Nodes Not Yet in Garden)

- [[Trust Begins with Context Not Identity]] -- Pattern: context assessment before identity verification
- [[Trust Registry as Power Concentration]] -- Pattern: registries as governance disguised as security
- [[Three Trust Models Compared]] -- Model: classical vs. zero-trust vs. progressive
- [[Trust Gaps Are Informative]] -- Principle: what is withheld reveals trust level
- [[Technical Architecture Determines Human Rights Outcomes]] -- Principle: architecture is not neutral
- [[How Does Progressive Trust Defend Against Trust Escalation Attacks]] -- Inquiry: gaming the graduation
- [[Trust Escalation Attack]] -- Gloss: adversary passes early trust phases to exploit later access
- [[Elision and Redaction]] -- Gloss: removing or masking information to control disclosure
- [[Escrowed Encryption]] -- Gloss: future enforcement of information commitments
- [[Trust Dynamics Over Time]] -- Model: trust as evolving process, not fixed state

## Connections to Existing Garden Nodes

**Connects to [[Allen (2024) Building Trust in Gradients]]:**
The 2024 article provides the eleven-phase lifecycle that this 2022 article argues for but does not specify. This article provides the *why* (the three-model comparison, the trust registry critique, the human rights argument). The 2024 article provides the *what* (the phases, the contractor scenario, the operational detail). Together they form an argument-specification pair.
[source: direct -- 2024 article explicitly extends this 2022 article]

**Connects to [[Allen (2024) Progressive Trust]]:**
The developer reference at Blockchain Commons operationalizes the concepts in this article with implementation vocabulary and domain examples. The developer reference is the *how* to this article's *why*.
[source: direct -- developer reference covers the same conceptual territory with implementation focus]

**Connects to [[Allen (2023) Data Minimization and Selective Disclosure]]:**
This 2022 article names four required technical capabilities (data minimization, elision, escrowed encryption, selective disclosure). The 2023 data minimization article develops the first and last of these in depth: the three-axis minimization framework and the cryptographic selective disclosure taxonomy. They are the technical depth behind this article's capability requirements.
[source: direct -- 2023 article was written to develop capabilities named here]

**Connects to [[Allen (2016) The Path to Self-Sovereign Identity]]:**
Self-sovereign identity provides the philosophical framework; progressive trust provides the trust-building model compatible with that framework. Trust registries violate self-sovereign identity by concentrating trust decisions in a third party. Progressive trust preserves self-sovereignty by keeping trust decisions bilateral.
[source: garden-level inference -- progressive trust is the trust model for self-sovereign identity]

**Connects to [[Allen (2023) Origins of Self-Sovereign Identity]]:**
Allen's living systems theory of identity (identity as membrane) provides the biological metaphor for progressive trust. The membrane is selectively permeable; progressive trust defines the selection criteria. This 2022 article does not use the membrane metaphor explicitly, but the 2024 Building Trust in Gradients article connects them.
[source: garden-level inference -- progressive trust operationalizes the membrane model]

**Connects to [[Allen (2025) The Exodus Protocol]]:**
Exodus Protocols protect infrastructure from centralized capture. Progressive trust protects trust-building from centralized capture (trust registries). Both resist the same mechanism: concentration of authority in a single entity that can be coerced or can pursue self-interested goals. Exodus Protocols address infrastructure autonomy; progressive trust addresses trust autonomy.
[source: garden-level inference -- parallel resistance to centralized capture]

**Connects to [[Allen (2021) Principal Authority]]:**
Principal authority (the individual as the root of their own authority) requires a trust model where the individual controls their own trust decisions. Progressive trust is that model. Trust registries violate principal authority by delegating trust decisions to a registry operator.
[source: garden-level inference -- principal authority requires progressive trust]

## Key Tensions for Garden Exploration

**Progressive trust and zero-trust are less incompatible than Allen implies.** The zero-trust principle ("never assume trust, always verify") is compatible with progressive trust ("build trust gradually through verified interactions"). Allen's real target is trust registries and trust frameworks, not the zero-trust philosophy itself. A more nuanced treatment would separate the zero-trust principle from its trust-registry implementations.

**The four technical capabilities span multiple maturity levels.** Data minimization is a policy principle with well-understood regulatory backing. Elision/redaction has working implementations (Gordian Envelope). Escrowed encryption exists but has limited deployment. Cryptographic selective disclosure (zero-knowledge proofs at scale) remains largely aspirational. The progressive trust architecture requires all four, but they are at different readiness levels.

**This article is the argument; the specification came two years later.** The 2022 article's lack of lifecycle phases is not a flaw -- it is setting up the need that the 2024 article fulfills. But it means that citing this article alone gives only the architectural argument, not the operational model. Both are needed for a complete picture.

## Extraction Targets

1. Trust Begins with Context -> [[Pattern Form]] named [[Trust Begins with Context Not Identity]]
2. Trust registry power -> [[Pattern Form]] named [[Trust Registry as Power Concentration]]
3. Three trust models -> [[Model Form]] named [[Three Trust Models Compared]]
4. Trust gaps -> [[Principle Form]] named [[Trust Gaps Are Informative]]
5. Architecture and rights -> [[Principle Form]] named [[Technical Architecture Determines Human Rights Outcomes]]
6. Trust escalation attacks -> [[Inquiry Form]] named [[How Does Progressive Trust Defend Against Trust Escalation Attacks]]
