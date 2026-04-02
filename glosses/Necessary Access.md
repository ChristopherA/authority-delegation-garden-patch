---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Allen's Necessary Access (2023): the inside-out of least access. The system declares its data needs upfront so the holder has complete information for consent. Transforms the interaction from unilateral extraction to bilateral negotiation."
tagline: "Allen's inversion of least access — declare data needs upfront for bilateral consent, not unilateral extraction"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

# Necessary Access

Necessary access is Allen's inside-out of the Principle of Least Access (2023). Where least access asks "what data exposure should we minimize?", necessary access asks "what data does the system actually need — and how do we make that need visible to the person whose data it is?"

## From Minimization to Negotiation

Least access is a minimization strategy: reduce data exposure to the minimum required. Necessary access is a negotiation strategy: the system declares its data requirements upfront, and the holder decides whether to grant them. The shift is from unilateral extraction (the verifier requests whatever it wants, the holder tries to limit disclosure) to bilateral negotiation (the system states what it needs, the holder evaluates the request with complete information).

This changes the consent dynamic. Under least access, consent is a gate — "do you allow this request?" Under necessary access, consent is informed — "the system needs these specific data elements for these specific purposes; here is what it does not need." The holder has enough information to make a real decision rather than performing consent theater.

## Credential System Application

In verifiable credential systems, necessary access means a verifier declares exactly which claims it needs and why. An age-verification system needs "over 21" — not date of birth, not name, not address. The declaration is part of the protocol, not a side channel. The holder sees the request, evaluates it against their own interests, and responds. If the verifier requests more than necessary, the request itself reveals the overreach.

This is the constructive counterpart to least access's restrictive analysis. Least access audits what data flows are excessive. Necessary access designs the interaction so that data needs are transparent from the start. The two together produce systems where data flows are both minimal and comprehensible to the people whose data is flowing.

## Position in the Taxonomy

Necessary access completes the enabling row of Allen's 2x3 taxonomy, paired with [Principle of Least Access](Principle%20of%20Least%20Access.html) in the restrictive row. Together they define the access corridor for data-handling systems: no more data than needed (least access), no less transparency about needs than required for informed consent (necessary access).

## Sources

- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - The source article introducing necessary access as the sixth pattern in the taxonomy
- relates_to::[Principle of Least Access](Principle%20of%20Least%20Access.html)
  - The restrictive counterpart that necessary access inverts
- relates_to::[Necessary Privilege](Necessary%20Privilege.html)
  - The privilege-scope sibling in the enabling row
- relates_to::[Necessary Authority](Necessary%20Authority.html)
  - The authority-scope sibling in the enabling row
- relates_to::[Allen (2024) Progressive Trust](../citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html)
  - Progressive trust is the interaction model for implementing necessary access — trust and disclosure increase incrementally
- relates_to::[[Allen (2023) Origins of Self-Sovereign Identity]]↑
  - Self-sovereign identity provides the dignity framing that motivates bilateral negotiation over extraction
- relates_to::[Allen (2021) Principal Authority](../citations/Allen%20(2021)%20Principal%20Authority/Allen%20(2021)%20Principal%20Authority.html)
  - Principal authority defines who decides about data; necessary access defines how data needs are communicated for that decision
