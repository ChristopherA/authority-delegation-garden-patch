---
created: 2026-03-28
author: Christopher Allen
brief_summary: "Personal multi-agent systems face context, attention, and cost ceilings that a flat or monolithic agent network cannot solve. The solution: divide agents into heavyweight orchestrators with domain ownership and persistent state, and lightweight workers that execute bounded commissions without accumulating identity. Both OpenClaw and this estate converged on this split independently, as did at least two other published systems."
tagline: "Domain owners on top, task executors below — the split every personal agent system needs"
---

- is_a::[Pattern Form](../forms/Pattern%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Agentic Architecture](../domains/Agentic%20Architecture.html)
- in_precinct::[[Garden Precinct]]↑
- extracted_from::[[Garden Node Candidates from OpenClaw Estate Convergence]]↑

# Orchestrator-Worker Separation in Personal Multi-Agent Systems

## Heart

Domain owners on top, task executors below. A small number of heavyweight orchestrators hold persistent state and coordinate work within their domains; a larger pool of lightweight workers execute bounded commissions without accumulating identity across invocations. This two-tier split resolves three ceilings simultaneously — context, attention, and cost — that a flat network or monolithic agent cannot.

## Problem

Personal multi-agent systems face context, attention, and cost ceilings that a flat peer network cannot solve — no single agent holds enough context to span multiple domains, the principal cannot oversee many heavyweight agents, and running every agent at maximum capability is economically unsustainable.

## Context

A builder assembles a personal multi-agent system and faces an immediate design question: should all agents be peers, or should some agents coordinate others? The naive starting point is a flat network where any agent can call any other, or a single powerful agent that handles everything. Neither holds up as the system grows.

## Forces

- **Context ceiling**: No single agent holds enough context to span multiple domains without degradation. An agent responsible for fiction writing, infrastructure monitoring, and research routing cannot maintain deep expertise in all three simultaneously.

- **Attention ceiling**: A single principal overseeing many heavyweight, stateful agents cannot monitor each one effectively. Agent count grows until oversight becomes infeasible.

- **Cost ceiling**: Running every agent at maximum capability is economically unsustainable for a personal system.

- **Task isolation**: Many tasks are bounded and stateless — they don't require accumulated context to execute well. Giving them heavyweight, stateful agents wastes resources and complicates oversight.

## Solution

Separate agents into two tiers: a small number of heavyweight orchestrators with domain ownership, persistent state, and coordination authority; and a larger pool of lightweight workers that execute bounded commissions without accumulating identity across invocations. Orchestrators run on expensive, capable models; workers run on cheaper models matched to their task types. Each orchestrator owns a domain — it routes work to workers rather than executing everything directly.

## Consequences

The orchestrator-worker ratio converges empirically across independent systems: Lawson reduced from approximately 30 to 8 orchestrators; the author's personal system operates with 3 orchestrators and 7+ workers. Both landed somewhere between a 2:1 and 5:1 workers-to-orchestrators ratio.

Adding a new domain requires adding an orchestrator, not just workers. The pattern enables model tiering: workers execute bounded tasks that match cheaper models; only orchestrators require the full judgment capability of expensive models.

A flat network or single monolithic agent exhibits predictable failure modes: context overload, oversight burden, or cost unsustainability. The two-tier structure solves all three ceilings simultaneously, though it introduces coordination overhead and requires clear domain boundaries between orchestrators.

## Known Results

Lawson (2026) built OpenClaw with 8 orchestrators and approximately 35 personas, converging down from an earlier attempt at 30 agents. The author's personal system runs 3 orchestrators with 7+ workers. Osmani and Brady's Squad system both describe a "conductor to orchestrator" and "coordinator to specialist" progression — arriving at the same structural split from different starting contexts.

## Sources

- [[Lawson (2026) OpenClaw as Force Multiplier]]↑: 8 orchestrators plus approximately 35 personas, convergence from 30 agents
- [[The Code Agent Orchestra - what makes multi-agent coding work (@addyosmani)]]↑: "conductor to orchestrator" progression
- [[How Squad runs coordinated AI agents inside your repository (@bradygaster)]]↑: coordinator routing to specialist agents

## Relations

- relates_to::[[Functional Types in Agent Taxonomy]]↑
  - The Decision names the three functional types; this Pattern explains why the orchestrator-worker split is needed and what forces create it. Not duplicative — the Decision names the types, this Pattern covers the problem-solution structure.

- relates_to::[[Augmentation Over Autonomy in Agent Architecture]]↑
  - The orchestrator tier is where human augmentation is concentrated. Orchestrators run with human oversight; workers execute within orchestrator-defined boundaries.

- composes_with::[[Tiered Model Allocation by Task Type]]↑
  - Orchestrator-worker separation enables model tiering. Once structural roles are separated, model allocation maps naturally onto them.

- relates_to::[[Persona Specialization Beats Generalization in Multi-Step Work]]↑
  - The worker tier benefits from deep specialization. Bounded task scope makes specialization practical.
