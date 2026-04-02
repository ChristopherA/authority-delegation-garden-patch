---
created: 2026-04-02
part_of: "[[Miller & Drexler (1988) Markets and Computation]]"
role: analysis
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- part_of::[[Miller & Drexler (1988) Markets and Computation]]

# Miller & Drexler (1988) Markets and Computation — Analysis

## Core Thesis

Miller and Drexler argue that market mechanisms — price signals, property rights, trade, and decentralized decision-making — should be imported wholesale into the computational domain. Their claim rests on a structural parallel: both societies and software systems face the problem of coordinating action among diverse entities with distributed knowledge and limited resources. If markets solve this coordination problem in human economies, the same mechanisms can solve analogous problems in software systems.

The paper does not merely propose markets as a metaphor for computation. It proposes markets as an actual operating mechanism: objects charge each other for services, pay rent for memory, bid for processor time, and earn royalties for their creators. Currency circulates within the system, generating price information that guides resource allocation decisions.

## Argument Structure

The paper follows a levels-of-analysis approach, moving from foundations through agents to emergent system properties:

1. **Foundational level** (Section 4): What computational properties must exist for markets to function? Encapsulation of information, access, and resources — corresponding to property rights in human systems.
2. **Agent level** (Section 5): How do individual objects participate in markets? Through delegation to business agents that handle negotiations, reputation assessment, and resource allocation.
3. **Emergent level** (Section 6): What happens when a large system of market-interacting objects evolves? A software distribution marketplace with charge-per-use economics and emergent intelligence from multi-agent interaction.

This levels structure is itself an argument: markets are not bolted on top of computation but arise naturally from the same encapsulation principles that object-oriented programming already provides.

## Named Patterns

### Encapsulation-as-Property-Rights

Miller and Drexler identify a direct structural correspondence between object encapsulation in software and property rights in law. Both establish "protected spheres in which entities can plan the use of their resources free of interference from unpredictable external influences." This is not an analogy — it is a claim about shared function. Object-oriented programming reinvented property rights without recognizing it had done so.

The significance: if encapsulation already provides property rights for information and access (the competence domain), extending encapsulation to computational resources (the performance domain) is a natural next step. This extension gives objects ownership of processor time and memory, enabling trade.

### Capability Security as Market Foundation

The paper identifies capability security as the necessary access-control mechanism for computational markets. An object can obtain access to another only by: (1) being born with it, (2) receiving it in a message, or (3) being the creator of the accessed object. This is equivalent to the "object-capability model" that Miller later formalized in his 2006 dissertation on robust composition.

The argument about Turing-equivalence and security is striking: Turing-equivalence describes what a system *can* do, but security rests on what a system *cannot* do. Adding interpreters cannot subtract abilities, so an insecure foundation cannot be made secure by layering. Security must be built into the computational substrate.

### The Firm Analogy (Computational Coase)

Drawing on Ronald Coase's theory of the firm, Miller and Drexler explain why computational markets will not be uniformly fine-grained. Transaction costs — advertising, negotiation, accounting — make market mechanisms expensive for small interactions. Objects will aggregate into "firms" with internal command structures, participating in markets only at boundaries where transactions are large enough to justify the overhead.

This provides a principled answer to the question "at what granularity should market mechanisms apply?" The answer is: wherever the benefits of flexible, price-sensitive tradeoffs exceed the overhead of accounting and negotiation. Market competition itself tunes this boundary.

### Business Agent Delegation

Simple objects in a complex market survive by delegating performance-domain decisions to business agents, just as competence-domain decisions are delegated to subcontractors. This separation of competence from performance is a design pattern: an object can be simple in what it does (competence) while being sophisticated in how it manages resources (performance), because the sophistication lives in shared agents.

Data-type agents illustrate the pattern concretely. A lookup table agent knows which implementations exist (array, hash table, B-tree), what tradeoffs each embodies, and how to monitor usage patterns and switch implementations transparently. The agent can respond to price changes — if memory becomes expensive relative to processor time, it switches to a more compact representation.

### Positive Reputation Systems

The paper distinguishes positive and negative reputation systems. Negative systems (avoiding bad actors) fail when pseudonyms are cheap. Positive systems (seeking known-good actors) require only that one entity cannot claim another's identity — a condition met by capability-based identity. New objects establish positive reputations through cash bonds guaranteeing performance, enforced by trusted third parties. This mechanism enables software entities to make credible commitments.

### Spontaneous Order Through Price Signals

