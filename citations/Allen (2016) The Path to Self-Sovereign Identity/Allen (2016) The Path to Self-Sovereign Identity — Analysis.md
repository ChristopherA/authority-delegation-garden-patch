---
created: 2026-03-22
part_of: "[[Allen (2016) The Path to Self-Sovereign Identity]]"
role: analysis
---

part_of::[[Allen (2016) The Path to Self-Sovereign Identity]]

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]

# Analysis: The Path to Self-Sovereign Identity

## Core Thesis

Allen's central argument is simultaneously historical and normative: digital identity has evolved through four phases, and the fourth — self-sovereign identity — is the necessary destination because the prior phases each left ultimate authority over identity records with institutions rather than the individuals those records represent.

The article's key conceptual move is the distinction between "center" and "ruler." User-centric identity, which Allen praises as an improvement over federated models, still left identity ownership with platforms and registering entities. Self-sovereign identity makes the individual not merely central to the process but the ultimate authority:

> "Rather than just advocating that users be at the center of the identity process, self-sovereign identity requires that users be the rulers of their own identity."

This framing names a specific failure mode in prior approaches. User-centric identity gave users a voice while preserving institutional control. Self-sovereign identity aims to remove that residual institutional ownership. The tension between naming this ideal and specifying how to achieve it runs through the entire piece — and would remain unresolved for years.

## Theoretical Framework: Four Phases of Digital Identity

Allen structures the history of digital identity as progressive failure followed by necessary correction. Each phase addressed the failures of the prior phase but introduced its own failure mode.

**Phase 1: Centralized Identity (1988–1998).** Organizations like IANA (1988) and ICANN (1998) controlled DNS-based identity; certificate authorities validated trust. Allen characterizes this as producing "balkanization" — users managing dozens of site-specific identities they did not own. The failure mode: identity ownership resided entirely with registering entities.

**Phase 2: Federated Identity (1999–2001).** Microsoft Passport (1999) and Liberty Alliance (2001) attempted to solve the proliferation problem by consolidating identity across services. They merely redistributed centralized power to fewer, larger institutions — "oligarchies" in Allen's framing. The failure mode: redistribution without resolution. Centralization moved up a level.

**Phase 3: User-Centric Identity (2000–2005+).** The Augmented Social Network (2000) and Internet Identity Workshop (2005–present) advanced "user consent" as the organizing principle. Technologies like OpenID, OAuth, and FIDO gave users more control over data flows. Allen credits this phase with establishing that identity should be user-controlled, but notes that "ultimate ownership remained with the registering entities." The failure mode: user-centric meant user-consulted, not user-sovereign.

**Phase 4: Self-Sovereign Identity (2012+).** Allen traces this phase to emerging decentralized identity work beginning around 2012, seeking to eliminate residual institutional ownership by grounding identity in user-controlled cryptographic material. The defining characteristic: users "maintain autonomous control" across any number of authorities.

This taxonomy is the article's most durable analytical contribution. It provides vocabulary for distinguishing identity architectures by authority structure rather than technical implementation. The phases are analytically useful but should not be read as strict chronology — OpenID (Phase 3) launched in 2005 but continued evolving well past 2012, and the "self-sovereign" phase would not produce production implementations for years after 2016.

## The Principles as a System

The ten principles are the article's most cited contribution. They function as design criteria: a self-sovereign identity system satisfies all ten, and a system that violates any is not truly self-sovereign. Read as a system rather than a list, they organize around three clusters.

**Identity existence and persistence (Principles 1, 5): Existence and Persistence.** Existence establishes that the individual has an identity prior to any digital representation — grounded in the "ineffable 'I'" rather than state-issued credentials. Persistence requires that identity endure as long as the user wants it to, separate from any particular claim set. Together these assert that identity is not created by institutions; institutions at most record and attest aspects of identities that already exist.

**User authority (Principles 2, 8, 9, 10): Control, Consent, Minimalization, Protection.** Control gives users ultimate authority to update, reveal, or hide their identity. Consent requires deliberate agreement to identity use. Minimalization limits disclosure to what is necessary. Protection requires that when user rights conflict with network needs, user rights prevail. These four together define what it means to be a "ruler" rather than a "center."

**Technical openness and freedom (Principles 3, 4, 6, 7): Access, Transparency, Portability, Interoperability.** Access requires that users can retrieve all their data without hidden gatekeeping. Transparency requires open-source algorithms. Portability prevents identity capture by any single entity. Interoperability extends the system globally without sacrificing control. These four are infrastructure-level requirements that make the user-authority principles functional in practice: without portability, "control" is nominal. The user controls nothing they cannot move.

