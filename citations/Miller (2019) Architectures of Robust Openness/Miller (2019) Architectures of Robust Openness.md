---
created: 2026-04-02
author: Christopher Allen
citation_slug: miller-2019-architectures-of-robust-openness
publication_year: 2019
canonical: https://www.youtube.com/watch?v=NAfjEnu6R2g
brief_summary: "Miller's keynote at ActivityPub Conference 2019 applies the object-capability model to federated social systems. He presents a four-level intermediation taxonomy for building trust between strangers, introduces the Horton protocol for adding accountability to capability-based authority, and argues that federated systems need proactive safety guarantees more than centralized ones. 77 minutes."
tagline: "How to build social systems that are both robust against attacks and open to strangers"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Mark S. Miller]]

# Miller (2019) Architectures of Robust Openness

## Bibliographic Entry

* _**Architectures of Robust Openness**_ (2019). [video/talk]. _Miller, Mark S._ Keynote, ActivityPub Conference 2019, Prague, September 2019. Agoric, YouTube. Retrieved 2026-04-02 from: <https://www.youtube.com/watch?v=NAfjEnu6R2g>

## Summary

Miller addresses a central tension in decentralized systems: how to maintain safety while remaining open to strangers. He recapitulates the object-capability model (only connectivity begets connectivity), then builds beyond it with the Horton protocol, which adds accountability for requests, responses, and introductions without modifying the underlying capability system. He presents a four-level intermediation taxonomy -- from bilateral logging through three-party vouching to multi-attestor corroboration -- as a design space for trust architectures. The talk is honest about remaining problems: pure capability systems cannot welcome strangers, and the cold-start trust problem remains open.

## Key Points

**Safety and openness are architecturally opposed defaults.** Centralized identity-based systems (Access Control Lists) enable reactive safety through naming and permission revocation but are vulnerable to censorship. Object capabilities enable proactive safety through reference-graph scoping but are inherently anonymous. Miller argues these are incompatible starting points, not complementary tools -- you must choose a foundation and layer the other on top.

**Only connectivity begets connectivity.** The object-capability model's central invariant: two objects with no reference path between them cannot affect each other. New authority enters the system only through introduction (an existing participant passes a reference), parenthood (a creator holds the sole initial reference), endowment (a creator shares its own references), or initial conditions. This invariant makes security analysis tractable because the reference graph is the access graph.

**The car key analogy grounds capability intuition.** A physical key simultaneously designates a car, provides the means to operate it, and confers the right to operate it. It transfers without involving any central authority. It can be revoked by changing the locks. Possession is sufficient; identity is not required. This is the capability model in physical form -- and it illustrates both the strength (proactive safety) and the limitation (no inherent accountability) that Horton addresses.

**Four levels of intermediation form a trust design space.** Two-party: bilateral logging, no tiebreaker. Three-party: a platform vouches for both sides (Uber model), but platform independence is questionable. Four-party: multiple independent attestors achieve name integrity through corroboration (Secure Scuttlebutt model), resisting censorship. Horton: a protocol layer that holds participants accountable for requests, responses, and introductions, combining capability-based authority with identity-based responsibility.

**Horton separates authority delegation from responsibility delegation.** Existing capability systems support delegating authority (Alice gives Bob the car key). Existing identity systems support assigning responsibility (the DMV records who owns the car). Horton combines both: the car key transfers with accountability metadata so Bob becomes responsible for how he uses the authority Alice delegated. The protocol is interposed between existing capability objects without modifying either the objects or the underlying capability foundations.

