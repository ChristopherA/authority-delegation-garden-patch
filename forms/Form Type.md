---
created: 2026-03-06
author: Christopher Allen
brief_summary: "A form type is a knowledge object category with a known internal structure — a contract about what sections it contains and what question it answers. 17 form types are defined across five categories (Orientation, Structural, Action, Generative, Governance)."
tagline: "The structural contract that defines what shape a knowledge object takes"
---

- is_a::[[Form Type]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Garden Precinct]]
- in_precinct::[[Household Precinct]]

# Form Type

A form type is a knowledge object category with a known internal structure — a contract about its shape. Each form type answers a distinct question and serves a distinct purpose.

Form types belong to five categories:

### Orientation Forms

*What matters? What do we believe?*

| Form Type | Core Question |
|-----------|---------------|
| [[Conviction Form]] | What do we believe is true about the world? |
| [[Value Form]] | What do we care about? |
| [[Principle Form]] | What must we always or never do? |

### Structural Forms

*How do things relate? What do we understand?*

| Form Type | Core Question |
|-----------|---------------|
| [[Model Form]] | How do these elements relate to each other? |
| [[Reference Form]] | What do I need to know about this domain to act effectively? |
| [[Gloss Form]] | What does this specific source or concept mean? |
| [[Citation Form]] | What do I need to know about this source? |
| [[Opus Form]] | What am I saying here, and how does it connect? |
| [[Domain Form]] | What knowledge area does this cluster of forms belong to? |

### Action Forms

*What to do? What happened? Who acts?*

| Form Type | Core Question |
|-----------|---------------|
| [[Pattern Form]] | What resolves this recurring tension? |
| [[Case Form]] | What happened when this was tried? |
| [[Decision Form]] | Why did we choose this over the alternatives? |
| [[Protocol Form]] | How do independent parties coordinate reliably? |
| [[Skill Form]] | How does an agent execute this reliably? |
| [[Persona Form]] | Who is this agent and how does it behave? |

### Generative Forms

*What should we investigate? What might happen?*

| Form Type | Core Question |
|-----------|---------------|
| [[Inquiry Form]] | What should we think about X, and how would we find out? |
| [[Scenario Form]] | What might happen if these forces play out? |

### Governance Forms

*Who decides? How do rules change?*

| Form Type | Core Question |
|-----------|---------------|
| [[Boundary Form]] | Where does this system's authority end? |

All 18 form types have definition pages. 15 types have instantiated nodes in the garden; 3 types (Protocol, Skill, Scenario) have definition pages but no content nodes yet. Persona Form is new (2026-03-21) with two exemplars (Groundskeeper, Gardener).

## Garden Nodes and Vault Nodes

Form types serve two precincts within the deep context architecture. [[Garden Precinct]] nodes (the 16 types above) carry structural contracts — required sections, specific shapes, enforceable constraints. [[Household Precinct]] nodes (Meeting Note, Transcript, Person Note, Chat Log, Sidecar) are operational templates with conventions but lighter structural requirements. Both precincts use `is_a::` predicates, typed edges, and the same graph infrastructure. Some form types (Status Stages, Domain Form) serve both precincts.

The two precincts solve different problems — the garden curates durable knowledge, the vault captures operational information — rather than representing different maturity levels of the same thing.

## Sources

Taxonomy from [[Deep Context as an Architecture for Captured Reasoning]], "The Forms" section.

## Relations

- relates_to::[[Seed Stage]] — all nodes start at seed stage
- relates_to::[[Deep Context Architecture]] — the domain that defines the type system
