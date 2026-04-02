---
created: 2026-03-22
author: Christopher Allen
citation_slug: allen-2016-path-ssi
publication_year: 2016
canonical: https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/
brief_summary: "Allen names the concept of self-sovereign identity, proposes a four-phase history of digital identity (centralized, federated, user-centric, self-sovereign), and defines ten principles for SSI systems. Published April 2016 before RWOT2 and the ID2020 Summit at the United Nations. ~6,000 words."
tagline: "The article that named self-sovereign identity and set its ten design principles"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Christopher Allen]]

# Allen (2016) The Path to Self-Sovereign Identity

## Bibliographic Entry

* _**The Path to Self-Sovereign Identity**_ (2016). [blog post]. _Allen, Christopher._ Life with Alacrity, April 26, 2016. Retrieved 2026-03-22 from: <https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/>

## Summary

Allen proposes that digital identity has evolved through four phases — centralized, federated, user-centric, and self-sovereign — and that the fourth phase requires users to be "rulers" rather than merely the "center" of their identity process. He defines ten principles for self-sovereign identity systems: Existence, Control, Access, Transparency, Persistence, Portability, Interoperability, Consent, Minimalization, and Protection. Written to launch community dialogue at RWOT2 and the ID2020 Summit at the United Nations.

## Key Points

**The ruler vs. center distinction.** Allen's key conceptual move: prior user-centric approaches put individuals at the center of identity flows while leaving ownership with registering entities. Self-sovereign identity makes the individual the ultimate authority — not merely consulted but sovereign. Every subsequent SSI debate about compliance with the principles turns on this distinction.

**The four-phase taxonomy as diagnostic tool.** The progression from centralized to federated to user-centric to self-sovereign is not just historical description — it is a diagnostic framework for evaluating any identity system by its authority structure. An identity system that presents itself as SSI while retaining institutional authority over portability or key rotation is, by this taxonomy's logic, a Phase 2 or Phase 3 system with different branding. Allen's 2024 critique applies exactly this diagnostic to did:web and government-centralized wallets.

**Portability as the practical test.** Principle 6 (Portability) is where self-sovereignty meets reality: if a user cannot move their identity from one provider to another without prohibitive friction, control is nominal. The portability principle implies that any identity architecture requiring ongoing institutional involvement for key management or rotation violates self-sovereignty even if it uses decentralized terminology.

**Minimalization's honest admission.** Principle 9 acknowledges that non-correlatibility — the ability to present minimum data without revealing identity across contexts — "is still a very hard (perhaps impossible) task." This admission marks which cryptographic work remained to be done in 2016 and would drive development of BBS+ signatures and selective disclosure credentials in subsequent years.

**Protection as priority rule.** Principle 10 establishes that when individual rights conflict with network needs, individual rights prevail. This is the most explicitly political principle and the one most directly connected to the human rights framing Allen anchors to ID2020 and refugee identity crises.

## Key Quotes

> "Rather than just advocating that users be at the center of the identity process, self-sovereign identity requires that users be the rulers of their own identity."

> "Users must have an independent existence. Any self-sovereign identity must exist in the world — independent of any registrars, identity providers, and certificate authorities." [Principle 1, Existence]

> "Users must control their identities. Users are the ultimate authorities over their identity, able to refer to it, update it, or hide it. Users can make claims, but others may make claims about users too." [Principle 2, Control]

> "Information and services about identity must be transportable. Identities must not be held by a singular third-party entity, even if it's a trusted one. The problem is that entities can disappear — and on the Internet, most eventually do." [Principle 6, Portability]

> "Minimalization of Disclosure of claims must be minimized. When data is disclosed, that disclosure should involve the minimum amount of data necessary to accomplish the task at hand... unfortunately, non-correlatibility is still a very hard (perhaps impossible) task." [Principle 9, Minimalization]

> "The rights of users must be protected. When there is a conflict between the needs of the identity network and the rights of individual users, then the network should err on the side of preserving the freedoms and rights of the individuals over the needs of the network." [Principle 10, Protection]

## Influence

The article named the self-sovereign identity field and established the vocabulary used in subsequent technical and policy discourse. Semantic Scholar records 269 citations as of early 2026, with 46 classed as highly influential. The W3C Decentralized Identifiers specification and Verifiable Credentials 2.0 (W3C Recommendation, May 2025) engage with Allen's principles as reference points. The article has been cited in policy discussions with legislators in Taiwan, the Netherlands, and Wyoming.

The [[European Digital Identity Wallet]] (eIDAS 2.0, 2024) is the largest real-world test of the principles against government-scale implementation. Academic consensus: EUDIW is "State-Supported Identity," not SSI — it violates Control (state-recognized wallets only), Portability (EU-scoped), and the Existence/claims distinction (legal requirements make separating identity from claims impossible). A 2024 Frontiers in Blockchain study found no SSI framework achieved full compliance with all ten principles across nine evaluated implementations.

Allen revisits the principles in [[Allen (2023) Origins of Self-Sovereign Identity]] and challenges ecosystem compliance in [[Allen (2024) Has our SSI Ecosystem Become Morally Bankrupt]]. As of March 2026, Allen is preparing revised principles for publication on April 26, 2026 — the ten-year anniversary — under the #RevisitingSSI initiative.

## Limitations and Critiques