Prices summarize global information about relative values into a local signal. An object need only ensure its output price exceeds its input costs to create value as judged by the system as a whole. The paper explicitly invokes Hayek's insight that the price mechanism tells agents not just how hard to work, but *what to do*.

This is the mechanism by which coherent global behavior emerges from local decisions — the computational analog of the "invisible hand."

## Second-Order Analysis

### What the Paper Gets Right About Its Own Future

Miller and Drexler's 1988 predictions about system scale have been validated beyond their own projections. The paper anticipated "millions of personal computers linked by networks" — the actual internet exceeded this by orders of magnitude. Their prediction that "computers are becoming too complex for central planning" describes cloud computing and microservice architectures exactly.

The paper's prediction of charge-per-use software markets anticipated the software-as-a-service model that became dominant by the 2010s, though through subscription rather than per-invocation pricing.

### What the Paper Does Not Address

**Power concentration.** The paper assumes that market mechanisms naturally distribute power through competition. It does not address the tendency of computational markets to concentrate into monopolies or oligopolies, which has been the actual trajectory of software markets. Platform effects, network externalities, and data advantages create winner-take-all dynamics that markets alone do not correct.

**The principal problem.** The paper treats objects as agents acting on their own behalf or on behalf of clearly defined owners. It does not address the question of who the principal is in a complex delegation chain. When an object delegates to an agent that delegates to a sub-agent, whose interests are served? Miller addressed this directly in his 2005 paper with Tulloh and Shapiro on the structure of authority, and in his 2006 dissertation on robust composition.

**Governance of the commons.** The paper mentions Hardin's tragedy of the commons (the round-robin scheduler as a commons) but does not engage with Ostrom's later work on commons governance. The paper's solution to commons problems is privatization (encapsulation of resources), but many computational resources are better modeled as commons than as private property.

**Opportunism in practice.** Appendix II discusses Malone's assumption that computational agents can be made non-opportunistic, and correctly notes that in open systems, programmers will have opportunistic motives. But the paper does not fully develop how market mechanisms handle adversarial agents beyond reputation systems.

### The Seed of Object-Capabilities

This paper contains the earliest published articulation of ideas that became Miller's object-capability model. The three rules for obtaining access (born with it, received in a message, or created the object) are precisely the rules of object-capability discipline. The argument about security resting on *inabilities* rather than abilities foreshadows the principle of least authority. The connection between encapsulation and property rights provides the economic grounding for why capability discipline matters.

Reading the paper with knowledge of Miller's later work reveals a continuous intellectual thread: capability security enables property rights, property rights enable markets, markets enable coordination without central planning, and the whole system preserves the ability of local entities to make decisions based on local knowledge.

### The Hayek Connection

The paper draws extensively on Friedrich Hayek's work on spontaneous order, the knowledge problem, and price mechanisms. The acknowledgments list Hayek as a primary intellectual inspiration. This is significant because Hayek's argument was about the impossibility of central planning when knowledge is distributed — the same argument Miller and Drexler make about computational systems.

The paper quotes Hayek six times, more than any other source. The Hayekian framework provides the theoretical backbone: prices aggregate distributed knowledge, central planning fails because no single mind can possess all relevant information, and spontaneous order emerges from rule-governed interaction among self-interested agents.

### Conway's Law Inverted

The paper invokes Conway's law — organizations produce systems that mirror their communication structures — to argue that decentralized societies should produce decentralized software. This is the reverse of the usual application. Rather than designing organizations to produce desired software structures, Miller and Drexler propose designing software structures that mirror the decentralized organization of markets.

## Structural Observations

The paper covers an enormous range — from processor scheduling to artificial intelligence — in roughly 15,000 words. This breadth comes at a cost: many claims are sketched rather than developed. The companion paper on "Incentive Engineering" (referenced as [III]) handles the detailed economic analysis; this paper provides the vision.

The paper's structure mirrors its argument: it moves from centralized (a single introduction) through intermediate (increasingly autonomous agents) to decentralized (emergent system properties). The appendices handle cross-cutting concerns (levels and scale) and situate the work relative to prior art. The acknowledgments list is a who's-who of 1980s computer science and economics: Minsky, Hewitt, McCarthy, Milton Friedman, David Friedman.

The publication context matters: this appeared in *The Ecology of Computation* (Bernardo Huberman, editor), a 1988 volume that also included papers by Malone, Stefik, Hewitt, and others working on distributed and multi-agent systems. The volume represented a moment when computer science was seriously engaging with economic and ecological metaphors for computation.
