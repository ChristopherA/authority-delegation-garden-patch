---
created: 2026-03-31
author: Christopher Allen
brief_summary: "The same agent persona operates under different authority models depending on how it is launched. Commission topology — main versus worktree, orchestrator versus worker role — determines the authority relationship. This separates persona identity from operational authority."
tagline: "The same persona, different topology, different authority."
---

- is_a::[[Principle Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]

# Topology Determines Authority

An agent's authority is determined by its operational topology, not by its persona identity. The same persona operating on main as an orchestrator and operating in a worktree as a worker holds different authority relationships, even though its identity, knowledge, and capabilities are identical.

## Rationale

Agent systems risk collapsing authority into identity: "the Groundskeeper has full authority" as a property of the Groundskeeper persona rather than a property of its position in the current commission structure. When authority is persona-bound, it cannot be safely restricted for bounded work — a worker Groundskeeper carries the same authority as an orchestrator Groundskeeper, which defeats the isolation that worktree-based commissioning provides.

Separating topology from persona allows the same agent definition to be deployed in multiple authority contexts. The persona's capabilities, knowledge, and behavioral constraints remain stable. The authority relationship — what the agent is permitted to do, which files it may write, when it must escalate — is conferred by the commission topology.

## Manifestations

**On main branch**: An orchestrator Groundskeeper retains full authority over the garden: routing decisions, workstream creation, domain-level coordination. It can write to any garden path, merge worktree branches, and commission workers.

**In a worktree**: A worker Groundskeeper operates under a bounded commission: specific deliverables, specific file paths, a defined close-out report. It proposes changes to its own agent file; a human or orchestrator reviews at merge.

**In both cases**: The Groundskeeper persona is the same. Its skill set, its domain knowledge, its behavioral constraints are identical. Only the authority relationship differs.

## Diagnostic

If an agent's permissions or escalation requirements change based on which branch it is running on rather than what it knows, topology-based authority is working. If an agent in a worker worktree self-authorizes actions that an orchestrator would require approval for, topology is not determining authority — persona identity is.

## Sources

Topology-based authority analysis for the commission architecture, developed during garden foundation work (2026).

## Relations

- relates_to::[[Orchestrator-Worker Separation in Personal Multi-Agent Systems]] — the two-tier hierarchy implements topology-based authority structurally
- relates_to::[[Git Worktree Isolation as Agent Sandbox]] — worktrees are the mechanism that gives topology physical meaning; different branch, different authority scope
- relates_to::[[Delegated Decision Authority Spectrum]] — the boundary that topology-based authority enforces; which decisions each topology permits
- relates_to::[[Human Authority Over Augmentation Systems]] — the principle that topology-based authority operationalizes; human decisions determine who gets which topology
