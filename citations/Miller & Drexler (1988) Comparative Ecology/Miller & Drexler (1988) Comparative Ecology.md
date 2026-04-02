---
created: 2026-04-01
author: Christopher Allen
citation_slug: miller-drexler-1988-comparative-ecology
publication_year: 1988
canonical: https://papers.agoric.com/papers/comparative-ecology-a-computational-perspective/full-text/
brief_summary: "Miller and Drexler compare biological ecosystems, Axelrod tournament strategies, and market systems to argue that computational 'direct markets' — where software entities earn resources and replicate based on economic performance — produce more robust evolutionary stable strategies than biological or command-based systems. Introduces agoric open systems and encapsulation-as-property-rights."
tagline: "Why computational markets out-evolve biological ecosystems — and what that means for agent design"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Mark S. Miller]]

# Miller & Drexler (1988) Comparative Ecology

## Bibliographic Entry

* _**Comparative Ecology: A Computational Perspective**_ (1988). [book chapter]. _Miller, Mark S. and Drexler, K. Eric._ In: Huberman, Bernardo A. (ed.), *The Ecology of Computation*. Elsevier/North-Holland, 1988. Physical copy in Christopher Allen's archive. Digital version: <https://papers.agoric.com/papers/comparative-ecology-a-computational-perspective/full-text/>

## Summary

Miller and Drexler compare three evolutionary systems — biological ecosystems, Axelrod's iterated prisoner's dilemma tournaments, and market economies — to identify which properties enable effective computation. Their central finding: market ecosystems encourage symbiotic strategies ("productive and wary") while biological ecosystems tend toward predation and arms races. A "direct market" in software, where successful entities directly acquire processing power and replicate with variation, avoids the parasitism problems that plague other computational evolution schemes such as Lenat's EURISKO. The paper argues that object encapsulation and public-key cryptography can enforce property rights "as physical laws," making voluntary exchange the foundation of a productive computational ecology.

## Key Points

**Direct markets solve EURISKO's parasitism problem.** Lenat's EURISKO system allowed heuristics to directly adjust their own worth without earning resources. This created parasitic feedback loops — groups of mutually rewarding heuristics that extracted resources without contributing. A conserved currency prevents this: heuristics can only gain funds from outside the group, so non-productive coalitions go broke by conservation law.

**Trade is symbiotic; predation is an arms race.** Biological ecosystems trend toward "teeth and armor" — zero-sum competition where each participant's gain comes at another's expense. Market ecosystems favor symbiotic outcomes because "trade typically increases the viability of both participants." This makes market-based computational systems more productive in aggregate than biologically modeled ones.

**The evolutionarily stable strategy shifts from "nice and retaliatory" to "productive and wary."** Axelrod's tournament showed that cooperative strategies dominate in iterated games. In direct computational markets, the ESS extends this: be productive and honest as a producer, cautious as a consumer — for the same structural reasons Axelrod's tit-for-tat succeeds.

**Encapsulation enforces property rights as physical law.** In human markets, property rights depend on imperfectly enforced legal codes. In software, object encapsulation can make theft structurally impossible — a computational entity cannot take what it cannot access. This turns a social constraint into an architectural one.

**Public-key cryptography extends the property rights framework.** Cryptographic identity enables unforgeable currencies and trademarks across open networks. An agent cannot impersonate another or counterfeit currency. This completes the property rights picture: encapsulation prevents internal theft; cryptography prevents external forgery.

**Direct vs. indirect market is the key architectural distinction.** Human markets are "indirect" — success in the market influences idea replication through cultural and educational channels, with long delays and lossy transmission. A direct computational market couples economic success to replication and variation immediately, creating a tighter evolutionary loop.

**Agoric open systems generalize the framework.** The paper positions this ecological analysis as foundation for "agoric open systems" — computational environments where market mechanisms coordinate diverse agents without central control. This anticipates the full agoric program: decentralized resource allocation, incentive-compatible protocols, and emergent productive behavior.

## Key Quotes

> "In a computational setting, these rules can be enforced as unbreakable 'physical' laws. In particular, rights of property (or ownership) can be implemented through encapsulation."

> "In a direct market implemented in software, a successful heuristic or strategy can directly acquire more processing power and can replicate itself with small variations if it chooses."

> "The resulting ESS is to be 'productive and wary'—wary as a consumer and productive and honest as a producer—for many of the same reasons that 'nice and retaliatory' is Axelrod's ESS."

> "Non-productive loops of mutually-rewarding heuristics then go broke, since (by conservation of currency) a group of heuristics can only gain net funds by receiving them from a solvent entity outside the group."

## Influence

This paper provided the theoretical ecology for what became the agoric open systems program. Its encapsulation-as-property-rights argument fed directly into capability security thinking — Mark Miller's later work on least authority and robust composition traces back to the intuition that access rights should be structural, not social. Nick Szabo referenced agoric systems in his early smart contract writing, and the direct market concept anticipates blockchain-enforced contracts. The paper remains a founding document for anyone arguing that market mechanisms and object capabilities are natural partners.

## Sources

- Primary: Miller, Mark S. and Drexler, K. Eric. "Comparative Ecology: A Computational Perspective." In: Huberman, B.A. (ed.), *The Ecology of Computation*. Elsevier/North-Holland, 1988. Full text at: <https://papers.agoric.com/papers/comparative-ecology-a-computational-perspective/full-text/>
- Secondary: Agoric Papers collection. <https://papers.agoric.com/papers/>
- Secondary: nvas blog, "The Agoric Papers." <https://blog.n.vasilak.is/post/46983306430/the-agoric-papers>
- Secondary: Agoric/Medium, "Agoric and the Decades-Long Quest for Secure Smart Contracts: Epicenter Interview with Mark S. Miller." <https://medium.com/agoric/agoric-and-the-decades-long-quest-for-secure-smart-contracts-epicenter-interview-with-mark-s-76c9a0fab6e2>
- Secondary: Wikipedia, "Mark S. Miller." <https://en.wikipedia.org/wiki/Mark_S._Miller>

## Relations

- relates_to::[[Miller & Drexler (1988) Markets and Computation]]
  - The companion paper in the same volume; Markets and Computation develops the agoric open systems program that Comparative Ecology provides the ecological rationale for
- relates_to::[[Miller (2006) Robust Composition]]
  - Miller's dissertation extends the encapsulation-as-property-rights argument from this paper into a formal capability security framework
- relates_to::[[Mark S. Miller]]
  - Person note for the primary architect of agoric systems and capability security; this paper is one of his earliest published contributions
- relates_to::[[Human Authority Over Augmentation Systems]]
  - The paper's voluntary-exchange foundation — agents interact through capability-mediated trade, not command — connects to the question of how human authority is preserved in agentic systems
