---
created: 2026-03-31
author: Christopher Allen
brief_summary: "Inquiry into what governs collaborators' agents operating in shared spaces. When multiple sovereign estates interact through garden patches and commons, their agents may need to cross estate boundaries. Victoria Gracia's diploma concept addresses this — a trust credential for external agents — but the estate currently has no inter-estate agent governance mechanism. Explores whether diploma fills the gap or whether the publication-boundary model already handles it."
tagline: "What governs your agents in my space? — inter-estate trust for the commons"
---

- is_a::[[Inquiry Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Garden Precinct]]

# Federated Agent Governance Across Sovereign Estates

## Research Question

When collaborators bring their own agents to shared work — reading each other's published patches, contributing to commons repositories, operating on shared content — what governs those agents' behavior? The estate currently has no mechanism for inter-estate agent governance. Is one needed, and if so, does Victoria Gracia's **diploma** concept fill the gap, or does the garden patch publication model already handle inter-estate interaction without requiring agent-level trust credentials?

## Current State

**What the estate has**: The boundary guardian pattern (Chatelaine enforces cross-precinct constraints within one estate) and the publication membrane ([[Three-Layer Publication Membrane]] — secrets never leave, operations stay private, synpraxis crosses to collaborators). Interaction between estates currently flows through published content: garden patches, citations, glosses, seeds. No collaborator's agent has ever operated directly within this estate's file system.

**What Uni-Versum has**: The **diploma** concept — a trust credential that formalizes what external agents can and cannot do when operating in your system. Diploma specifies workspace access, permitted operations, and terms. The scope distinction: autonomia governs trust within one system (principal to their own agents); diploma governs trust between systems (your agents operating in my space).

**What already works**: The gift-with-invitation model. One person publishes a garden patch; others consume and respond through their own systems. Cross-referencing happens through citations and glosses, not through shared file access. Victoria's Uni-Versum vocabulary appears as glosses in the estate's garden. The estate's persona architecture appears as cited material in others' systems. No agent crosses the boundary.

**What Gordian Envelope provides**: Gordian Envelope's elision capability solves Victoria's information-hiding problem — the ability to selectively reveal or conceal parts of a structured document. This could be a mechanism for partial publication that supports graduated inter-estate trust.

## Open Questions

1. **Is agent-level governance premature?** Currently, collaboration works through publication — each estate's agents operate only within their own estate, and cross-estate interaction is mediated by published content. Does agent-level governance solve a problem that exists, or one that might exist in the future?

2. **What scenarios require inter-estate agent access?** Concrete candidates: a collaborator's agent reading your published patch to generate cross-references automatically; a shared commons repository where multiple estates' agents write; a collaborative editing session where agents from different estates modify the same document. Which of these are real needs vs hypothetical?

3. **Does the publication membrane already handle this?** If inter-estate interaction stays at the publication layer (layer 3 of the [[Three-Layer Publication Membrane]]), then no agent-level governance is needed — the membrane itself governs what crosses. Diploma becomes relevant only if agents need to operate below the publication layer.

4. **How does this connect to Ostrom's commons governance?** The [[Knowledge Estate as Peer Commons Architecture]] decision references Ostrom's principles but acknowledges they are aspirational — "no multi-estate interaction exists yet." The diploma concept is one possible mechanism for Ostrom's "clearly defined boundaries" and "monitoring" principles applied to agent access.

5. **What vocabulary should the estate use?** If inter-estate agent governance is needed, should the estate adopt "diploma" as a loan term (with gloss mapping to the estate's own trust vocabulary), or develop its own concept? The [[Vocabulary Collision Navigation]] pattern suggests translation. But "diploma" has a clear semantic field (credentials, authorization, formal trust agreement) that may not need translation.

## Sources

- [[Gracia (2026) Uni-Versum Personal Knowledge Architecture]] — diploma concept (Insights file, Insight 4)
- [[Six Approaches to Persona Architecture — Synthesis]] — Axis 4 (commons potential) frames the interoperability question
- [[Knowledge Estate as Peer Commons Architecture]] — the commons architecture that would need governance
- Ostrom, Elinor. *Governing the Commons* (1990) — commons governance principles

## Relations

- relates_to::[[Gracia (2026) Uni-Versum Personal Knowledge Architecture]]
  - Diploma is Gracia's concept that prompted this inquiry
- relates_to::[[Progressive Trust as Agent Delegation Model]]
  - Sibling inquiry: autonomia governs trust within an estate, diploma governs trust between estates. Both are integration questions about Gracia's trust vocabulary
- relates_to::[[Three-Layer Publication Membrane]]
  - The publication membrane may already solve the governance problem at the boundary layer, making agent-level governance unnecessary
- relates_to::[[Knowledge Estate as Peer Commons Architecture]]
  - The commons architecture's aspirational governance principles are the context for this inquiry
- relates_to::[[Vocabulary Collision Navigation]]
  - The vocabulary decision: adopt "diploma," translate it, or find that the estate's existing publication model makes the concept unnecessary
- relates_to::[[Six Approaches to Persona Architecture — Synthesis]]
  - The Thursday practical question: "how do we publish patches so we can cross-reference each other?" is the immediate context
