---
created: 2026-04-02
part_of: "[[Miller (2019) Architectures of Robust Openness]]"
role: insights
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- part_of::[[Miller (2019) Architectures of Robust Openness]]

# Miller (2019) Architectures of Robust Openness — Insights

## Insight 1: Accountability as a Layer, Not an Alternative

Miller's architecture places accountability (Horton) on top of capability-based authority rather than replacing it with identity-based access control. This layering is load-bearing for the garden's agentic architecture domain. The garden principle [[Authority Flows from the Person]] asserts that authority originates with the human principal and flows through delegation. Miller's design makes this concrete: the capability layer ensures that authority flows only through explicit reference passing, and the Horton layer ensures that each exercise of delegated authority is attributable to a specific actor.

This directly addresses a gap in the garden's current treatment of [[Human Authority Over Augmentation Systems]]. That principle establishes that humans must retain authority over AI agents, but does not specify a mechanism for tracking what agents do with delegated authority. Horton's three-part accountability model (requests, responses, introductions) provides one: each agent action is attributable, each delegation is traceable, and each introduction (connecting two agents, or an agent to a resource) is recorded.

**Ghost link**: [[Accountability Layer for Delegated Authority]] -- a potential Pattern Form node describing the architectural principle that accountability should be layered on top of authorization rather than replacing it. [source: garden-level inference from Miller's architecture mapped to existing garden principles]

## Insight 2: The Intermediation Spectrum as Design Space

Miller's four-level intermediation taxonomy (two-party, three-party, four-party, Horton) is not just a description of existing systems but a design space for trust architectures. Each level trades structural complexity for stronger accountability guarantees. This maps to a design choice that the garden's agentic architecture must make: how much intermediation does a personal knowledge estate need between the human principal and the agents operating on their behalf?

Current estate design uses direct delegation (the orchestrator commissions workers) without a formal accountability layer. Miller's spectrum suggests this is two-party intermediation at best: the orchestrator and worker each maintain their own logs, but there is no protocol-level accountability for how delegated authority was used. Adding Horton-style accountability would mean that when the Groundskeeper commissions a Forager, the commission itself carries accountability metadata: who requested the work, who performed it, and who introduced the Forager to the source material.

**Ghost link**: [[Intermediation Patterns for Agent Delegation]] -- a potential Model Form node mapping Miller's intermediation levels to multi-agent system designs. [source: analysis-level inference connecting Miller's taxonomy to estate architecture]

## Insight 3: "Only Connectivity Begets Connectivity" as an Architectural Invariant

This phrase, which Miller traces back through the Granovetter diagram to social network theory, is the object-capability model's central security invariant. In capability terms: two objects with no reference path between them cannot affect each other. New connections form only through introduction by an existing connected party.

For the garden, this invariant has direct implications for how agent authority is scoped. An agent that is not given a reference to a resource cannot access that resource -- regardless of what other agents can access. This is the formal expression of what [[Principle of Least Authority]] requires: authority is not ambient but positional, determined by the topology of reference relationships.

The garden's existing treatment of POLA (through the Miller 2006 and Miller et al. 2005 citations) discusses this principle in terms of software components. This talk extends it to social systems: the same invariant that protects software modules from unauthorized access also protects social network participants from unwanted contact. The extension matters for agentic architecture because agents operate in both technical and social domains -- they access resources (technical) and interact with humans and other agents (social).

