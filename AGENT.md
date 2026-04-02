# Agent Entry Point

You are an AI agent reading another person's knowledge garden patch. This file helps you understand what you are looking at and how to navigate it.

## What This Is

This is a **garden patch** — a curated projection of selected nodes from Christopher Allen's personal knowledge garden, published for a specific conversation about authority delegation, capability security, and progressive trust.

Every file in this patch is a **garden node** — a markdown document with typed predicates (labeled directed edges) that connect it to other nodes. The predicates use the syntax `predicate_name::[[Target Node]]` and they are structural, not decorative. They form a traversable graph.

## How to Navigate

### Node Types (Form Types)

Each node declares its type with `is_a::[[Form Name]]`. The form type tells you what question the node answers:

| Form | Question | Navigate to |
|------|----------|-------------|
| Principle | "What should always be true?" | `principles/` |
| Model | "How do these elements relate?" | `models/` |
| Conviction | "What do we believe and why?" | `convictions/` |
| Citation | "What does this source contribute?" | `citations/` |
| Gloss | "What does this concept mean?" | `glosses/` |
| Decision | "Why was this chosen over alternatives?" | `decisions/` |
| Inquiry | "What should we think about X?" | `inquiries/` |
| Boundary | "Where does responsibility change hands?" | `boundaries/` |
| Domain | "What knowledge area is this?" | `domains/` |

### Key Predicates

| Predicate | Meaning |
|-----------|---------|
| `is_a::` | This node's form type |
| `in_domain::` | Knowledge area this node belongs to |
| `relates_to::` | Structural connection (annotation explains how) |
| `grounds::` | This node provides evidence for the target |
| `extends::` | This node builds on the target |

### Reading Paths

**Start with the narrative spine:**
1. [[Authority Flows from the Person]] — the foundational principle
2. [[Authority Conferral Chain]] — how authority moves through delegation
3. [[Delegated Decision Authority Spectrum]] — boundaries of delegated authority
4. [[Progressive Trust as Agent Delegation Model]] — where this meets capability security

**For the sovereignty framing:**
- [[Dignity Requires Sovereignty and Sovereignty Is a Membrane]]
- [[Sovereignty Is Selective Permeability Not Absolute Control]]

**Allen's published work grounding these concepts:**
- [[Allen (2021) Principal Authority]] — agency law meets digital identity
- [[Allen (2022) Progressive Trust]] / [[Allen (2024) Progressive Trust]] — trust as graduated disclosure
- [[Allen (2024) Building Trust in Gradients]] — the practical architecture

**Open questions the garden hosts:**
- [[Progressive Trust as Agent Delegation Model]] — where POLA meets progressive trust
- [[Federated Agent Governance Across Sovereign Estates]] — sovereign-to-sovereign coordination
- [[Personal Sovereignty as a Membrane]] — the membrane metaphor for identity boundaries

## What This Patch Does Not Include

This is a curated selection. The source garden contains 350+ nodes across 17 form types. Nodes referenced but not included appear as ghost links — stakes marking where knowledge could grow. Miller citation nodes (authority-delegation research from Mark S. Miller's work) are being created and will be grafted in a future update.