This clustering reveals a design logic. Existence and Persistence establish what kind of thing identity is. User Authority principles specify the user's relationship to it. Technical Openness principles specify the infrastructure that relationship requires.

**Tensions within the system:** The principles create productive tensions the article acknowledges but does not resolve. Persistence ("identities should be long-lived") sits in tension with Protection ("users must be able to protect themselves"), because protection sometimes requires abandoning an identity. Allen acknowledges this indirectly by noting users "should retain the ability to dispose of identities," but the tension between long-lived identity and exit rights receives no resolution.

Interoperability sits in tension with Minimalization because global interoperability typically requires richer, more widely-shared attribute sets. Building an identity that works everywhere creates a single attribute profile that could be correlated everywhere. Allen acknowledges this directly: "non-correlatibility is still a very hard (perhaps impossible) task" — a striking admission that one of his core principles may be technically unachievable with current cryptography.

## Principle-Level Analysis

**Existence.** The philosophical anchor. Grounding identity in the "ineffable 'I'" rather than any institutional record asserts that registrars do not create identity; they attest to it. The principle has notable parallels to Locke's theory of personal identity, though Allen does not cite these sources directly. Its operational import: systems that treat identity as created-by-registration have fundamentally misunderstood what they are doing.

**Control.** The operational core. "Users are ultimate authorities" who can refer to, update, or hide their identities. The strength: it names the failure mode of all prior phases — institutional authority over the record. The gap: "control" is ambiguous between control over the identity record (what claims it contains) and control over the credential (who gets to verify it). Real systems must handle both, but the principle does not distinguish them.

**Access.** Consequential and often overlooked: users can retrieve all claims and data associated with their identity with no hidden data or gatekeepers. This is transparency-toward-the-subject, not merely transparency-toward-outsiders. Many identity systems satisfy the latter while failing the former. Allen correctly distinguishes access from the ability to modify claims others have made about you.

**Transparency.** Open-source requirements for identity system algorithms. Enforcement is non-trivial: an open-source algorithm can still be deployed in a closed-source environment with opaque data flows. The principle points in the right direction but does not specify what transparency requires at the governance level.

**Persistence.** Allen immediately qualifies the "ideally lasting forever" statement: "this goal may not be entirely reasonable" given the need for identity evolution. The qualification is honest but weakens the principle's constraining force.

**Portability.** One of the clearest principles: identity should not be held by singular entities, because entities can disappear. This has an implicit corollary: any SSI method that effectively requires an institution to maintain the identity — because revocation or rotation cannot occur without that institution — violates portability even if it superficially resembles a decentralized system.

**Interoperability.** Correct as aspiration but creates a design challenge: most identity systems achieve interoperability by standardizing attribute sets, which enables correlation. Allen acknowledges the tension with minimalization but defers resolution.

**Consent.** Users must agree to identity use, with consent being "deliberate and well-understood" even if not always interactive. The parenthetical acknowledgment that consent "might not be interactive" is significant: automated or delegated consent flows (OAuth silent refresh, for example) can satisfy the letter of consent while violating its spirit. Allen does not specify how to distinguish genuine from performative consent — a gap that would become visible as SSI systems encountered enterprise and government deployments.

**Minimalization.** Data disclosure should involve "minimum necessary information," supported by selective disclosure and zero-knowledge proofs. Allen's admission that non-correlatibility may be "perhaps impossible" is technically honest. This principle would later drive significant cryptographic work on range proofs, selective disclosure credentials, and BBS+ signatures, none of which existed in deployable form in 2016.

**Protection.** When individual rights conflict with network needs, individual rights prevail. The principle is explicitly political: identity systems should be "censorship-resistant" and "force-resilient." Protection is stated as a priority rule rather than an absolute prohibition — the network can have legitimate needs, they just cannot override individual rights. The principle does not specify how to adjudicate conflicts in practice.

## Critical Assessment

**What the article accomplishes:** Allen successfully names and defines a category that prior discourse had been approaching without crystallizing. The four-phase taxonomy and the ten principles gave the SSI community a shared vocabulary at a strategic moment. The article appeared immediately before the Rebooting Web of Trust 2 workshop and the ID2020 Summit at the United Nations — placing it where a new field's foundational text would have maximum institutional impact. The principles are general enough to apply across different technical implementations while specific enough to exclude clear failures. A centralized identity system with SSO cannot satisfy Portability or Control as stated.

