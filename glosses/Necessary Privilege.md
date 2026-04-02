---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Allen's Necessary Privilege (2023): the inside-out of least privilege. Instead of asking what to deny, asks what the user actually needs to do their work. Everything else excluded by default. Shifts the designer's attention from enumerating abuses to enabling legitimate function."
tagline: "Allen's inversion — what does the user actually need? Everything else excluded by default"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Deep Context Architecture](../domains/Deep%20Context%20Architecture.html)
- in_precinct::[[Garden Precinct]]↑

# Necessary Privilege

Necessary privilege is Allen's inside-out of the Principle of Least Privilege (2023). Where least privilege asks "what privileges should we deny?", necessary privilege asks "what privileges does the user actually need to do their work?" The answer to both questions should converge on the same permission set — but the design process that gets there is different, and the difference produces different systems.

## The Inversion

Least privilege starts with all possible permissions and removes what is unnecessary. Necessary privilege starts with nothing and adds what is required. The restrictive framing forces designers to enumerate every possible abuse — a potentially endless task. The necessary framing concentrates attention on the positive: what does this user need to accomplish, and what is the minimum privilege set that enables it?

Allen's insight is that framing changes what designers discover. A least-privilege analysis tends to produce permission sets that are technically minimal but functionally brittle — users bump against barriers, work around restrictions, and accumulate frustration. A necessary-privilege analysis starts from work requirements, producing permission sets that enable smooth operation. If a user proactively has access to everything they need, they never bump up against barriers. This reduces human error and increases satisfaction.

## Not Just Restatement

Necessary privilege is not simply least privilege stated differently. The two framings lead to different design conversations. Least privilege asks: "Is this permission necessary?" — a yes/no gate applied permission by permission. Necessary privilege asks: "What does this role require?" — a constructive enumeration that may surface permissions the least-privilege analysis would never have considered, because they were not in the initial permission set being trimmed.

## Position in the Taxonomy

Necessary privilege occupies the enabling row of Allen's 2x3 taxonomy, paired with [Principle of Least Privilege](Principle%20of%20Least%20Privilege.html) in the restrictive row. Together they bracket the privilege scope — one sets the ceiling (no more than necessary), the other sets the floor (no less than necessary). A well-designed system satisfies both simultaneously.

## Sources

- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - The source article introducing the inside-out methodology and all six patterns
- relates_to::[Principle of Least Privilege](Principle%20of%20Least%20Privilege.html)
  - The restrictive counterpart that necessary privilege inverts
- relates_to::[Necessary Authority](Necessary%20Authority.html)
  - The authority-scope sibling in the enabling row
- relates_to::[Necessary Access](Necessary%20Access.html)
  - The access-scope sibling in the enabling row
- relates_to::[Saltzer & Schroeder (1975) The Protection of Information in Computer Systems](../citations/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems.html)
  - Saltzer and Schroeder defined the original restrictive pattern that Allen inverts
- relates_to::[Delegated Decision Authority Spectrum](../boundaries/Delegated%20Decision%20Authority%20Spectrum.html)
  - Authority zones are a practical application of the ceiling/floor bracket
