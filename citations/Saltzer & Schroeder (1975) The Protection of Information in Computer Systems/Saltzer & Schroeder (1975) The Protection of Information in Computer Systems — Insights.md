---
created: 2026-04-01
author: Christopher Allen
brief_summary: "Extraction candidates from the Saltzer & Schroeder (1975) paper. Each item is tagged with a target garden form type and the inference level (direct, extended, or synthesized). Ghost links name nodes that do not yet exist."
tagline: "Extraction candidates from the 1975 principles paper, tagged by form type"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]

# Saltzer & Schroeder (1975) The Protection of Information in Computer Systems — Insights

## Extraction Candidates

### Principles

**Target: [Principle of Least Privilege](../../glosses/Principle%20of%20Least%20Privilege.html)** — **Extracted** as Gloss
The paper's Principle f: "Every program and every user of the system should operate using the least set of privileges necessary to complete the job." The paper provides both the canonical statement and the rationale (limits damage from accidents, reduces auditable surface, provides a rationale for placing firewalls). A Principle Form node would capture this as a first-class garden principle with its full definition, lineage, and application to agentic contexts.

**Target: [[Fail-Safe Defaults]]** — `Principle Form` — direct
Principle b: base access decisions on permission rather than exclusion. The default situation is lack of access; conditions under which access is permitted must be identified. The paper articulates the asymmetric failure mode logic: permission-granting mechanisms fail safely (by refusing access, which is immediately detected); denial-based mechanisms fail dangerously (by granting access, which may go unnoticed).

**Target: [[Complete Mediation]]** — `Principle Form` — direct
Principle c: every access to every object must be checked for authority. The paper's rationale — "forces a system-wide view of access control, which in addition to normal operation includes initialization, recovery, shutdown, and maintenance" — is the full statement. Performance caching of authorization results must be designed so authority changes invalidate cached results.

**Target: [[Separation of Privilege]]** — `Principle Form` — direct
Principle e: where feasible, a protection mechanism that requires two keys to unlock is more robust and flexible than one allowing access with a single key. The paper names the nuclear weapons authorization system and bank safe-deposit boxes as non-computer exemplars. The application to agentic systems — requiring two independent conditions for high-consequence irreversible actions — is a direct extension.

**Target: [[Economy of Mechanism]]** — `Principle Form` — direct
Principle a: keep the design as simple and small as possible. The paper's rationale is specific to protection mechanisms: implementation errors that result in unwanted access paths will not be noticed during normal use, so line-by-line inspection techniques are necessary, and those techniques require a small and simple design to succeed.

**Target: [[Open Design]]** — `Principle Form` — direct
Principle d: the mechanism should not depend on the ignorance of potential attackers, but on possession of specific, more easily protected keys or passwords. Closely related to Kerckhoffs's principle in cryptography. Enables public review without compromising the mechanism.

**Target: [[Least Common Mechanism]]** — `Principle Form` — direct
Principle g: minimize the amount of mechanism common to more than one user and depended on by all users. Every shared mechanism is a potential information path between users. When a function can be implemented as a shared supervisor procedure or as a library procedure in the user's own environment, prefer the latter.

**Target: [[Psychological Acceptability]]** — `Principle Form` — direct
Principle h: the human interface must be designed for ease of use so that users routinely and automatically apply the protection mechanisms correctly. The principle identifies a mechanism design failure mode: if users must translate their mental model of protection goals into a radically different specification language, they will make errors that become security violations.

### Glosses

**Target: [[Principal (Security)]]** — `Gloss Form` — direct
The paper's glossary defines a principal as "the entity in a computer system to which authorizations are granted; thus the unit of accountability in a computer system." This is a precise technical definition distinguishing principal (who is accountable) from user (who operates the system) — a distinction important for multi-agent systems where a user may operate through multiple agents.

