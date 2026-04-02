---
created: 2026-04-02
part_of: "[[Miller (2019) Architectures of Robust Openness]]"
role: analysis
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- part_of::[[Miller (2019) Architectures of Robust Openness]]

# Miller (2019) Architectures of Robust Openness — Analysis

## The Central Problem: Safety vs. Openness

Miller frames the talk around a tension that existing systems handle badly: how to build social systems that are simultaneously robust against attacks and open to strangers. This is not a new problem -- physical societies solved it incrementally over centuries through institutions, norms, and property rights. But digital systems face it in a compressed form because the cost of attack scales differently online than offline. Physical junk mail costs the attacker proportionally to scale; email spam does not. The asymmetry between attack cost and defense cost is the structural driver of the problem.

The talk's contribution is to show that object capabilities provide a foundation for resolving this tension, and that a specific protocol layer -- Horton -- can be added on top of capabilities to provide accountability without sacrificing the safety properties that capabilities offer.

## Object Capabilities as the Foundation Layer

Miller recapitulates the object-capability model from his earlier work (the 2006 dissertation and the 2005 "Structure of Authority" paper) but positions it for an audience of federated social network developers. The core claim remains: in a capability system, only connectivity begets connectivity. Two parties with no reference path between them cannot affect each other. Authority is conferred through reference passing, not ambient context.

Miller grounds this with a precise diagram walkthrough: objects A, B, and C are circles; thin arrows are unforgeable references in a memory-safe language. When A sends `B.foo(C)`, A exercises its permission to invoke B and simultaneously grants B permission to invoke C by passing a copy of its pointer. "The main difference between objects and object capabilities is that these messages sent on these references are the *only* means by which an object can cause effects on the world outside of itself." The reference graph *is* the permission system.

For the ActivityPub audience, this maps directly to the problem of social network trust. Current social networks either rely on identity-based access control (centralized, vulnerable to censorship, but allowing reactive damage control) or on open protocols (decentralized, but vulnerable to spam and abuse). Miller argues that object capabilities occupy a third position: decentralized authority that is proactively safe because authority can only propagate through explicit introduction.

### The Car Key Analogy

Miller uses a recurring physical analogy: the car key. A physical key simultaneously designates a particular car, provides the means to operate it, and confers the right to operate it. It can be handed to another person without involving any central authority. It can be revoked by changing the locks. It does not require the recipient to prove their identity -- possession is sufficient. This is the capability model in miniature: designation, access, and authority bundled into a single unforgeable token, transferable through direct handoff.

The analogy also illustrates the limitation Miller's talk addresses. A car key provides proactive safety (only holders can drive) but not accountability (if someone drives badly, the key alone doesn't tell you who). Identity-based systems provide accountability but at the cost of centralization. Miller's argument is that you can add accountability to capabilities without losing the proactive safety properties.

## Identity vs. Authorization: Two Incompatible Defaults

Miller draws a sharp distinction between identity-based and authorization-based approaches to security, framing them as architecturally incompatible starting points rather than complementary tools.

**Identity-based systems (Access Control Lists)** start with naming: who is this entity? What permissions are associated with that name? This enables reactive security -- after something goes wrong, you can trace back to the named entity and impose consequences. But identity-based systems are inherently centralizable: someone must maintain the mapping from names to permissions, and that entity becomes a point of censorship and control. The identity layer also creates ambient authority: any program running as a named user inherits all that user's permissions.

**Object capabilities** start with authorization: what can this entity do with the references it holds? No naming is required. This enables proactive security -- unauthorized actions are structurally impossible because there is no reference through which to perform them. But pure capability systems are anonymous: the system knows that a valid capability was exercised but not necessarily by whom. This makes reactive measures (banning, accountability, reputation) difficult.

Miller presents three logical approaches to combining these strengths and argues that only one works:

1. **Start with ACL foundations, add capability benefits.** Systems like Polaris, Plash, and BitFrost used ACL mechanisms in surprising ways to support least-authority patterns. Miller acknowledges these are "interesting and worth studying" but says they "don't compose well" and "only help one more level deep, and then they stop helping."

