---
created: 2026-03-22
part_of: "[[Allen (2016) The Path to Self-Sovereign Identity]]"
role: insights
---

part_of::[[Allen (2016) The Path to Self-Sovereign Identity]]

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]

# Insights: The Path to Self-Sovereign Identity

Extracted takeaways from the 2016 Allen article for the garden's knowledge domains, with connections to existing nodes.

## Authority Origins

Allen's Principle 1 (Existence) and Principle 2 (Control) together establish the foundational claim that authority over identity originates with the person, not with any institution that registers or attests to that identity. Registrars are witnesses, not creators.

This maps directly to [[Authority Flows from the Person]] in the principles domain. Allen's article is the source from which that principle was extracted for vault architecture use. The citation grounding this principle's claim — "users are ultimate authorities over their identity, able to refer to it, update it, or hide it" — belongs here, not in the principle node itself.

## Delegation Without Transfer

The "ruler vs center" distinction Allen draws has a precise legal analog: the principal-agent relationship. Being at the "center" of an identity process describes a user-centric system where institutions process identity on behalf of users. Being the "ruler" describes a principal-agent system where users confer authority to institutions, which then act within those boundaries.

This connects directly to [[Principal Authority as Agency Law for Digital Identity]]. The gloss applies Allen's "ruler" framing to the legal structure of agency law — the principal directs, agents act within conferred scope, and authority cannot be alienated (only delegated). Allen does not use the agency law vocabulary in 2016, but the structural identity between his "ruler" concept and the principal-agent relationship is close.

## Portability as Escape Condition

Allen's Principle 6 (Portability) establishes a design requirement that has broader implications: any system that makes exit prohibitively costly violates portability even if exit is nominally possible. This is the same diagnostic test [[Principal Authority as Agency Law for Digital Identity]] identifies as "revocability as litmus test." If a user cannot practically revoke delegation to an identity provider — because their identity cannot be moved elsewhere — the relationship is coerced, not genuinely sovereign.

The convergence between Allen's portability principle and the revocability test suggests these are different expressions of the same underlying constraint: genuine authority requires genuine exit.

## Consent Theater Predicted

Allen's Principle 8 (Consent) requires that consent be "deliberate and well-understood" even when not interactive. His parenthetical acknowledgment that consent "might not be interactive" opens a gap that [[Principal Authority as Agency Law for Digital Identity]] later names "consent theater" — performative consent (clicking "I agree") without the comprehension that makes consent genuine. Allen identified the risk in 2016 but did not name it or develop the analysis. The later work extended this insight.

## The Impossible Principle Problem

Allen's admission in Principle 9 (Minimalization) — that non-correlatibility is "a very hard (perhaps impossible) task" — is methodologically significant for the garden. The principles present a normative ideal but Allen signals that at least one principle may not be technically achievable with then-current cryptography.

This creates a standing open question for [[Self-Sovereign Identity]] domain work: which of the ten principles have become achievable since 2016? BBS+ signatures and selective disclosure credentials advanced the state of the art on minimalization. Zero-knowledge proofs have matured. A gap assessment between the 2016 principles and 2024 implementation capabilities would be worth producing — see open inquiry ghost link below.

## Phase Taxonomy as Diagnostic Tool

The four-phase taxonomy (Centralized → Federated → User-Centric → Self-Sovereign) is not merely historical description. It is a diagnostic taxonomy for evaluating any identity system by its authority structure. A system that presents itself as "SSI" but retains institutional authority over portability or rotation is, by the taxonomy's logic, Phase 3 or Phase 2 technology with different branding.

Allen's 2024 moral bankruptcy critique applies exactly this diagnostic: did:web and centralized government approaches are Phase 2/3 systems being marketed as Phase 4. The taxonomy provides the diagnostic, the 2024 article applies it.

## Governance as Ghost Link

The article's most significant omission — the governance gap — creates a ghost link to work that needs doing. Allen specifies what identity systems should do for individuals but not how the identity ecosystem governing them should itself be governed. This is not a criticism of the 2016 article, which was establishing principles, not governance architecture. But it is a gap that remains largely unfilled in the SSI literature and points toward [[Self-Sovereign Identity Governance]] as a needed garden node.

## Human Authority Extended

Allen's Principle 10 (Protection) — individual rights prevail when they conflict with network needs — maps structurally onto [[Human Authority Over Augmentation Systems]]. The DCA principle applies the same priority rule to knowledge work: when AI augmentation creates tension with human authority over knowledge products, human authority prevails. The conceptual structure is identical; the domain of application differs.

This suggests the SSI principles, particularly Protection, informed the vault's own design logic for human-AI authority relationships, not just digital identity systems.

## Dialogue, Not Doctrine

Allen's explicit prefatory admission — "there's no consensus on what self-sovereign identity precisely means" — positions the article as an invitation rather than a declaration. Combined with his dedication of the piece to RWOT2 and the ID2020 Summit, the principles were designed to be debated and refined by the community he was assembling, not accepted as fixed. This framing matters for how Allen's 2024 critique is read: when he says the ecosystem "abandoned the principles," the principles themselves were always intended to evolve through community dialogue. The 2024 critique can be read as an argument that the evolution went in the wrong direction, not that it was wrong to evolve.

This creates a garden extraction opportunity: [[Framework as Departure Point]] — the methodological practice of stating principles explicitly as "starting dialogue" rather than "settling it," inviting refinement while providing conceptual anchors.

## Connections Summary

| Insight | Existing Garden Node | Relationship |
|---------|---------------------|--------------|
| Existence + Control → authority from person | [[Authority Flows from the Person]] | Source citation |
| "Ruler" framing → principal-agent | [[Principal Authority as Agency Law for Digital Identity]] | Conceptual antecedent |
| Portability → revocability test | [[Principal Authority as Agency Law for Digital Identity]] | Convergent reasoning |
| Consent gap → consent theater | [[Principal Authority as Agency Law for Digital Identity]] | Extended by |
| Protection → human authority prevails | [[Human Authority Over Augmentation Systems]] | Structural parallel |
| Four-phase taxonomy | [[Self-Sovereign Identity]] domain | Diagnostic vocabulary |
| "No consensus" → dialogue not doctrine | [[Framework as Departure Point]] | Garden pattern candidate |

## Open Questions (Ghost Links)

- [[Ten Principles Gap Assessment 2024]] — which principles are now achievable that weren't in 2016?
- [[Self-Sovereign Identity Governance]] — what governance architecture would fulfill the principles' implicit requirements?
- [[Consent Theater in SSI Deployments]] — how prevalent is performative consent in actual SSI systems?
- [[Framework as Departure Point]] — a garden pattern for principle-stating that explicitly invites refinement rather than prescribes fixed doctrine