**Under-specification:** The principles are stated as design criteria but without compliance thresholds. How much control satisfies Control? Does a system that allows portable export but requires 30 days notice satisfy Portability? The generality that makes the principles broadly applicable also limits their usefulness as implementation guides. Practitioners would need to translate principles into concrete technical and governance requirements — work the Rebooting Web of Trust community would undertake in subsequent workshops.

**The governance gap:** The article addresses what identity should do for individuals but says almost nothing about governance of the identity ecosystem itself. Interoperability across jurisdictions raises immediate questions: which courts adjudicate disputes? What happens when sovereign authorities require disclosure? Who decides when "network needs" are legitimate enough to override individual rights? The human rights framing Allen invokes — ID2020, refugee crises — actually makes this governance gap more visible: stateless persons need identity precisely because normal governance structures do not protect them.

**The business model gap:** The article does not address how self-sovereign identity infrastructure sustains itself economically. Identity infrastructure requires ongoing maintenance. The Phase 2 and 3 systems Allen criticizes for centralizing identity also had business models that funded their infrastructure. Self-sovereign identity's decentralization creates a commons problem: infrastructure everyone needs, that no single entity controls, with no obvious funding mechanism. This would become a significant practical obstacle to adoption.

**The accountability gap:** The principle of Control gives users authority to "update or hide" claims about themselves. But others also make claims about users — a point Allen acknowledges for the Access principle. The system as specified gives users control over their own self-assertions but does not fully specify how third-party attestations (employer records, government credentials, financial history) are governed within the SSI model.

## Significance

The article's influence within the self-sovereign identity domain is substantial. It named the field, provided its vocabulary, and defined criteria against which subsequent SSI proposals would be measured. The W3C Decentralized Identifiers specification and the Verifiable Credentials specification both engaged with Allen's principles as reference points — either to claim compliance or to defend departures from them.

The publication moment was deliberate. Placing the article at RWOT2/ID2020 Summit at the United Nations linked the SSI concept to a specific institutional agenda: providing digital identity to the roughly 1.1 billion people worldwide who lack official documentation. This framing positioned SSI as human rights technology, not merely privacy-enhancement technology, shaping subsequent policy discussions — including debates about the European Digital Identity Wallet beginning in 2021.

Allen revisited the principles multiple times in subsequent years. His 2023 article on the origins of SSI clarified the philosophical influences he had brought to the 2016 piece. His 2024 critique of the SSI ecosystem argued that implementations had diverged from the principles' intent in ways that compromised their original purpose — particularly in accepting centralized "did:web" approaches and failing to enforce strict data minimization. Together, these three articles constitute a sustained argument about what SSI should be and what it has become.

## The Glossary as Definitional Map

Allen appends a five-term glossary (Authority, Claim, Credential, Identifier, Identity) that reveals his conceptual framing at a definitional level. Two choices are analytically significant.

**Authority redefined toward decentralization.** Allen defines Authority as "a trusted entity that is able to verify and authenticate identities" — but then explicitly projects this forward: "hopefully just an open and transparent algorithm run in a decentralized manner." The definition encodes his normative goal while acknowledging that 2016's authorities were still centralized. The SSI principles aim to dissolve this entity into an algorithm.

**Identifier deliberately minimized.** Allen notes Identifier is "minimized in this article, to reduce complexity." This is an honest admission: identifier schemes are technically complex and contested, and the principles paper did not have enough space to address them adequately. The omission points to a significant gap the Rebooting Web of Trust community would spend years filling — culminating in the W3C Decentralized Identifiers specification.

**"No consensus" acknowledged.** Immediately before presenting the ten principles, Allen writes: "there's no consensus on what self-sovereign identity precisely means." This is methodologically honest: the article explicitly frames itself as initiating dialogue rather than establishing doctrine. The principles are discussion-starters for RWOT2, not a fixed standard — a distinction that would matter when Allen's 2024 article argued the ecosystem had abandoned the original intent.

## Secondary Validation (2024–2026)

*Research conducted 2026-03-22. Sources: Semantic Scholar, arXiv, Springer, Frontiers in Blockchain, Electronic Markets.*

