---
created: 2026-03-31
author: Christopher Allen
brief_summary: "Inquiry into whether the estate's authorization-escalation model needs an explicit trust-evolution mechanism, or whether escalation tiers already cover the same ground as Victoria Gracia's autonomia concept. Explores how Christopher Allen's Progressive Trust framework applies to agent-principal delegation within the estate."
tagline: "Does agent delegation need a trust-evolution mechanism, or do escalation tiers already cover it?"
---

- is_a::[[Inquiry Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Garden Precinct]]

# Progressive Trust as Agent Delegation Model

## Research Question

Does the estate's agent delegation model need an explicit trust-evolution mechanism — a way for agent autonomy to expand as trust develops through successful delegation? Or does the existing authorization-escalation model (blast-radius tiers with explicit gates) already cover this ground?

Victoria Gracia's [[Gracia (2026) Uni-Versum Personal Knowledge Architecture|Uni-Versum]] introduces **autonomia**: a dynamic trust contract between the human principal (nos) and each agent that evolves over time. Some tasks are fully delegated; others require human judgment at each step. The boundary shifts as trust develops through successful delegation.

The estate currently uses authorization-escalation tiers (local reversible, local persistent, shared visible, irreversible) to govern what agents can do. This is an operational framework — blast radius determines gate strength. Autonomia describes a relational mechanism — trust develops through accumulated successful interactions.

Christopher Allen's own [[Progressive Trust]] framework provides a theoretical foundation: trust builds through graduated disclosure and verification, with each successful interaction expanding the scope of future interactions. If autonomia is a specialization of Progressive Trust applied to agent systems, the connection is architecturally significant — the estate's principal has already articulated the trust model that governs agent delegation.

## Current State

**What the estate has**: Authorization-escalation tiers that are static — the same gates apply regardless of whether an agent has been reliable across 50 sessions or is running for the first time. The tiers are calibrated to blast radius, not to accumulated trust.

**What Uni-Versum has**: A named concept (autonomia) that models trust as dynamic. The concept is defined but not operationalized in Gracia's published architecture — the mechanism for trust evolution is stated as a principle, not implemented as a protocol.

**What Progressive Trust provides**: A theoretical framework where trust develops through graduated disclosure and verification. Each stage introduces a small extension of trust, observes the result, and uses it to calibrate the next extension. Applied to agents: early sessions operate under tight gates; successful completion earns expanded autonomy in future sessions.

## Open Questions

1. **Is the current static model sufficient?** The escalation tiers work. Agents don't accumulate dangerous authority because every session starts fresh. Is there a practical benefit to making delegation dynamic, or does the session-reset pattern make accumulated trust operationally irrelevant?

2. **Where would trust-evolution manifest?** If implemented, what would change? Fewer approval gates for trusted agents? Broader commission scope? Autonomous push authority after N successful merges? Each candidate has different risk profiles.

3. **How does this relate to the estate's vocabulary?** Should the estate adopt "autonomia" as a loan term (with gloss), create its own naming, or simply extend the authorization-escalation model with a dynamic dimension? The [[Vocabulary Collision Navigation]] pattern suggests translation rather than adoption — but the estate currently lacks any term for this concept.

4. **Does Progressive Trust apply to agent-principal relationships?** Progressive Trust was designed for human-to-human and human-to-system interactions. Agent-principal relationships have a structural difference: the agent has no independent motivation to betray trust, and each session starts without memory of prior trust. Does the framework transfer, or does the session-reset pattern make trust accumulation meaningless?

## Sources

- [[Gracia (2026) Uni-Versum Personal Knowledge Architecture]] — autonomia concept (Insights file, Insight 3)
- [[Progressive Trust]] — Christopher Allen's trust-building framework
- Authorization-escalation-rule — the estate's current static model
- [[Six Approaches to Persona Architecture — Synthesis]] — Axis 3 compares authority models across six approaches

## Relations

- relates_to::[[Gracia (2026) Uni-Versum Personal Knowledge Architecture]]
  - Autonomia is Gracia's concept that prompted this inquiry
- relates_to::[[Six Approaches to Persona Architecture — Synthesis]]
  - Axis 3 (Where Does Authority Live?) compares the estate's delegated authority with Uni-Versum's fidelis-est/autonomia/diploma
- relates_to::[[Human Authority Over Augmentation Systems]]
  - Any trust-evolution mechanism must preserve this principle — expanded autonomy cannot erode human authority
- relates_to::[[Knowledge Estate as Peer Commons Architecture]]
  - The delegated authority spectrum that trust-evolution would modify
- relates_to::[[Naming Carries Relational Weight]]
  - The vocabulary question: adopt "autonomia," translate it, or name a new concept
