---
created: 2026-03-06
author: Christopher Allen
brief_summary: "Defines the Person Note vault type: a contact-style record for individuals referenced across the vault. Lives in People/Individuals/ and serves as the link target for attendee:: predicates in meetings and author:: references. Includes aliases, meeting history, project associations, and relationship context."
tagline: "Contact records linking people to their meetings, projects, and vault references"
formatted: "2026-03-14"
---

- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Household Precinct]]

# Person Note

A person note is a contact-style record for an individual referenced across the vault. Person notes live in `People/Individuals/` and serve as link targets for `attendee::` predicates in meeting notes and `author::` references in other contexts.

```
- is_a::[[Person Note]]
- has_status::[[Growing Stage]]
```

## Conventions

- **Location**: `People/Individuals/`, not `Notes/` (historical drift has some skills referencing `Notes/` — the canonical location is `People/Individuals/`).
- **Aliases**: YAML `aliases:` array for handles, shortened names, and social identifiers (e.g., `@ChristopherA`).
- **Frontmatter**: `created`, `reviewed`, `aliases`, `brief_summary`, `tagline`.
- **Content**: Professional context, project associations, meeting history (wikilinks to meeting notes), and relationship notes. Not a biography — focused on information relevant to vault work.

## Graph Participation

Person notes belong to the [[Household Precinct]] and participate in the knowledge graph through `attendee::` predicates (inbound from meeting notes) and as author references. They use the same typed-edge infrastructure as garden nodes. The vault principal authority (Christopher Allen) has a person note that documents his role in the augmented knowledge system.

## Sources

Person note conventions from vault-conventions-reference and meeting-capture skill (D8-D13 decisions).

## Relations

- relates_to::[[Meeting Note]] — person notes are linked from meeting attendee predicates