**Citation impact.** Semantic Scholar records 269 citations for the 2016 article as of early 2026, with 46 classed as highly influential. The article appears in peer-reviewed journals across Springer, Frontiers, ACM, and arXiv, and is an appendix in the O'Reilly SSI book (Preukschat and Reed, 2021). Allen's principles have been cited in policy discussions with legislators in Taiwan, the Netherlands, and Wyoming.

**European Digital Identity Wallet (EUDIW) — eIDAS 2.0.** The EUDIW, which became regulation in the EU in 2024, is the most significant real-world test of the ten principles against government-scale implementation. Academic classification is consistent: EUDIW is "State-Supported Identity," not self-sovereign identity. A 2025 arXiv paper (arXiv:2601.19893) states directly: "the current eIDAS 2.0 and its implementation acts diverge from SSI principles, rendering the European Digital Identity Wallet (EUDIW) centralized and merely user-centric, prioritizing security and legal protection over true self-sovereignty."

Specific principle violations in EUDIW:

- **Control (Principle 2) compromised**: Users cannot freely choose their wallet provider — only state-recognized wallets are permitted. The EU Member State remains the trust anchor for high-assurance credentials, not the user.
- **Portability (Principle 6) limited**: Portability is constrained to EU member states; the principle requires global portability.
- **Existence (Principle 1) structurally undermined**: A 2025 study notes that in the public sector, "users have an obligation to provide identity attributes to relying parties, and legal constraints make a firm separation between an identity and its claims impossible."

The 2025 arXiv paper proposes retrofitting SSI compliance into EUDIW using zero-knowledge proofs and trusted execution environments — acknowledging the gap while attempting to bridge it technically.

**No framework achieves full compliance.** A 2024 Frontiers in Blockchain study evaluated nine SSI frameworks (Sovrin, uPort, Jolocom, ShoCard, Litentry, Civic, KILT, Idena, ION) against Allen's ten principles, organized into three categories: Security (Protection, Persistence, Minimization), Controllability (Existence, Control, Consent), and Portability (Access, Transparency, Portability, Interoperability). Compliance was measured on a scale from 0.0 (Non-compliant) to 1.0 (Full). Result: no framework achieved full compliance (1.0) with all ten principles.

**GDPR tension.** A 2024 arXiv study (arXiv:2409.03624) identifies fundamental conflicts between SSI as typically implemented on blockchains and GDPR: blockchain immutability conflicts with GDPR's right to erasure; active network participants can process data without consent, contradicting data subject rights. This creates a regulatory constraint that most European SSI implementations cannot fully resolve.

**#RevisitingSSI initiative.** Allen is publishing revised principles on April 26, 2026 — the ten-year anniversary of the original article — as part of a "#RevisitingSSI" initiative. This signals Allen's own assessment that the original principles require refinement in light of technological development, institutional capture, and the geopolitical landscape of 2026. The revised principles have not yet been published at the time of this analysis (2026-03-22).

**Funding misalignment.** Blockchain Commons has noted that available funding has favored "Legally-Enabled Self-Sovereign (LESS) Identity" for business and government use over "Trust Minimized Identity" designed to protect vulnerable populations — reflecting institutional drift from the human rights framing Allen embedded in the 2016 article.

**Standards adoption is necessary but not sufficient.** W3C Verifiable Credentials 2.0 became a Recommendation in May 2025; W3C Decentralized Identifiers reached Candidate Recommendation. Allen's own assessment: "DIDs and VCs may be foundational architectural requirements for self-sovereign identity principles, but they are not themselves sufficient; additional privacy and human rights protections using cryptographic technologies are needed." The standards codify infrastructure; they do not enforce the principles.

**Conformity assessment gap.** A 2024 paper by Doege, Bochnia, and Anke (presented at OID2024) demonstrates that "SSI Principles are not fully met by current products," documenting a "trade-off between the ideal SSI world versus real-world implementation." Research from 2024–2025 indicates "very few productive SSI applications exist" in public sector deployment, and practitioners "lack insights into the process of successfully innovating with SSI in the public sector."

**Summary of 2024–2026 reception.** The ten principles are widely cited as a normative standard but widely violated in production deployments. The gap between theoretical compliance and implementation reality is substantial and documented across multiple independent studies. EUDIW represents the most significant institutional deployment in the principles' name, and it falls short on Control, Portability, and the Existence/claims distinction. Standards adoption (W3C DID, VCs) is real but insufficient. Allen's own response — #RevisitingSSI — acknowledges that the original principles, while directionally correct, require updating for the current environment.