**Federated systems need proactive safety more than centralized ones.** A centralized platform can impose reactive measures (banning, content removal) globally. A federated system cannot -- there is no single operator. This makes structural prevention of unauthorized actions (the capability model's strength) the primary defense mechanism for federated architectures. Miller argues this is why ActivityPub and similar protocols should adopt capability patterns rather than relying on instance-level blocking.

**The cold-start problem remains unsolved.** Pure capability systems cannot welcome strangers. "Only connectivity begets connectivity" means outsiders have no path into an existing trust network. Publicly open inboxes reintroduce spam. Cost mechanisms (CAPTCHAs, proof-of-work) are partial mitigations. Miller does not claim to solve this; he identifies the boundary of what capabilities can achieve and what requires additional mechanisms.

**The Granovetter diagram bridges social and computational analysis.** Miller adapts Mark Granovetter's sociological tool for analyzing how interpersonal introductions change network topology to the analysis of capability reference graphs. The same notation describes both human social networks and computational authority relationships, supporting cross-domain reasoning about trust and authority.

## Key Quotes

> "So today, let's talk about architectures for creating decentralized social networks that are both robust against attacks and open to strangers."

> "Object capabilities have the slogan: only connectivity begets connectivity. If you have two isolated subgraphs, they remain forever isolated because no one can introduce them."

> "What we need to do is separate the granularity at which we grant permission -- which wants to be as fine-grained as possible -- from the granularity at which we assign responsibility for bad actions."

> "The key thing about identity-based access control is all access decisions are rooted in the question, 'Who are you?' [...] The strength of this paradigm is its support for reactive damage control, but the problems make it very poor at proactively building safe arrangements."

> "A smart contracting fabric can enable those benefits at tiny costs, at incredibly tiny costs -- by eight orders of magnitude."

## Influence

This talk is Miller's only recorded presentation of the Horton protocol applied to federated social networks. It influenced the Spritely project's adoption of object capabilities for the fediverse, with the Spritely Goblins framework implementing Horton-style accountability layers. The intermediation taxonomy provided a design framework for comparing trust architectures in decentralized systems. Within the garden's Agentic Architecture domain, the talk extends the foundational capability work of Miller (2006) and Miller, Tulloh, and Shapiro (2005) into the domain of social trust and multi-party accountability -- directly relevant to how human-agent delegation should handle accountability for autonomous actions.

## Limitations

The talk covers decades of capability research in 77 minutes, necessarily compressing some arguments. The cold-start problem is identified but not resolved. The practical challenge of retrofitting capability patterns onto ActivityPub's existing HTTP-based server federation model is not addressed.

## Sources

- Primary: Miller, Mark S. "Architectures of Robust Openness." Keynote, ActivityPub Conference 2019, Prague. YouTube (Agoric channel). <https://www.youtube.com/watch?v=NAfjEnu6R2g>
- Mirror: Internet Archive. <https://archive.org/details/apconf-mark>
- Mirror: ConfTube. <https://conf.tube/w/g87k3yKzYwpGhtohvQdC3k>
- Secondary: zwilnik.com notes on the talk. <https://www.zwilnik.com/better-social-media/activitypub-conference-2019/architectures-of-robust-openness/>
- Pre-talk announcement: dustycloud.org. <https://dustycloud.org/blog/mark-miller-at-apconf-2019/>
- Horton paper: Miller, Donnelley, Karp. "Delegating Responsibility in Digital Systems: Horton's 'Who Done It?'" HotSec 2007. <https://www.usenix.org/legacy/events/hotsec07/tech/full_papers/miller/miller_html/index.html>
- Transcript: [[Miller (2019) Architectures of Robust Openness — Transcript]]
- Companion analysis and insights: [[Miller (2019) Architectures of Robust Openness — Analysis]], [[Miller (2019) Architectures of Robust Openness — Insights]]

## Relations

- relates_to::[[Miller (2006) Robust Composition]]
  - This talk recapitulates the object-capability model and POLA from Miller's dissertation and extends them to social systems -- the dissertation provides the formal foundation; this talk provides the social application

- relates_to::[[Miller, Tulloh & Shapiro (2005) The Structure of Authority]]
  - "Only connectivity begets connectivity" and the four mechanisms of authority propagation (introduction, parenthood, endowment, initial conditions) originate in the 2005 paper; this talk applies them to federated social network design

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
  - Allen traces design authority through a Saltzer/Schroeder to Miller lineage; this talk extends that lineage into social trust architecture, adding accountability (Horton) to the authority minimization (POLA) that Allen builds on

- relates_to::[[Human Authority Over Augmentation Systems]]
  - The talk operationalizes what human authority means in a multi-party system: capabilities ensure that authority flows only through explicit delegation, and Horton ensures each exercise of delegated authority is attributable

- relates_to::[[Authority Flows from the Person]]
  - Miller's "only connectivity begets connectivity" is the technical expression of this principle: authority propagates only through reference paths that trace back to deliberate grants

- relates_to::[[Mark S. Miller]]
  - Speaker; developer of the E language, co-founder of Agoric, designer of the object-capability security model

- relates_to::[[Principle of Least Authority]]
  - The talk applies POLA to social systems: just as software components should hold minimum authority, social network participants should receive minimum capability grants for each interaction

- relates_to::[[Saltzer & Schroeder (1975) The Protection of Information in Computer Systems]]
  - Miller's capability model extends the Principle of Least Privilege into the Principle of Least Authority by recognizing transitive authority; this talk further extends it into social accountability
