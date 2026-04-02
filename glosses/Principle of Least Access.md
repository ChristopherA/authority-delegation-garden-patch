---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Allen's Principle of Least Access (2023): extends the least privilege lineage from system permissions into data exposure. Only the minimum data access necessary to achieve a specific goal should be granted. Motivated by self-sovereign identity and verifiable credentials, where the primary threat is correlation, not unauthorized system access."
tagline: "Allen's extension into data — minimum exposure necessary, with correlation as the threat model"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

# Principle of Least Access

Allen's Principle of Least Access (2023) extends the least privilege lineage from system permissions into data. Where least privilege and least authority address what entities can do, least access addresses what entities can see. The shift is motivated by self-sovereign identity and verifiable credentials, where the primary concern is not unauthorized system access but unnecessary data exposure and the correlation opportunities it creates.

## The Data Extension

Least privilege minimizes permissions. Least authority minimizes transitive authority chains. Least access minimizes data exposure — and specifically targets the correlation surface.

In credential systems, a verifier who receives a full date of birth when they only need to confirm "over 21" has acquired unnecessary access. That extra data is not just wasted — it becomes a correlation vector. Combined with data from other interactions, it can reconstruct a profile the holder never intended to share. Least access incorporates Miller's ecosystem awareness (transitive authority thinking) but redirects it toward data flows rather than capability chains.

Allen frames this with a dignity orientation rather than asset protection. The military tradition of information security protects information as an organizational asset. Least access protects individuals "who are uniquely due respect and dignity." The threat model shifts from adversaries breaching perimeters to systems routinely extracting more data than they need.

## Architectural Coercion Resistance

Allen argues that a datastore implementing least access can refuse to grant improper data requests, creating architectural coercion resistance. If the system cannot produce data it does not hold, coercive demands are negated by design rather than by policy. This is a strong claim — coercion in practice operates through channels outside the data system (device confiscation, legal compulsion). But the architectural layer is real: what the system cannot produce, no order can extract.

## Position in the Taxonomy

Least access completes the restrictive row of Allen's 2x3 taxonomy: privilege (1975) → authority (2006) → access (2023). Its inside-out counterpart is [Necessary Access](Necessary%20Access.html), which inverts the interaction model from "limit what the verifier gets" to "declare what the system needs, so the holder can make an informed consent decision."

## Sources

- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - The source article where Allen introduces least access as the third pattern in the lineage
- relates_to::[Principle of Least Privilege](Principle%20of%20Least%20Privilege.html)
  - First in the lineage — least access extends from permissions through authority into data
- relates_to::[Principle of Least Authority](Principle%20of%20Least%20Authority.html)
  - Second in the lineage — least access adopts Miller's transitive thinking for data flows
- relates_to::[Necessary Access](Necessary%20Access.html)
  - The inside-out counterpart: declare data needs upfront for bilateral consent
- relates_to::[[Allen (2023) Origins of Self-Sovereign Identity]]↑
  - The dignity framing connects to self-sovereign identity's commitment to individual autonomy
- relates_to::[Allen (2024) Progressive Trust](../citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html)
  - Progressive trust provides the interaction model for implementing least access incrementally
- relates_to::[[Minimum Viable Architecture]]↑
  - Minimum viable architecture applies the least/necessary logic at the system level
