---
created: 2026-03-06
author: Christopher Allen
brief_summary: "Defines the Protocol form type: a specification for multi-party coordination across trust boundaries. Distinguished from a process by who must agree — a protocol works only if all parties follow it. Scope includes human coordination methods alongside technical protocols."
tagline: "How do independent parties coordinate reliably? — the structural contract for protocol forms"
---

- is_a::[[Form Type]]
- has_status::[[Seed Stage]]
- in_domain::[[Deep Context Architecture]]
- in_precinct::[[Garden Precinct]]

# Protocol Form

**Core question**: "How do independent parties coordinate reliably?"

A specification for multi-party coordination across trust boundaries. Distinguished from a process by who must agree: a process works if one agent follows it; a protocol works only if all parties follow it. Versioned and negotiated.

The scope includes human coordination methods (facilitation, deliberation, voting) alongside technical protocols. Whether "protocol" is the right name for this broader scope remains an open question — see [[Practices as Protocol Form Naming Alternative]] for detailed analysis of candidate names.

## Structural Contract

A protocol form requires:

- **Parties** — Who must participate and what roles they play.
- **Specification** — The coordination rules all parties must follow.
- **Trust boundaries** — What each party must trust and what they can verify.
- **Versioning** — How the protocol evolves and how changes are negotiated.
- **Sources** — Standards, RFCs, or precedent the protocol draws from.
- **Relations** — Connections to principles it embodies, patterns it implements, cases that demonstrate it.

Naming heuristic: name the coordination mechanism or its proper name. "Inter-Face Protocol" not "Agent Communication Protocol Form." If the protocol has an established name, use it.

## Typical Predicates

- `is_a::[[Protocol Form]]`
- `has_status::[[Seed Stage]]` or `[[Evergreen Stage]]`
- `in_domain::[[Domain Name]]`
- `coordinates::[[Party]]` — who participates
- `implements::[[Pattern Form]]` — patterns the protocol operationalizes
- `relates_to::[[Boundary Form]]` — authority boundaries the protocol respects

## Exemplars

- [[Inter-Face Protocol]] — peer-to-peer AI agent communication protocol for filtering social connections to surface conversations worth having

## Category

Action form — captures *what to do* and *what happened*.

## Sources

Definition from [[Deep Context as an Architecture for Captured Reasoning]], lines 97-98.

## Relations

- relates_to::[[Pattern Form]] — protocols operationalize patterns for multi-party contexts
- relates_to::[[Boundary Form]] — protocols respect authority boundaries between parties
- relates_to::[[Decision Form]] — protocol adoption is a decision; protocol design involves many decisions