2. **Hybrid foundations with both mechanisms.** 1970s-80s systems included both capability and ACL mechanisms, allowing an action only if both rule sets permitted it. Miller says this "intuitively obvious approach" gave "the worst of both worlds" under composition rather than the best.

3. **Start with pure capabilities, build accountability through patterns.** This is Horton: use object capability patterns themselves to construct identity-based accountability, without modifying the capability foundations.

Miller's conclusion is that the architectural foundations are incompatible as peers. Building accountability on top of capabilities works; building capabilities on top of identity does not compose.

## The Intermediation Spectrum

A distinctive contribution of this talk is Miller's taxonomy of intermediation patterns for building trust between strangers. He presents four levels, each adding accountability at the cost of additional structure.

### Two-Party Intermediation

Both sender and receiver independently log their interactions. Neither trusts the other's log, but both maintain their own record. SCoopFS (a capability-secure cooperative filesystem) exemplifies this: each party has an independent record of what happened. Accountability is bilateral but limited -- disputes reduce to "my log says X, yours says Y" with no tiebreaker.

### Three-Party Intermediation

A third party vouches for both participants. Miller grounds this with a personal anecdote: "Something amazing happened this morning -- somebody that I've never met before showed up in a car that I've never seen before and I got into that car." The Uber platform, in the role of Alice, communicates enough information to both Bob (driver) and Carol (rider) that they can authenticate each other -- not by knowing who the other person *is*, but by verifying "Is this the Bob that Uber meant to introduce me to?" The third party need not be trusted by both sides for the same reasons, but its independence is questionable.

### Four-Party Intermediation

Multiple independent attestors vouch for participants through separate channels. Miller uses Secure Scuttlebutt as an example: identity verification happens through multiple independent social connections rather than through a single authority. The "name integrity" property -- that a name consistently refers to the same entity -- emerges from corroborated attestation rather than centralized assignment. This resists censorship because no single entity controls the mapping.

### The Horton Layer: Accountability for Capabilities

Horton is the technical contribution that bridges capability-based authority with identity-based accountability. Named after the Dr. Seuss character ("a person's a person, no matter how small"), Horton adds a "whodunnit" layer on top of object capabilities. The protocol holds participants accountable for three types of actions:

1. **Requests**: who initiated this action?
2. **Responses**: who performed this service?
3. **Introductions**: who connected these parties?

Horton achieves this without modifying the underlying capability system. It is interposed between existing capability-based application objects as a protocol layer. Miller describes the mechanism in detail: when object A (run by Alice) sends a message to object B (run by Bob), the message first passes through Alice's *outgoing sentry*, which checks "Do I still make use of Bob's services?" and records the request. The message then goes to Bob's *incoming sentry*, which checks "Do I still honor Alice's requests?" and records that the message is being delivered on behalf of Alice. Only after both sentries have logged the interaction does the message reach object B. Miller calls this pair of sentries an "identity tunnel" and uses the graphic as shorthand throughout the rest of the talk.

The key property: Horton enables delegation of responsibility, not just delegation of authority. In Miller's framing from the 2007 paper with Donnelley and Karp, existing capability systems support delegating authority (Alice gives Bob the car key), and existing identity systems support assigning responsibility (the DMV records who owns the car), but no system combined both -- delegating authority coupled with assigning responsibility for how that authority is used.

## Openness Without Spam: The Remaining Problem

Miller acknowledges a hard remaining problem: pure capability systems struggle to welcome strangers. "Only connectivity begets connectivity" means that someone outside the existing reference graph has no way to reach anyone inside it. This is a feature for security but a failure for openness. A social network that cannot accept new participants is not a social network.

