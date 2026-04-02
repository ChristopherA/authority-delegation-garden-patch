---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Gloss on Saltzer and Schroeder's Principle of Least Privilege (1975): every program and user should operate with the minimum set of privileges necessary to complete the job. The original in a lineage that extends through least authority and least access."
tagline: "The 1975 original — minimum permissions for the job, considered in isolation"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

# Principle of Least Privilege

Every program and every privileged user of the system should operate using the least set of privileges necessary to complete the job. Saltzer and Schroeder stated this in 1975 as one of eight design principles for protection mechanisms in computer systems. It remains the foundation of the entire least/necessary taxonomy.

## What It Covers

Least privilege considers individual permissions in isolation. A user needs read access to a file — grant read access, not read-write. A program needs to open a network socket — grant socket access, not root. The analysis is local: examine what one entity needs, grant exactly that, deny everything else.

This locality is both the principle's strength and its limitation. It produces clean, auditable permission sets. But it does not account for what happens when permissions compose — when a user who can run a program that can access a resource effectively has authority over that resource through the program. That transitive dimension is where Miller's Principle of Least Authority picks up the thread.

## Position in the Taxonomy

Least privilege is the first column of Allen's 2x3 taxonomy: the restrictive pattern at the privilege scope. Its inside-out counterpart is [Necessary Privilege](Necessary%20Privilege.html), which asks not "what should we deny?" but "what does the user actually need to do their work?" The two patterns address the same design space from opposite directions — least privilege sets ceilings, necessary privilege sets floors.

The lineage runs: Least Privilege (1975, permissions) → [Principle of Least Authority](Principle%20of%20Least%20Authority.html) (2006, transitive authority) → [Principle of Least Access](Principle%20of%20Least%20Access.html) (2023, data exposure). Each expansion widens scope without invalidating what came before.

## Sources

- Saltzer, Jerome H. and Schroeder, Michael D. "The Protection of Information in Computer Systems." (1975)
- Allen, Christopher. "Musings of a Trust Architect: Least & Necessary Design Patterns." (2023)

## Relations

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - Allen places least privilege as the first pattern in his 2x3 taxonomy and traces its lineage forward
- relates_to::[Saltzer & Schroeder (1975) The Protection of Information in Computer Systems](../citations/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems.html)
  - The source paper that named and defined the principle
- relates_to::[Principle of Least Authority](Principle%20of%20Least%20Authority.html)
  - Miller's scope expansion from individual permissions to transitive authority chains
- relates_to::[Principle of Least Access](Principle%20of%20Least%20Access.html)
  - Allen's extension of the lineage from system permissions into data exposure
- relates_to::[Necessary Privilege](Necessary%20Privilege.html)
  - The inside-out counterpart: what does the user actually need?
- relates_to::[Delegated Decision Authority Spectrum](../boundaries/Delegated%20Decision%20Authority%20Spectrum.html)
  - Authority zones operationalize privilege boundaries for agent systems