**Principles without compliance thresholds.** The ten principles are stated as design criteria without specifying what satisfies them. How much portability satisfies Portability? Does a 30-day export delay violate Control? The generality that makes the principles broadly applicable also limits their usefulness as implementation guides. Allen explicitly notes "there's no consensus" on what self-sovereign identity precisely means, positioning the article as initiating dialogue rather than settling it.

**Governance left implicit.** The article specifies what identity systems should do for individuals but says almost nothing about how the identity ecosystem itself should be governed — who adjudicates disputes, which law applies across jurisdictions, what obligations the ecosystem imposes on its participants. The human rights framing Allen anchors to ID2020 actually sharpens this gap: stateless persons need identity precisely because normal governance structures do not protect them.

**Business model problem unaddressed.** The article does not address how self-sovereign identity infrastructure sustains itself economically. Phase 2 and Phase 3 systems Allen criticizes for centralizing identity also had business models that funded their infrastructure. Self-sovereign identity's decentralization creates a commons problem — infrastructure everyone needs, that no single entity controls, with no obvious funding mechanism. This would become a significant obstacle to adoption.

**Technical non-achievability acknowledged but unresolved.** Allen's admission that non-correlatibility — a core requirement of Minimalization — is "still a very hard (perhaps impossible) task" signals that at least one of the ten principles could not be satisfied with then-available cryptography. The article presents the principles as a system without distinguishing which are technically achievable in 2016 and which are aspirational targets requiring future cryptographic work.

## Sources

- Primary: Allen, Christopher. "The Path to Self-Sovereign Identity." Life with Alacrity, April 26, 2016. <https://www.lifewithalacrity.com/article/the-path-to-self-soverereign-identity/>
- Also archived at: <https://www.lifewithalacrity.com/2016/04/the-path-to-self-soverereign-identity.html>
- Companion analysis and insights: [[analysis]], [[insights]] (this compound node)

## Relations

- relates_to::[[Allen (2023) Origins of Self-Sovereign Identity]]
  - 2023 article clarifies the philosophical and historical influences behind the 2016 principles

- relates_to::[[Allen (2024) Has our SSI Ecosystem Become Morally Bankrupt]]
  - 2024 article argues the SSI ecosystem violated the 2016 principles in pursuit of adoption

- extracted_to::[[Authority Flows from the Person]]
  - Principle 1 (Existence) and Principle 2 (Control) ground this garden principle

- extracted_to::[[Principal Authority as Agency Law for Digital Identity]]
  - The "ruler" framing is the SSI antecedent to agency law application in digital identity

- relates_to::[[Human Authority Over Augmentation Systems]]
  - Principle 10 (Protection) applies the same priority structure to knowledge work in the DCA

- relates_to::[[European Digital Identity Wallet]]
  - EUDIW architecture is a primary test case for whether the ten principles can be honored in government implementations

- relates_to::[[Allen (2021) Principal Authority]]
  - Principal Authority provides the legal foundation for the 10 SSI principles — grounding aspirational design criteria in agency law duties

- relates_to::[[Allen (2021) Self-Sovereign Identity 5 Years On]]
  - The 2021 retrospective evaluates five years of field progress against the 2016 principles, naming the LESS vs Trust Minimized split

- relates_to::[[Allen (2022) Progressive Trust]]
  - Progressive trust is the trust-building model compatible with the self-sovereign framework; it operationalizes individual control over disclosure

- relates_to::[[Allen (2023) Data Minimization and Selective Disclosure]]
  - Data minimization and selective disclosure are the technical enforcement for Principle 9 (Minimalization) — the hardest-to-achieve of the ten principles

- relates_to::[[Allen (2023) Echoes from History]]
  - Carmille's minimalization approach provides historical grounding for why Principle 9 (Minimalization) is non-negotiable in identity systems

- relates_to::[[Allen (2023) Echoes from History II]]
  - The ten principles provide the evaluation framework for the eIDAS critique; this article argues eIDAS violates Control, Persistence, Minimalization, and Protection

- relates_to::[[Allen (2024) Building Trust in Gradients]]
  - Building trust in gradients operationalizes Principle 9 (Minimalization) within the self-sovereign framework — the user controls their own trust progression

- relates_to::[[Allen (2024) Edge Identifiers and Cliques]]
  - Edge identifiers restore the relational, social core of self-sovereign identity that the Single Signature Paradigm displaced

- relates_to::[[Allen (2025) Fair Witnessing in a Decentralized World]]
  - Fair witnessing fills the gap the original SSI principles left open — making claims credible without central authority, using context-dependent trust

- relates_to::[[Allen (2025) Five Anchors for Swiss eID]]
  - The five anchors operationalize the SSI principles for governmental systems; LESS identity bridges governmental and self-sovereign approaches

- relates_to::[[Allen (2025) How My Values Inform Design]]
  - The 10 SSI Principles are the primary application of the values-to-design pipeline — the principles are the values made concrete

- relates_to::[[Allen (2025) The Case for an International Right to Freedom to Transact]]
  - Identity as enabler of participation — transactional freedom completes the enabling stack the ten principles began

- relates_to::[[Allen (2025) When Technical Standards Meet Geopolitical Reality]]
  - GDC25 represents institutional inversion of the 2016 founding principles at the standards-process level

- relates_to::[[Allen (2026) Progress toward SEDI in Utah]]
  - Utah's Bill of Identity Rights independently codifies the 2016 SSI principles as law; Allen explicitly maps Section 1 to his Existence principle
