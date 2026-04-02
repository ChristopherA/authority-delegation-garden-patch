---
created: 2026-04-02
part_of: "[[Miller & Drexler (1988) Markets and Computation]]"
role: insights
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- part_of::[[Miller & Drexler (1988) Markets and Computation]]

# Miller & Drexler (1988) Markets and Computation — Insights

## Extraction Candidates

### Encapsulation as Property Rights

**Target form**: [[Gloss Form]]
**Inference level**: [source: direct from paper text]

Miller and Drexler identify a structural equivalence between object encapsulation in software and property rights in law. Both serve the same function: establishing protected spheres where entities plan and act with predictable consequences, despite limited knowledge of the external world. Object-oriented programming reinvented property rights without recognizing it had done so.

The insight extends: if encapsulation already handles property rights for *information* (the competence domain), extending it to *computational resources* (the performance domain) yields ownership and trade — the basis for markets.

**Ghost links**: [[Encapsulation as Property Rights]], [[Competence-Performance Distinction in System Design]]

**Garden connection**: This directly grounds [[Authority Flows from the Person]]. If encapsulation establishes protected spheres of action, then the authority exercised within those spheres flows from the encapsulation boundary — from the entity that controls what crosses the boundary, not from any external planner.

---

### Security Rests on Inabilities

**Target form**: [[Principle Form]]
**Inference level**: [source: direct from paper text]

"Turing-equivalence describes the *abilities* of a system, but security rests on inabilities — on the inability to violate certain rules. Adding an interpreter on top of a system cannot subtract abilities from the system itself."

This is a precise formulation of why security cannot be layered on after the fact. It anticipates the principle of least authority: security is not what a system *can* do but what it *cannot* do. Abilities are additive; inabilities must be foundational.

**Ghost links**: [[Security Rests on Inabilities Not Abilities]], [[Least Authority as Foundational Constraint]]

**Garden connection**: This grounds [[Allen (2023) Least and Necessary Design Patterns]] from a different direction. Allen's least authority is a design pattern; Miller and Drexler's formulation explains *why* it must be a foundational constraint rather than an applied pattern: you cannot subtract abilities by adding layers.

---

### The Firm Boundary in Computational Markets

**Target form**: [[Pattern Form]]
**Inference level**: [source: direct from paper text, with garden-level inference]

**Context**: A computational market must decide at what granularity market mechanisms apply. Fine-grained markets impose overhead on every transaction; coarse-grained markets lose the benefits of price-guided tradeoffs.

**Forces**: Transaction costs (accounting, negotiation) favor aggregation into larger units with internal command structures. But internal command structures lose the benefits of distributed knowledge and price-guided tradeoffs.

**Solution**: Objects aggregate into "firms" — internally coordinated units that participate in markets only at boundaries where transactions are large enough to justify overhead. Market competition itself tunes this boundary. "Islands of central direction in a sea of trade."

**Consequences**: No single granularity is optimal everywhere. The system self-organizes into a hierarchy of market and command zones.

**Ghost links**: [[Computational Coase Theorem]], [[Market-Command Boundary in Agent Systems]]

**Garden connection**: The estate's own architecture exhibits this pattern. Orchestrator agents coordinate workers internally (command), while the commission architecture between orchestrators and workers uses bounded contracts (market-like). The Groundskeeper's commission to a Forager is a transaction at a natural boundary; the Forager's internal file reads are not.

---

### Business Agent Delegation as Competence-Performance Separation

**Target form**: [[Pattern Form]]
**Inference level**: [source: direct from paper text]

**Context**: Simple objects in a complex market cannot handle both their core function (competence) and sophisticated resource management (performance).

**Forces**: Market sophistication requires negotiation, reputation assessment, and adaptive resource allocation. Embedding this in every object bloats simple services with market logic.

**Solution**: Separate competence delegation (subcontractors that do work) from performance delegation (agents that manage resources, prices, and negotiations). Simple objects delegate performance-domain decisions to shared business agents, just as they delegate competence-domain tasks to subcontractors.

**Consequences**: Simple objects compete in open markets despite limited sophistication. Agent logic is shared across many objects, amortizing overhead. Different objects can use different agents, providing evolutionary flexibility.

**Ghost links**: [[Competence-Performance Separation]], [[Agent Delegation for Resource Management]]

**Garden connection**: This maps to the estate's persona-agent distinction. The persona defines *what* the agent does (competence); the estate charter and commission architecture define *how* it manages resources, context budget, and close-out obligations (performance). A simple Gardener worker does not need to know commission design — it delegates that to the Groundskeeper.

---

### Positive Reputation Through Bonded Commitment

**Target form**: [[Pattern Form]]
**Inference level**: [source: direct from paper text]

New objects establish reputations not by demonstrating past performance but by posting cash bonds guaranteeing future performance, enforced by trusted third parties. This resolves the bootstrap problem of reputation ("can't get the job without experience").

The paper notes that "despite the idea that software entities cannot make commitments, contracts with enforceable penalty clauses provide a way for them to do so."

**Ghost links**: [[Bonded Commitment as Reputation Bootstrap]], [[Enforceable Software Contracts]]

**Garden connection**: Connects to [[Allen (2022) Progressive Trust]] — progressive trust builds through graduated interactions, but bonded commitment provides an alternative path: trust established through verifiable stake rather than accumulated history.

---

### Price as What-To-Do Signal

