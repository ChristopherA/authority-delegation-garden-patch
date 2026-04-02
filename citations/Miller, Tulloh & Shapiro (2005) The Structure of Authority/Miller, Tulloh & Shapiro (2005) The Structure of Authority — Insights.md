---
created: 2026-04-01
part_of: "[[Miller, Tulloh & Shapiro (2005) The Structure of Authority]]"
---

# Miller, Tulloh & Shapiro (2005) The Structure of Authority — Insights

## Extraction Candidates

### Insight 1: The Designation-Authority Coupling Principle
**Target form**: [[Principle Form]] or [[Gloss Form]]
**Inference level**: Direct extraction
**Garden connection**: [[Human Authority Over Augmentation Systems]], [[Authority Flows from the Person]]

The `cp`/`cat` example crystallizes a principle applicable far beyond Unix shell commands: how a system handles designation (naming, addressing, reference) determines what authority any component requires to do its job. Systems that pass string names push namespace resolution authority down into receiving components. Systems that pass resolved references let callers retain namespace authority and grant only what the callee needs.

For agentic architectures, this principle has direct application: an agent given a task by name ("process my email") must hold broad authority to interpret what that means. An agent given a specific designated object (a reference to a specific email thread, an open file handle) needs only the authority to work with that object. The user's act of designation is itself an authority grant.

Ghost link: [[Designation as Authority Grant]]

---

### Insight 2: Security as Modularity Traced to Its Limit
**Target form**: [[Conviction Form]] or [[Principle Form]]
**Inference level**: Direct from Table 1 and the paper's framing
**Garden connection**: [[Values Precede Technical Decisions]]

The paper's Table 1 maps software engineering practices to capability discipline equivalents: information hiding → POLA; omit needless coupling → omit needless vulnerability; responsibility-driven design → authority-driven design. The underlying claim: capability security is modular software engineering applied to the access dimension. An engineer who practices good modularity has already done most of the work; the remaining step is to make access graphs as sparse as knowledge graphs.

This reframes capability security from "security mechanism" to "design discipline." The question is not "how do we add security?" but "have we applied our modularity principles to authority as rigorously as we have to knowledge?"

Ghost link: [[Authority Sparseness as Design Quality]]

---

### Insight 3: The Fractal POLA Model for Agent Systems
**Target form**: [[Model Form]] or [[Pattern Form]]
**Inference level**: Analogical — the four-level model applies directly to multi-agent architectures
**Garden connection**: [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]], [[Human Authority Over Augmentation Systems]]

The paper's four-level hierarchy (organization → user → application → module → object) maps onto multi-agent system architecture. An agentic estate has:

- **Estate level** (organization): the human principal holds ultimate authority
- **Orchestrator level** (application): the Groundskeeper, Chancellor, etc. hold bounded precinct authority
- **Worker level** (module): Cultivators, Pruners, Foragers hold commission-scoped authority
- **Operation level** (object): individual tool calls hold only what the operation requires

At each level, the TCB is the entity that manages authority delegation to the level below. The orchestrator is in the worker's TCB; the human is in the orchestrator's TCB. Compromise at any level exposes only that level's authority, not the levels above it — if the level above practiced POLA.

Ghost link: [[POLA Applied to Multi-Agent Authority Hierarchies]]

---

### Insight 4: Request-Time Authority as the Right Primitive
**Target form**: [[Principle Form]]
**Inference level**: Direct from the abstract's formulation
**Garden connection**: [[Human Authority Over Augmentation Systems]]

"Only when requests are made... can we determine how much authority is adequate." This sentence resolves a persistent tension in agent permission design: how to give agents enough authority to be useful without giving them excess authority that could be abused.

The answer the paper implies: the right unit of authority is a request with its designated objects, not a role with its static permissions. An agent should receive authority when it is designated a task with specific objects — not in advance, as a standing permission. The human's designation act is the authority grant; the agent's authority expires when the task is complete.