Publicly open inboxes -- the standard solution -- reintroduce the spam problem. Miller cites PetMail, a prior decentralized federated social network that used pet names, corroboration, and open public inboxes for cold calling, but attached a per-message cost via CAPTCHAs. He then acknowledges directly: "Given the state of artificial intelligence, we should certainly assume that CAPTCHAs cannot continue to work, and pretty much they don't work already." He favors monetary stamps -- "The nice thing about stamps, about money transfer, is it also compensates the victim" -- but does not present a complete implementation.

The talk's honest framing: the object capability model provides strong foundations for safety within an existing trust network, and Horton adds accountability for delegation within that network, but the cold-start problem of establishing initial trust with complete strangers remains an open research question.

## Relevance to Federated Social Networks

The ActivityPub context is not incidental. Miller argues that federated protocols face the safety-openness tension more acutely than centralized platforms because there is no single operator who can impose reactive measures globally. A centralized platform can ban a bad actor across the entire network; a federated network cannot. This makes proactive safety (the capability model's strength) more valuable in federated contexts, and it makes the Horton layer's accountability properties more important -- because accountability in a federated system must work without a global authority.

The talk implicitly argues that ActivityPub's current model (server-to-server federation with instance-level blocking) is architecturally closer to ACL-based security than to capability-based security, and that adopting capability patterns would provide stronger proactive safety guarantees while maintaining federation's censorship resistance.

## Relationship to Miller's Earlier Work

This talk synthesizes and extends concepts from Miller's prior publications:

- The **object-capability model** from the 2006 dissertation ("Robust Composition") provides the foundational layer
- The **Principle of Least Authority** from the 2005 paper with Tulloh and Shapiro ("The Structure of Authority") informs the design of minimal authority grants
- The **Horton protocol** from the 2007 HotSec paper with Donnelley and Karp provides the accountability layer
- The **Granovetter diagram** (Miller's adaptation of social network topology analysis to capability reference graphs) underlies the "only connectivity begets connectivity" principle

What is new in this 2019 presentation is the synthesis of these elements into a unified architecture for social systems, presented to an audience building federated social protocols. Miller connects his longstanding security research to the concrete problem of building abuse-resistant, censorship-resistant social infrastructure.

## Limitations

**The cold-start problem remains unresolved.** Miller acknowledges that pure object capability systems cannot welcome strangers, but the talk does not present a complete solution. The Horton layer addresses accountability for existing connections, not bootstrapping new ones.

**Practical adoption gap.** The talk does not address the practical challenge of retrofitting capability patterns onto ActivityPub's existing HTTP-based server federation model. Whether the theoretical architecture maps cleanly onto real protocol engineering is an open question.

**77-minute talk, broad scope.** Miller covers decades of capability security research compressed into a single keynote. Some arguments are necessarily compressed, and the depth of treatment varies across sections.

## Sources

- Transcript: [[Miller (2019) Architectures of Robust Openness — Transcript]]
- Primary: Miller, Mark S. "Architectures of Robust Openness." Keynote, ActivityPub Conference 2019, Prague, September 2019. YouTube (Agoric channel): <https://www.youtube.com/watch?v=NAfjEnu6R2g>
- Mirror: Internet Archive: <https://archive.org/details/apconf-mark>
- Mirror: ConfTube: <https://conf.tube/w/g87k3yKzYwpGhtohvQdC3k>
- Secondary summary: zwilnik.com notes on the talk: <https://www.zwilnik.com/better-social-media/activitypub-conference-2019/architectures-of-robust-openness/>
- Pre-talk context: dustycloud.org announcement: <https://dustycloud.org/blog/mark-miller-at-apconf-2019/>
- Horton paper: Miller, Donnelley, Karp. "Delegating Responsibility in Digital Systems: Horton's 'Who Done It?'" HotSec 2007. <https://www.usenix.org/legacy/events/hotsec07/tech/full_papers/miller/miller_html/index.html>
- Foundation: Miller (2006) "Robust Composition" dissertation. <http://www.erights.org/talks/thesis/markm-thesis.pdf>
- Foundation: Miller, Tulloh, Shapiro (2005) "The Structure of Authority." MOZ 2004 proceedings.