**Target form**: [[Gloss Form]]
**Inference level**: [source: direct quote from Hayek via the paper]

The paper quotes Hayek: "the chief guidance which prices offer is not so much how to act, but *what to do*." Applied to computation: price signals do not tell software how hard to work (that is the "incentives make software sweat" misconception). They tell software which actions create value and which destroy it. An object that ensures output price exceeds input costs is producing value as judged by the system as a whole.

**Ghost links**: [[Price Signals as Action Guidance Not Effort Incentives]]

---

### Round-Robin Scheduler as Tragedy of the Commons

**Target form**: [[Gloss Form]]
**Inference level**: [source: direct from paper text]

A round-robin scheduler treats the processor as a commons: the processing power allocated to any process decreases whenever another process spawns. Miller and Drexler identify this as a classic tragedy of the commons, with the standard Hardin solution: privatization through resource encapsulation.

**Ghost links**: [[Round-Robin Scheduling as Computational Commons Problem]]

**Garden connection**: The estate explicitly addresses commons problems through Ostrom-style governance rather than pure privatization, following [[Allen (2015) Ostrom's Design Principles for Collective Governance]]. Miller and Drexler's 1988 framing is pure privatization; Ostrom's alternative (published one year later in 1990) shows a third path between commons tragedy and privatization.

---

### Intelligence Without Individuality or Consciousness

**Target form**: [[Model Form]]
**Inference level**: [source: direct from paper text]

Miller and Drexler propose that intelligence can be separated from individuality, consciousness, and will. A society demonstrates intelligence by achieving a range of goals through complex information processing, even though the society has no individual consciousness or unified goals. Intelligence is measured by the *range* of goals achievable, the *speed* of achievement, and the *efficiency* of means employed.

This definition applies equally to individuals, corporations, ad-hoc supplier networks, and computational market ecosystems. "The idea of intelligence may thus be separated from the ideas of individuality, consciousness, and will."

**Ghost links**: [[Distributed Intelligence Without Unified Agency]], [[Intelligence as Goal-Achievement Capacity]]

**Garden connection**: This directly informs [[Human Authority Over Augmentation Systems]]. If a multi-agent system can exhibit intelligence without any single agent being conscious or having unified goals, then the question of authority becomes structural, not metaphysical. Authority does not flow from intelligence but from the principal-agent relationship — the human sets the goals and provides the resources, the system achieves them.

---

### Charge-Per-Use vs. Charge-Per-Copy

**Target form**: [[Model Form]]
**Inference level**: [source: direct from paper text]

The paper identifies charge-per-copy as a structural barrier to software composition. When building a program from five components, the licensing cost sums pathologically — the composite costs at least as much as all components together. Charge-per-use eliminates this barrier: occasional users pay proportionally less, high-volume users face marginal pricing that guides efficient use, and software creators earn proportionally to the value provided. Switching costs drop because users pay nothing to stop using one product and start using another.

**Ghost links**: [[Charge-Per-Use as Composition Enabler]]

---

### Pareto-Preferred Compilation

**Target form**: [[Gloss Form]]
**Inference level**: [source: direct from paper text]

A compiler that optimizes composed objects while guaranteeing that every component is at least as well off as before compilation. Compilation typically "violates" modularity boundaries — combining separate objects into non-modular optimized code. In an agoric system, the compiler also compiles out the overhead of runtime accounting. The resulting savings produce a larger total income to divide, enabling a Pareto improvement where some components are better off and none are worse off.

**Ghost links**: [[Pareto-Preferred Compilation]]

---

## Cross-Cutting Themes

### From 1988 to Object-Capabilities

The paper contains the intellectual seed of Miller's later object-capability work, though the term "object-capability" does not appear. The three rules for obtaining access (born with it, received in a message, created the object) are exactly the rules of object-capability discipline. The argument about security resting on inabilities is the foundation of least authority. The connection between encapsulation and property rights is the economic argument for why capabilities matter.

Reading Miller's 1988 and 2006 works together reveals a 18-year intellectual arc: the 1988 paper provides the economic vision; the 2006 dissertation provides the formal model for making that vision safe.

**Ghost links**: [[Miller (2006) Robust Composition]], [[Object-Capability Model as Market Foundation]]

### The Hayek-to-Computation Pipeline

The paper is the most direct importation of Hayekian economics into computer science. Six Hayek quotes structure the argument. The knowledge problem (no central planner can possess all relevant information), spontaneous order (coherent systems emerging from rule-governed local interaction), and the price mechanism (summarizing distributed knowledge into local signals) all transfer directly.

This pipeline — Hayek to Miller/Drexler to object-capabilities to smart contracts — is a significant intellectual genealogy for the field of decentralized systems.

**Ghost links**: [[Hayekian Knowledge Problem in Computation]], [[Spontaneous Order in Software Systems]]

### Limits of the Market Analogy

The paper acknowledges "fundamental differences between computational and human markets" (Section 1) but treats these as reasons for optimism: computational systems can enforce rules as genuine constraints (not just penalties), information does not deplete, and labor forces can be replicated instantly. The paper does not fully explore the possibility that these differences might make market mechanisms *less* appropriate in some computational contexts — for example, when the marginal cost of replication is zero, price signals carry different information than in markets for scarce physical goods.

**Ghost links**: [[Limits of Market Mechanisms in Zero-Marginal-Cost Systems]]