This is harder to implement than role-based permissions but is the correct design. Current agentic frameworks largely use role-based or capability-list approaches because they are simpler; the paper explains why this creates the same excess-authority problem as conventional operating systems.

Ghost link: [[Just-In-Time Authority vs Standing Permissions]]

---

### Insight 5: The TCB Nesting Insight for Agent Architecture
**Target form**: [[Model Form]] or [[Pattern Form]]
**Inference level**: Analogical extension
**Garden connection**: [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]]

The paper's TCB nesting insight: every entity that manages authority delegation to others is in the TCB of the authority it manages. Applied to agent systems: the orchestrator agent is in the TCB of every worker it spawns, because the orchestrator determines what authority those workers receive. The human is in the orchestrator's TCB.

This means that reducing TCB exposure in agentic systems requires minimizing what orchestrators hold. An orchestrator that holds all estate authority (to take any action, access any resource) places that full authority at risk of any orchestrator compromise. An orchestrator that holds only the authority it needs to delegate appropriate sub-authority to workers limits its compromise exposure.

A commission architecture where workers operate in worktrees with limited scope partially implements this. The open question is whether orchestrators — agents that coordinate workers — can also be scoped to hold only the authority they need to delegate, rather than holding full estate authority by default.

---

### Insight 6: Legacy Coexistence as Incremental Path
**Target form**: [[Pattern Form]]
**Inference level**: Direct from Section 3.7
**Garden connection**: No direct existing node — ghost link candidate

The paper describes how capability-secure systems can coexist with legacy components through external containment (Polaris: run legacy in a limited account) and taming (wrap legacy so it cannot exceed granted authority). The key property: incremental adoption is possible. A system does not need to be fully capability-secure to benefit from capability security in the parts that are.

For agent estates: existing tools, shell commands, and APIs are "legacy" in this sense — they were not designed for capability security. The pattern of wrapping them with explicit authority grants (analogous to Polaris's file designation flow) is the practical path toward POLA-compliant agent operations.

Ghost link: [[Legacy Containment Pattern for Agent Tools]]

---

### Insight 7: Connectivity Propagation Rules
**Target form**: [[Gloss Form]] or [[Model Form]]
**Inference level**: Direct from Section 3.4
**Garden connection**: Ghost link — no existing node

The paper's four rules for how authority propagates (introduction, parenthood, endowment, initial conditions) define the complete authority propagation algebra for capability systems. "Only connectivity begets connectivity" is the invariant. Two subsystems with no reference path between them cannot affect each other — which is why garbage collection can be transparent and why security analysis is tractable.

For the garden's multi-agent work, these rules describe how to reason about what an agent can do: trace forward from its initial endowment through introduction events (what did the user pass to it? what did the orchestrator introduce it to?). The authority boundary is always the reference boundary.

Ghost link: [[Capability Propagation Rules]]

---

## Domain Relevance Assessment

**Primary domain**: [[Agentic Architecture]] — the paper provides the theoretical grounding for capability-based agent authority management

**Secondary domain**: [[Self-Sovereign Identity]] — the designation-authority coupling principle applies to identity systems (who can access your identity attributes, and how that authority propagates)

**Strong connection nodes already in garden**:
- [[Human Authority Over Augmentation Systems]] — the paper operationalizes what "boundary-setting" means at the code level
- [[Authority Flows from the Person]] — the capability model's "only connectivity begets connectivity" rule expresses at the code level what this principle expresses at the design level
- [[Orchestrator-Worker Separation in Personal Multi-Agent Systems]] — the TCB nesting insight directly informs how to scope orchestrator authority

**Ghost links generated** (candidate nodes for the garden):
- [[Designation as Authority Grant]]
- [[Authority Sparseness as Design Quality]]
- [[POLA Applied to Multi-Agent Authority Hierarchies]]
- [[Just-In-Time Authority vs Standing Permissions]]
- [[Legacy Containment Pattern for Agent Tools]]
- [[Capability Propagation Rules]]
- [[Object-Capability Model]]
- [[Principle of Least Authority]]