**Target: [[Capability (Computer Security)]]** — `Gloss Form` — direct
Defined in the paper's glossary as "an unforgeable ticket, which when presented can be taken as incontestable proof that the presenter is authorized to have access to the object named in the ticket." The capability system section (Section II-B) develops the full architecture.

**Target: [[Protection Domain]]** — `Gloss Form` — direct
Implied throughout but explicitly defined in the glossary as "the set of objects that currently may be directly accessed by a principal." Domain switching — changing which protection domain a computation operates within — is the mechanism by which protected subsystems work.

### Patterns

**Target: [[Two-Key Authorization Pattern]]** — `Pattern Form` — extended
Separation of privilege as an architectural pattern: any high-consequence operation requires two independent conditions to be satisfied before it proceeds. The two keys can be cryptographic, organizational (two different approvers), or architectural (two independent code paths). The agentic architecture application: agent judgment + user confirmation for irreversible actions.

**Target: [[Permission-First Default Pattern]]** — `Pattern Form` — direct
The fail-safe defaults principle as an architectural pattern: when building any access decision system, structure it so that the default outcome is denial, and conditions for permission must be explicitly enumerated. Applied to agent tool grants: agents hold no tools by default; each capability must be explicitly granted for each session or task.

### Models

**Target: [[Access Control List vs. Capability System]]** — `Model Form` — direct
The paper's Section II develops both models in detail and their structural comparison. The fundamental insight: access control lists answer "who can access this object?" efficiently; capability systems answer "what can this principal access?" efficiently. The tradeoffs in revocation, delegation, and dynamic authorization are described. This warrants a Model Form node capturing the comparison and the conditions under which each is preferred.

### Inquiries

**Target: [[How Should Agent Capability Systems Handle Revocation]]** — `Inquiry Form` — extended
The paper identifies revocation as the hard problem in capability systems: unforgeable tickets cannot easily be "unticketed." Modern approaches include short-lived capabilities that expire, capability lists with revocation bits, and indirect capabilities through a revocable indirection layer. The question for agentic architectures: what is the right revocation model for agent tool grants, especially in multi-agent systems where one agent may have delegated capabilities to another?

**Target: [[When Does Shared Mechanism Become Acceptable Risk]]** — `Inquiry Form` — extended
The least common mechanism principle counsels minimizing shared mechanisms, but total elimination is neither possible nor desirable — shared mechanisms are how systems provide services. The inquiry: what criteria determine when a shared mechanism's benefit outweighs its information-path risk? The paper gestures toward this ("some mechanisms serving all users must be certified to the satisfaction of every user") but does not resolve it.

## Ghost Links

The following nodes are referenced or implied but do not exist in the garden:

- [Principle of Least Privilege](../../glosses/Principle%20of%20Least%20Privilege.html) — **extracted** as gloss
- [[Fail-Safe Defaults]] — should be a Principle Form node
- [[Complete Mediation]] — should be a Principle Form node
- [[Separation of Privilege]] — should be a Principle Form node
- [[Economy of Mechanism]] — should be a Principle Form node
- [[Open Design]] — should be a Principle Form node (related to [[Kerckhoffs's Principle]])
- [[Least Common Mechanism]] — should be a Principle Form node
- [[Psychological Acceptability]] — should be a Principle Form node
- [Principle of Least Authority](../../glosses/Principle%20of%20Least%20Authority.html) — **extracted** as gloss
- [[Two-Key Authorization Pattern]] — Pattern Form for the separation of privilege mechanism
- [[Permission-First Default Pattern]] — Pattern Form for fail-safe defaults as architectural pattern
- [[Access Control List vs. Capability System]] — Model Form comparison
- [[Principal (Security)]] — Gloss Form; distinct from user and from principal in agency law
- [[Capability (Computer Security)]] — Gloss Form for the ticket-based authorization model
- [[Protection Domain]] — Gloss Form for the set of objects accessible to a principal
- [[Kerckhoffs's Principle]] — parallel open design principle from cryptography
