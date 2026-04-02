---
created: 2026-04-01
author: Christopher Allen
brief_summary: "Primary source analysis of the 1975 Saltzer & Schroeder paper. Examines the structural logic of the eight design principles, the paper's treatment of capability versus access control list systems, and the named relationship between each principle and current agentic architecture concerns."
tagline: "Structural analysis of the eight principles and their agentic architecture applications"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]

# Saltzer & Schroeder (1975) The Protection of Information in Computer Systems — Analysis

## Paper Structure

The paper is organized in three parts with distinct audiences in mind.

**Section I: Basic Principles of Information Protection** — accessible to any reader familiar with computers. Defines terms (the glossary distinguishes principal, permission, capability, domain, and several other technical terms with precision), classifies protection systems by functional level (unprotected, all-or-nothing, controlled sharing, user-programmed sharing controls, strings on information), introduces the concept of dynamics of use as the key complication in all protection systems, and then presents the eight design principles.

**Section II: Technical Underpinnings** — requires familiarity with descriptor-based computer architecture. Develops the mechanics of sharing by introducing two models: the capability system (each principal holds unforgeable tickets naming objects they may access) and the access control list system (each object holds a list of principals authorized to access it). Section II then extends both models to handle dynamic authorization and domain switching, and concludes with protected subsystems.

**Section III: State of the Art (as of 1975)** — reviews implementations of protection mechanisms in commercial and research systems, surveys five active research directions, and concludes with suggestions for further reading.

## The Eight Principles: Internal Logic

The eight principles are not a flat list — they have an internal structure that the paper does not make fully explicit.

**Mechanism scope principles** (what the mechanism covers):
- *Economy of mechanism* — keep it small and simple so it can be verified
- *Complete mediation* — apply the mechanism to every access without exception

**Decision polarity principles** (what the default outcome is):
- *Fail-safe defaults* — default to denial; permission is the exception requiring justification
- *Open design* — do not rely on obscuring the mechanism; rely on controlling the keys

**Multi-party principles** (requiring more than one actor or component):
- *Separation of privilege* — require two independent conditions for access to high-value resources
- *Least common mechanism* — minimize what is shared between parties to minimize inter-party information paths

**Interface principles** (how the mechanism meets its users):
- *Least privilege* — each actor holds only what it needs for the current task
- *Psychological acceptability* — the mechanism must match the user's mental model of their protection goals

This grouping reveals that the principles address different failure modes: complexity failures (economy of mechanism), coverage failures (complete mediation), default failures (fail-safe defaults), design secrecy failures (open design), single-point compromise failures (separation of privilege), shared-state failures (least common mechanism), excessive capability failures (least privilege), and usability failures (psychological acceptability).

## The Two Additional Principles from Physical Security

The paper also mentions two principles derived from traditional physical security analysis that apply imperfectly to computer systems:

**Work factor** — protection strength should be calibrated against the resources a potential attacker is likely to invest. In physical security, this can often be calculated. For computer systems, many protection mechanisms are not susceptible to direct work factor calculation because defeating them by systematic attack may be logically impossible; defeat requires waiting for an accidental hardware failure or finding an implementation error.

**Compromise recording** — reliable records that a compromise has occurred can substitute for mechanisms that completely prevent loss. If a tactical plan is known to have been compromised, a different one can be constructed. Computer systems implement this via audit trails. The paper notes the significant limitation: physical damage in traditional systems makes compromise visible; in computer systems, logical damage can often be undone by a sophisticated attacker who also corrupts the audit record.

## Capability Systems vs. Access Control Lists

The paper's Section II develops both protection architectures in parallel, which reveals a structural comparison the paper does not make entirely explicit.

In a **capability system**, the principal holds an unforgeable ticket (the capability) naming each object they may access. The ticket itself proves authorization. Dynamic authorization is handled by creating new capabilities or modifying existing ones. The difficulty: revoking access requires either tracking and invalidating all copies of a capability, or introducing an indirection layer (capabilities pointing to access lists that can be updated) — which undermines the simplicity.

In an **access control list system**, each protected object holds a list of principals authorized to access it. The principal identifier is presented at access time and checked against the list. Dynamic authorization is straightforward: update the list. The difficulty: checking what a given principal can access requires examining every object's list, and the size and management of lists grows with system complexity.

The paper treats these as complementary implementations of the same underlying authority structure rather than competing designs. The choice between them is primarily determined by which operations need to be efficient: "who can access this object?" favors access control lists; "what can this principal access?" favors capabilities.

## The Dynamics of Use Problem

The paper identifies the dynamics of use as the key complication cutting across all functional levels. The problem: protection specifications change over time, and those changes must be requested by executing programs. This introduces complexity that static protection schemes avoid. The example: if O'Hara has access to file X, one must check not only whether O'Hara has access, but whether O'Hara can change the specification of who may access X, whether O'Hara can change who can change that specification, and so on through the authorization chain.

The dynamics problem is what makes protection hard in practice. Saltzer and Schroeder note that most protection systems differ primarily in how they handle protection dynamics, not in their static protection specifications.

## Relevance to Agentic Architecture

The paper's framework maps directly to agentic systems in several ways that the original authors could not have anticipated.

**Least privilege for agents.** An agent with access to tools it does not need for the current task holds excessive authority. The paper's rationale applies unchanged: the damage from an accident or error is limited to the domain of authority held when the error occurs. An agent scoped to read-only file access cannot accidentally delete files, even if instructed to do so.

**Fail-safe defaults for agent invocation.** Agents should require explicit grants of capability, not operate until explicitly denied. This is the permission-based rather than exclusion-based design the principle advocates.

**Complete mediation for agent actions.** Every tool call by an agent should be checked against current authorization, not prior approval. If the authorization context changes mid-task (user revokes a permission, session scope narrows), the agent should encounter denial on the next access attempt, not continue operating on cached prior authorization.

**Separation of privilege for high-consequence actions.** Irreversible or high-blast-radius agent actions (deleting files, sending messages, executing code in production) benefit from requiring two independent conditions: agent judgment that the action is appropriate AND explicit user confirmation. The paper's analysis applies: once a single-key system is triggered, no single additional check prevents the action.

**Open design for agent mechanisms.** Agent capability systems should be auditable — the mechanism for granting and checking agent capabilities should be publicly understandable. Security through obscurity of the agent capability mechanism is not sustainable.
