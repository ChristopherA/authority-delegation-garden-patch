---
created: 2026-04-01
part_of: "[[Miller (2006) Robust Composition]]"
role: insights
---

part_of::[[Miller (2006) Robust Composition]]

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]

# Insights: Miller (2006) Robust Composition

Extracted takeaways from Miller's dissertation for the garden's knowledge domains, with connections to existing nodes.

## POLA as the Formal Grounding for Authority Flows from the Person

Miller's dissertation provides the formal security theory behind [[Authority Flows from the Person]]. The principle node asserts that authority over one's knowledge system originates with the person and is delegated outward — not acquired contextually by agents through ambient access.

The capability model is the structural implementation of this principle: authority travels with capability references that must be explicitly passed by the person (or their authorized delegates). A system in which an agent acquires authority through ambient execution context — because it runs with the user's credentials — is precisely the POLA violation Miller is identifying. The garden principle is the normative statement; Miller's dissertation is the formal security architecture behind it.

This is a citation-grounds-principle relationship, not merely a relates-to: Miller's work provides the theoretical foundation for why the principle is architecturally sound, not just ethically preferable.

**Extraction target**: [[Authority Flows from the Person]] — add Miller (2006) as a formal security grounding citation alongside the SSI citations that currently anchor it.

## Transitive Authority as the Diagnostic for Agentic AI Systems

The most direct application to the garden's agentic architecture work is Miller's transitivity insight: least authority analysis requires mapping the full authority graph, not just direct permissions.

Applied to agentic AI: when an agent runs in a user's environment with broad file, API, and tool access, the POLA violation is not the specific operations the agent performs — it is the reachable authority from the agent's execution context. Any malicious input (prompt injection, compromised tool response, adversarial web page) that can invoke the agent can redirect the agent's ambient authority toward arbitrary resources.

The confused deputy problem in agentic systems is not hypothetical. It is the structure of every prompt injection attack: the user's trusted agent is given malicious instructions by an untrusted input source, and the agent exercises its ambient authority on behalf of that input. This is exactly Hardy's 1988 compiler example, with the AI agent in the compiler's role.

**Extraction target**: [[Confused Deputy Problem in Agentic Systems]] — ghost link, worth creating as a Gloss Form node grounding the prompt injection failure mode in capability security theory.

**Extraction target**: A Pattern Form node on capability-scoped agentic architecture — each agent invocation should receive only the capability references required for the specific task, with no ambient authority beyond those explicit grants.

## The Unification Claim Applied to Multi-Agent Systems

Miller's unification of access control and concurrency control has an implication for multi-agent estate architectures: a correctly designed concurrent multi-agent system is also a correctly designed access-control system.

The estate's orchestrator-worker model already applies this implicitly: workers operate in scoped worktrees with limited read/write permissions, receive commissions that specify their scope, and cannot affect the main branch directly. This is a capability-scoped architecture for concurrency (parallel workers without shared state conflicts) that simultaneously provides access control (workers cannot exceed their commission scope).

The convergence is not accidental — it is exactly what Miller's thesis predicts. The estate architecture arrived at capability discipline from the concurrency direction (worktrees for parallelism) and the security direction (scope boundaries for safety) and found the same architecture.

**Connection**: [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]] — this pattern is an application of capability-scoped concurrency at the estate level.

## Ambient Authority as the Root Risk in Current AI Deployment

Miller distinguishes ambient authority (available to any code in the execution context without explicit designation) from capability-conferred authority (travels with an explicit reference). This distinction names the most common failure mode in current AI agent deployments.

Most AI agents deployed today operate with substantial ambient authority: they run with the user's API keys, have filesystem access, can invoke arbitrary tools, and exercise network access. The user may believe they have authorized a specific task; they have actually authorized the agent's entire ambient authority scope, because authority is not bundled with the specific task designation. This is an ACL-style architecture for AI delegation: the agent inherits execution context rather than receiving explicit capability grants.

The principle implication: AI agent architectures that grant ambient authority rather than capability-scoped authority cannot satisfy POLA by construction, regardless of what the agent's behavioral constraints say. Behavioral constraints (system prompts, fine-tuning for safety) are like ACL checks: they operate at execution time, not at architecture time, and can be bypassed through confused-deputy-style injection.

**Extraction target**: [[Behavioral Constraints Cannot Substitute for Capability Architecture]] — ghost link, worth creating as a Principle Form node. The argument: runtime behavioral constraints on agents are analogous to ACL checks on programs — they do not prevent confused-deputy attacks, which exploit the gap between authority and designation.

## Capability Discipline as a Design Quality Signal

Chapter 8's argument that POLA produces cleaner, more modular software — not just more secure software — maps onto the garden's own design principles.

[[Content Over Container]] and [[Living Documents Over Static Publications]] reflect a preference for design discipline that has intrinsic quality properties beyond their stated purpose. Miller makes the same argument about capabilities: a system designed for minimum authority necessarily has explicit interfaces, narrow scopes, and traceable dependencies — properties that improve understandability and testability independently of security.

This suggests a design heuristic for the estate: when an agent or component needs broad ambient access to function, that is a design signal that its scope is too wide, not just a security concern. The capability check and the modularity check are the same check.

## Ghost Links Surfaced

- [[Confused Deputy Problem in Agentic Systems]] — Gloss Form node grounding prompt injection in capability security theory
- [[Behavioral Constraints Cannot Substitute for Capability Architecture]] — Principle Form node on the limits of runtime safety constraints
- [[Capability-Scoped Agentic Architecture]] — Pattern Form node on minimum-authority agent design
- [[Mark S. Miller]] — Person Note, the author; important enough for garden representation given how many principles trace through his work
- [[Saltzer and Schroeder (1975) Protection of Information in Computer Systems]] — the prior citation Miller extends; ghost link as a citation the garden should have
- [[Object-Capability Model]] — Gloss Form node defining the security model the dissertation formalizes
- [[Transitive Authority]] — Gloss Form node; the key diagnostic concept from Chapter 8

## Connections Summary

| Insight | Existing Garden Node | Relationship |
|---------|---------------------|--------------|
| POLA = formal grounding for authority-from-person | [[Authority Flows from the Person]] | Formal foundation |
| Transitivity = diagnostic for agent ambient authority | [[Human Authority Over Augmentation Systems]] | Architectural application |
| Confused deputy = prompt injection structure | [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]] | Failure mode analysis |
| Capability scope = concurrency + access control unified | [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]] | Theoretical grounding |
| Capability discipline = design quality signal | [[Content Over Container]] | Convergent principle |
| Allen 2023 extends Miller's transitivity to data | [[Allen (2023) Least and Necessary Design Patterns]] | Direct lineage |
| POLA and SSI minimalization share structure | [[Allen (2016) The Path to Self-Sovereign Identity]] | Structural parallel |