**Ghost link**: [[Connectivity Begets Connectivity]] -- a potential Principle Form node stating the invariant and its implications across technical and social domains. [source: direct from Miller's talk, extending existing garden principle treatment]

## Insight 4: The Cold-Start Problem as Honest Limitation

Miller's acknowledgment that capability systems cannot welcome strangers -- that publicly open inboxes reintroduce spam -- is notable for its honesty. Most capability advocates present the model as a complete solution. Miller identifies the boundary of what capabilities can and cannot do: strong proactive safety within an existing trust network, but no inherent mechanism for bootstrapping trust with unknown parties.

This maps to a known gap in the garden's agentic architecture. The estate currently assumes a closed system: the human principal delegates to known agents. But research tasks require agents to interact with external sources, APIs, and potentially other agents outside the estate boundary. Miller's cold-start problem applies: how does an agent establish initial trust with an external service that is not part of the existing capability graph?

Allen (2022) "Progressive Trust" addresses this gap in the identity domain -- trust is earned incrementally through interaction. Miller's talk suggests that the capability domain needs an analogous mechanism: a way to extend minimal, revocable capabilities to untrusted parties as a first step in building a trust relationship.

**Ghost link**: [[Cold-Start Trust in Capability Systems]] -- a potential Inquiry Form node exploring how capability-based systems bootstrap trust with unknown parties, connecting Miller's identified gap to Allen's Progressive Trust framework. [source: garden-level inference connecting Miller's limitation acknowledgment to Allen's work]

## Insight 5: Federated Systems Need Proactive Safety More Than Centralized Ones

Miller's argument that federated protocols face the safety-openness tension more acutely than centralized platforms has implications beyond social networks. A centralized platform can impose reactive measures (banning, content removal) globally. A federated system cannot. This makes proactive safety -- structural prevention of unauthorized actions rather than after-the-fact punishment -- the primary defense mechanism for federated architectures.

The garden's estate model is structurally federated: multiple agents with separate worktrees, operating on the same knowledge base but without a single point of control. The human principal is the coordinating authority, but they are not always present during agent operations. This means the estate needs proactive safety guarantees (capability-based authority scoping) more than reactive ones (post-hoc audit and correction). Miller's argument for federated social networks applies with equal force to multi-agent knowledge estates.

**Ghost link**: [[Proactive Safety in Federated Agent Systems]] -- a potential Pattern Form node describing why federated multi-agent systems should prefer capability-based proactive safety over identity-based reactive safety. [source: analysis-level inference from Miller's federated systems argument applied to estate architecture]

## Insight 6: Delegation of Responsibility vs. Delegation of Authority

The Horton protocol's distinction between delegating authority and delegating responsibility is a concept the garden does not yet have a dedicated node for. Existing capability systems let Alice give Bob the car key (authority delegation). Existing identity systems let the DMV record that Alice owns the car (responsibility assignment). Horton combines both: Alice gives Bob the car key AND Bob becomes accountable for how he uses it.

In the estate context, the orchestrator-worker pattern involves both. The Groundskeeper delegates authority to the Forager (commission with specific capabilities) and assigns responsibility (the commission specifies deliverables and boundaries). But the mechanism for enforcing that responsibility -- for holding the Forager accountable for how delegated authority was used -- is currently informal (session logs, commission returns). Horton suggests a more formal protocol layer could make this accountability structural rather than procedural.

**Ghost link**: [[Delegation of Responsibility]] -- a potential Gloss Form node defining the concept and distinguishing it from delegation of authority. [source: direct from Miller and the 2007 Horton paper]

## Insight 7: Granovetter Diagram as Cross-Domain Tool

Miller's adaptation of the Granovetter diagram -- originally a sociological tool for analyzing how interpersonal connections change through introductions -- to object-capability analysis is itself a methodology insight. The same topological notation describes both human social networks and computational reference graphs. This dual applicability supports the garden's treatment of authority as a concept that spans human and technical domains.

The existing garden nodes [[Topology Determines Authority]] and [[Authority Flows from the Person]] both make claims about the structure of authority relationships. Miller's Granovetter diagram provides a visual and analytical tool for testing those claims: if you can draw the reference graph and trace who introduced whom, you can determine what authority each participant holds and how they acquired it.

**Ghost link**: [[Granovetter Diagram as Authority Analysis Tool]] -- a potential Model Form node describing how the Granovetter diagram applies to both social and computational authority analysis. [source: direct from Miller's work, connecting to existing garden topology principles]

## Insight 8: The Unit of Responsibility Is Not the Object

Miller makes a precise distinction that secondary sources compressed: the granularity of *permission* (fine-grained, at the object level) must be separated from the granularity of *responsibility* (coarse-grained, at the human/organization level). Objects are ephemeral — "by the time somebody looks at what happened... there is no object A anymore. Object A has already gone away." Attributing abuse to an ephemeral object is pointless. But the person running those objects persists and can be held accountable.

This separation is architecturally load-bearing. Miller defines the "unit of responsibility" as Alice-the-human *plus* Alice's software *plus* Alice's local user interface — the entire sphere. If Bob receives abusive messages from Alice's sphere, "Bob doesn't need to know or care whether these abusive messages are coming because Alice is running malware or because Alice has turned evil." The accountability is at the sphere level regardless of internal cause.

For estate architecture, this maps to the question of agent accountability scope. When a Forager produces bad citations, is the Forager accountable, or the Groundskeeper who commissioned it? Miller's answer: the Groundskeeper's sphere, because that's the unit Bob (the human reviewer) can meaningfully hold responsible.

**Ghost link**: [[Responsibility Sphere]] -- a potential Gloss Form node defining Miller's concept of the coarse-grained unit that persists long enough to be held accountable. [source: verbatim from transcript, not captured in secondary sources]

## Insight 9: Bitcoin as Naming Integrity Proof-of-Concept

Miller uses Bitcoin not as a financial example but as an existence proof that impersonation resistance and censorship resistance can coexist in a decentralized system. A Bitcoin account is keyed to a public key; the holder knows the private key. No one else can generate a matching private key (impersonation resistance). No one can stop you from spending (censorship resistance). "When you cross a border, no matter what the capital controls are, if you've memorized your keys... you can still cross and no one can stop you from taking your wealth with you."

Miller then applies the same two properties to communication: "We want the same kind of security and decentralization for our knowledge and ability to communicate with each other." This is a stronger claim than secondary sources reported — Miller is not merely analogizing, he is asserting that the cryptographic primitives that solved the double-spending problem also solve the naming integrity problem for social networks.

**Ghost link**: [[Cryptographic Naming Integrity]] -- a potential Gloss Form node on using public-key cryptography to achieve both impersonation resistance and censorship resistance for human-meaningful names. [source: verbatim from transcript]

## Sources

- Transcript: [[Miller (2019) Architectures of Robust Openness — Transcript]]
- Primary: Miller (2019) "Architectures of Robust Openness" keynote. YouTube: <https://www.youtube.com/watch?v=NAfjEnu6R2g>
- Secondary: zwilnik.com talk notes. <https://www.zwilnik.com/better-social-media/activitypub-conference-2019/architectures-of-robust-openness/>
- Horton paper: Miller, Donnelley, Karp (2007). <https://www.usenix.org/legacy/events/hotsec07/tech/full_papers/miller/miller_html/index.html>
- Garden context: [[Miller (2006) Robust Composition]], [[Miller, Tulloh & Shapiro (2005) The Structure of Authority]], [[Allen (2023) Least and Necessary Design Patterns]], [[Allen (2022) Progressive Trust]], [[Human Authority Over Augmentation Systems]], [[Authority Flows from the Person]], [[Principle of Least Authority]]
