---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Miller's Principle of Least Authority (2006): scope expansion from individual privileges to transitive authority chains. Permissions form a web, not isolated grants — a user who can invoke a program that can access a resource has authority over that resource."
tagline: "Miller's expansion — privileges form a web of transitive authority, not isolated grants"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

# Principle of Least Authority

Mark Miller's Principle of Least Authority (2006) — sometimes abbreviated as the Principle of Least Authority in capability literature — expands Saltzer and Schroeder's least privilege from individual permissions to transitive authority. The shift matters: a user who can run a program that can access a resource effectively has authority over that resource, whether or not any single permission grant says so.

## The Scope Expansion

Least privilege asks: does this entity have more permissions than it needs? Least authority asks: does this entity have more authority than it needs — including authority acquired transitively through the things it can access?

The difference is not academic. Modern software systems compose. A web application that can call an API that can query a database has authority over that database's contents, even if the application's direct permissions say nothing about databases. Least privilege analysis, which examines each permission in isolation, misses this entirely. Least authority analysis follows the chains.

Miller formalized this in his Johns Hopkins dissertation on object-capability security. Capabilities — unforgeable references that combine designation with authority — make transitive authority visible and controllable. In a capability system, you can trace exactly who has authority over what, because authority flows only through explicitly granted references.

## Many Discussions Conflate the Two

Allen notes that many modern security discussions use "least privilege" and "least authority" interchangeably. They are not the same. Least privilege is a necessary but insufficient subset of least authority. A system can satisfy least privilege (every individual permission is minimal) while violating least authority (transitive chains grant excessive authority). The scope difference changes what you audit and what you find.

## Position in the Taxonomy

Least authority occupies the middle column of Allen's 2x3 taxonomy: the restrictive pattern at the authority scope. Its inside-out counterpart is [Necessary Authority](Necessary%20Authority.html), which asks what authority a user genuinely needs to accomplish their work — the floor that complements Miller's ceiling. Without both, systems either over-restrict (blocking legitimate work) or under-restrict (leaking transitive authority).

## Sources

- Miller, Mark S. "Robust Composition: Towards a Unified Approach to Access Control and Concurrency Control." PhD Dissertation, Johns Hopkins University. (2006)
- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - Allen traces the lineage from least privilege through least authority to least access
- relates_to::[Miller (2006) Robust Composition](../citations/Miller%20(2006)%20Robust%20Composition/Miller%20(2006)%20Robust%20Composition.html)
  - Miller's dissertation where the principle is formalized within object-capability security
- relates_to::[Principle of Least Privilege](Principle%20of%20Least%20Privilege.html)
  - The predecessor — least authority extends least privilege by adding transitive scope
- relates_to::[Principle of Least Access](Principle%20of%20Least%20Access.html)
  - Allen's further extension from authority over systems to exposure of data
- relates_to::[Necessary Authority](Necessary%20Authority.html)
  - The inside-out counterpart: what authority must not be withheld?
- relates_to::[Delegated Decision Authority Spectrum](../boundaries/Delegated%20Decision%20Authority%20Spectrum.html)
  - Authority zones map transitive chains to human-visible boundaries
- relates_to::[Saltzer & Schroeder (1975) The Protection of Information in Computer Systems](../citations/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems.html)
  - The 1975 paper that named least privilege, which least authority subsumes
