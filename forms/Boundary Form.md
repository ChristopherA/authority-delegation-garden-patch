---
created: 2026-03-05
author: Christopher Allen
brief_summary: "Defines the Boundary form type: a declaration of what an agent may and may not decide. Not what the right choice is, not how to make it, but who holds authority. Amendable through deliberative process, never unilaterally. 1 instance in Garden/boundaries/."
tagline: "Where does this system's authority end? — the structural contract for boundary forms"
---

- is_a::[[Form Type]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Garden Precinct]]

# Boundary Form

**Core question**: "Where does this system's authority end?"

A declaration of what an agent (LLM, individual, group) may and may not decide. Not *what* the right choice is (principle), not *how* to make it (protocol), but *who holds authority*. Boundaries are the governance layer — the rules about who gets to play and what moves they can make. Amendable through deliberative process, never unilaterally by an LLM.

## Structural Contract

A boundary form requires:

- **Authority zones** — A table or structured list showing zones of authority with levels (autonomous, guided, escalate, prohibited) and examples for each zone.
- **Agent behavior at boundaries** — Steps for recognition and escalation when an agent encounters the boundary edge.
- **Amendment** — How the boundary can be changed and by whom. This section is mandatory because boundaries without amendment processes become brittle.
- **Sources** — Values and principles the boundary is grounded in.
- **Relations** — Connections to principles it enforces, models it constrains, and patterns it governs.

Naming heuristic: what's bounded + distinctive feature. "Delegated Decision Authority Spectrum" not "Authority Boundary."

## Typical Predicates

- `is_a::[[Boundary Form]]`
- `has_status::[[Seed Stage]]` or `[[Growing Stage]]`
- `in_domain::[[Deep Context Architecture]]`
- `grounded_in::[[Value]]` — values that justify the boundary
- `embodies::[[Pattern Form]]` — patterns that demonstrate the boundary
- `relates_to::[[Principle Form]]`, `[[Model Form]]`

## Exemplars

- [[Delegated Decision Authority Spectrum]] — authority zone table with HAAH spectrum, amendment process, and escalation steps

## Category

Governance form — establishes *who decides* and *how rules change*.

## Sources

Definition from [[Deep Context as an Architecture for Captured Reasoning]], lines 117-118.

## Relations

- relates_to::[[Principle Form]] — principles inform what boundaries protect
- relates_to::[[Model Form]] — models map the authority zones boundaries define
- relates_to::[[Decision Form]] — boundaries constrain what decisions an agent can make autonomously
