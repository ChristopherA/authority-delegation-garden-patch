---
part_of: "[[Allen (2022) Progressive Trust]]"
role: analysis
created: 2026-03-29
brief_summary: "Primary source analysis of Allen (2022) on progressive trust: the conference meeting as explanatory metaphor, the three-model comparison (classical, zero-trust, progressive), the trust registry critique, and the technical capabilities required for progressive trust architecture."
---

- is_a::[[Citation Form]]
- has_status::[[Budding Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]

part_of::[[Allen (2022) Progressive Trust]]

# Analysis: Allen (2022) Progressive Trust

## The Article's Position in Allen's Progressive Trust Arc

This December 2022 post is the foundational restatement of Allen's progressive trust concept for the decentralized systems era. Allen first wrote about progressive trust in 2004, describing how software should model real-world human group behavior. Eighteen years later, this article repositions that concept as a concrete alternative to both classical trust models and zero-trust architectures in decentralized systems.

The intellectual arc: 2004 (concept introduction) -> 2022 (this article: full argument for decentralized systems) -> 2023 (data minimization as disclosure mechanism) -> 2024 (developer reference: operational vocabulary) -> 2024 (Building Trust in Gradients: eleven-phase lifecycle). This 2022 article is the pivot point where progressive trust transforms from a software design observation into a comprehensive architectural position against trust registries and for human-modeled trust in digital systems.

## The Conference Meeting as Foundational Metaphor

Allen builds the entire progressive trust argument on a single extended metaphor: meeting someone at a conference. The sequence:

1. You listen and understand each other (shared interest as initial credential)
2. You exchange information: shared acquaintances, interests, ideas
3. You unconsciously check if others are listening; adjust behavior accordingly
4. If you meet again, you authenticate earlier credentials
5. As collaboration grows, you seek more credentials and endorsements
6. Eventually, you bring in third parties to witness and enforce obligations

This conference-meeting metaphor is doing significant architectural work. It establishes that:

- **Trust starts with context assessment**, not identity verification. You assess whether the person is worth talking to before asking who they are.
- **Credential exchange is mutual and incremental.** Both parties simultaneously evaluate and are evaluated. Neither party "grants" trust.
- **Environmental awareness is a trust operation.** Checking if others are listening is a privacy operation -- the equivalent of data minimization in physical space.
- **Third parties enter late, not early.** Witnesses and enforcers are brought in only after substantial bilateral trust has been established. This is the opposite of trust registries, where third parties are consulted at the beginning.

**Named Pattern: Trust Begins with Context, Not Identity.** In progressive trust, the first operation is not "who are you?" but "is this worth my time?" Context assessment (shared conference, shared interest) precedes identity verification. Systems that start with identity verification (certificates, passwords, trust registries) skip the most natural phase of human trust-building.

## The Three-Model Comparison

Allen's most architecturally important contribution is the three-way comparison between classical trust, zero-trust, and progressive trust:

**Classical trust**: verify every interaction as "trusted" through authentication mechanisms (passwords, certificates, firewalls). The problem: these mechanisms "can be easily compromised and do not adequately capture the dynamic and evolving nature of trust between people and groups." Classical trust is static -- once authenticated, the trust level does not change.

**Zero-trust**: assume trust should never be relied upon; mandate consultation of a centralized third-party, or more recently a "trust framework" or "trust registry." Allen identifies four specific problems with trust registries:
1. They create centralization and vulnerability to coercion
2. They cannot capture trust dynamics over time
3. They become outdated requiring privacy-breaking "phone home" checks
4. They depend on a third party that may not treat all parties' risks equally

**Progressive trust**: model how trust works in real life -- not as binary state but as dynamic, evolving process built through successive interactions. Trust is built gradually through interactions that "allow parties to test and verify each other's credentials and capabilities."

The progressive trust model does not reject verification (it includes it) or third parties (they enter at late stages). It rejects two things: (a) starting with third-party consultation rather than bilateral assessment, and (b) treating trust as a fixed state rather than an evolving process.

## The Trust Registry Critique as Political Analysis

Allen's critique of trust registries goes beyond technical limitations to political analysis. Trust registries "must rely on a third party to hold and update the registry." This third party:

- May not treat all parties' risks equally
- May focus on mitigating risks of those with more power to influence the registry
- Creates dependency that "is likely to be expensive and only benefits the few"

This is a power analysis, not just a technical analysis. The trust registry concentrates decision-making authority about who is trustworthy in the hands of whoever controls the registry. In Allen's framing, this is not a security architecture -- it is a governance architecture that happens to use security vocabulary. The entity controlling the registry decides the rules of trust for the entire ecosystem.

**Named Pattern: Trust Registry as Power Concentration.** Trust registries are framed as security infrastructure but function as governance infrastructure. Whoever controls the registry controls who is considered trustworthy within the ecosystem. This concentrates power in the registry operator, who may optimize for their own interests rather than the interests of all parties.

This connects to Allen's broader intellectual project: self-sovereign identity is about preventing exactly this kind of power concentration in digital identity systems. Progressive trust is the trust-building model compatible with self-sovereign identity because it does not require ceding trust decisions to a centralized authority.

## Technical Capabilities as Architectural Requirements

Allen identifies four specific technical capabilities required for progressive trust:

1. **Data minimization**: limit shared data to the minimum necessary
2. **Elision/redaction**: allow parties to decide what information to share, removing or masking portions
3. **Escrowed encryption**: allow information and promises to be enforced in the future
4. **Cryptographic selective disclosure**: prevent future data correlation

He frames these as "techniques that we use in real-life when progressively increasing trust with someone else; they just need to be modeled in digital space." This framing is important: the techniques are not inventions for digital systems but digitalizations of existing human practices. When you check if others are listening at a conference (environmental awareness), you are performing real-time data minimization. When you share a business card but not your home address, you are performing selective disclosure.

The design principles Allen specifies are: flexible, scalable, modular (combining and updating atomic credentials as needed), leveraging cryptographic tools (inclusion proofs, zero-knowledge protocols), and using data models that "express how the various sub-credentials are connected, allow for gaps, and minimize undue correlation."

The "allow for gaps" requirement is architecturally distinctive. Most trust models assume complete information or flag missing information as a risk. Allen's model accepts that trust is always built on incomplete information and that the gaps themselves are informative (what someone chooses not to share tells you something about their trust level).

## The Human Rights Framing

Allen consistently frames progressive trust in human rights terms: "This architecture is critical for protecting human rights and dignity, as it allows individuals to defend against coercion and violations of their privacy, autonomy, agency, and control."

This is not incidental -- it connects progressive trust to Allen's broader argument that technical architecture determines human rights outcomes. A trust registry that can be coerced (by governments, by powerful companies) means the trust decisions of all participants can be coerced. Progressive trust, by distributing trust-building to the bilateral relationship, resists coercion because there is no central point to pressure.

The specific rights Allen names -- privacy, autonomy, agency, control -- are the same rights he identifies in the self-sovereign identity articles. Progressive trust is the trust-building model that protects these rights; trust registries are the model that threatens them.

## Second-Order Analysis: Strengths and Gaps

**The "gray areas" acknowledgment is the article's most honest moment.** Allen notes that "trust is not binary; instead, it includes more gray areas" and that "trust is also not universal: each party will have a different view about it." This means progressive trust cannot be reduced to a simple algorithm -- it requires each party to understand their own risk tolerance and apply it contextually. This is both the model's strength (it preserves human judgment) and its implementation challenge (it cannot be fully automated).

**No lifecycle phases are specified.** This 2022 article describes progressive trust conceptually but does not specify phases. The eleven-phase lifecycle appears only in the 2024 "Building Trust in Gradients" article. This 2022 article provides the argument for why progressive trust is needed; the 2024 article provides the operational specification. They are complementary but distinct contributions.

**The zero-trust comparison is somewhat unfair.** Allen compares progressive trust to a specific implementation of zero-trust (trust registries) rather than to the zero-trust principle itself (never assume trust, always verify). The zero-trust principle is actually compatible with progressive trust -- you can "never assume trust" while still "building trust gradually." Allen's real target is trust registries and trust frameworks, not the zero-trust philosophy per se.

**No threat model for progressive trust itself.** Allen identifies risks of classical trust and zero-trust but does not systematically analyze risks of progressive trust. A sophisticated adversary could game the progressive trust process by passing early phases (appearing trustworthy in low-stakes interactions) to exploit access gained at later phases. The article does not address this "trust escalation attack."

**The 2004 connection creates intellectual continuity.** Allen explicitly connects this article to his 2004 post, creating an eighteen-year arc of progressive trust thinking. This continuity is a strength -- the concept was not invented for the current moment but has been developing across two decades of practice.
