---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Allen's Necessary Authority (2023): the inside-out of least authority. The floor that complements Miller's ceiling. Withholding authority a user genuinely needs creates friction, workarounds, and shadow systems — without improving safety."
tagline: "Allen's inversion of Miller — withholding necessary authority creates friction without improving safety"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Deep Context Architecture](../domains/Deep%20Context%20Architecture.html)
- in_precinct::[[Garden Precinct]]↑

# Necessary Authority

Necessary authority is Allen's inside-out of Miller's Principle of Least Authority (2023). Where least authority asks "what transitive authority should we limit?", necessary authority asks "what authority does the user genuinely need to accomplish their work — including the transitive authority that flows through the tools and systems they must use?"

## The Floor That Complements Miller's Ceiling

Least authority sets a ceiling: no entity should hold more authority than required. Necessary authority sets a floor: no entity should be denied authority it legitimately needs. Without the floor, least-authority analysis produces systems that are technically minimal but operationally hostile. Users who lack necessary authority develop workarounds — sharing credentials, escalating through informal channels, accumulating ad-hoc permissions that are never revoked. The workarounds are worse than the authority they replace, because they are invisible to the security model.

This is not a failure of least authority as a principle. It is a failure to ask the complementary question. A system that satisfies least authority but violates necessary authority has not achieved security — it has achieved friction. Friction that users route around.

## Transitive Scope Matters Here Too

Miller's contribution was recognizing that authority is transitive. Necessary authority inherits this scope. A user who needs to accomplish a task that requires invoking a service that accesses a database needs authority over that entire chain — not just the first link. Denying any link in a necessary chain does not remove the need; it forces the user to find another path, often one that is less auditable and less secure.

## Position in the Taxonomy

Necessary authority occupies the middle column of Allen's enabling row, paired with [Principle of Least Authority](Principle%20of%20Least%20Authority.html) in the restrictive row. The two patterns together define the authority corridor — the range between "more than needed" (violation of least authority) and "less than needed" (violation of necessary authority). Good design lives inside that corridor.

## Sources

- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)
- Miller, Mark S. "Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control." (2006)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - The source article introducing the inside-out methodology
- relates_to::[Principle of Least Authority](Principle%20of%20Least%20Authority.html)
  - The restrictive counterpart — Miller's ceiling that necessary authority floors
- relates_to::[Miller (2006) Robust Composition](../citations/Miller%20(2006)%20Robust%20Composition/Miller%20(2006)%20Robust%20Composition.html)
  - Miller's formalization of transitive authority, which necessary authority inherits
- relates_to::[Necessary Privilege](Necessary%20Privilege.html)
  - The privilege-scope sibling in the enabling row
- relates_to::[Necessary Access](Necessary%20Access.html)
  - The access-scope sibling in the enabling row
- relates_to::[Delegated Decision Authority Spectrum](../boundaries/Delegated%20Decision%20Authority%20Spectrum.html)
  - The spectrum operationalizes the authority corridor for agent systems
- relates_to::[Principal Authority as Agency Law for Digital Identity](Principal%20Authority%20as%20Agency%20Law%20for%20Digital%20Identity.html)
  - Principal authority defines who holds authority; necessary authority defines what authority must not be withheld
