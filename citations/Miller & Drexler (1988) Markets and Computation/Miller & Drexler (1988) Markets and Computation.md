---
created: 2026-04-02
author: Christopher Allen
citation_slug: miller-drexler-1988-markets-and-computation
publication_year: 1988
canonical: "https://web.archive.org/web/20050213182510/http://www.agorics.com/Library/agoricpapers/aos/aos.0.html"
brief_summary: "Proposes market mechanisms -- price signals, property rights, trade, and decentralized decision-making -- as operating principles for software systems. Identifies object encapsulation as a reinvention of property rights and capability security as a market foundation. Introduces business agents, reputation systems, and charge-per-use economics as coordination mechanisms for multi-agent open systems."
tagline: "Market mechanisms imported wholesale into the computational domain as a coordination architecture"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Mark S. Miller]]

# Miller & Drexler (1988) Markets and Computation

## Bibliographic Entry

* _**Markets and Computation: Agoric Open Systems**_ (1988). [conference paper]. _Miller, Mark S.; Drexler, K. Eric._ In Huberman, B. (editor), *The Ecology of Computation*, North-Holland. Retrieved 2026-04-02 from: <https://web.archive.org/web/20050213182510/http://www.agorics.com/Library/agoricpapers/aos/aos.0.html>

## Summary

Miller and Drexler argue that market mechanisms — prices, property rights, and trade — can coordinate large software systems the way they coordinate economies. Object encapsulation in programming already reinvents property rights; extending it to computational resources enables ownership and trade. The paper proposes "agoric systems" where objects charge for services, pay rent for memory, bid for processor time, and delegate market behavior to business agents. Drawing on Hayek's work on distributed knowledge and spontaneous order, the paper establishes the intellectual foundation for object-capability security and decentralized coordination in open systems.

## Key Points

**Encapsulation is property rights.** Object-oriented encapsulation serves the same structural function as property rights in law: establishing protected spheres where entities plan and act despite limited external knowledge. This is not analogy — it is functional equivalence. Extending encapsulation from information and access to computational resources yields ownership and trade, the basis for markets.

**Security rests on inabilities, not abilities.** Turing-equivalence describes what a system can do, but security depends on what it cannot do. Adding a secure interpreter atop an insecure foundation does not subtract the foundation's dangerous abilities. Security must be built into the computational substrate, not layered on afterward. This argument foreshadows the principle of least authority.

**Capability security as market foundation.** Access to an object can only be obtained by being born with it, receiving it in a message, or creating the object. These three rules — later formalized as the object-capability model — provide the access control needed for computational markets without imposing verification overhead on simple objects.

**Islands of command in a sea of trade.** Drawing on Coase's theory of the firm, Miller and Drexler explain why computational markets will not be uniformly fine-grained. Transaction costs make market mechanisms expensive for small interactions. Objects aggregate into internally coordinated "firms" that participate in markets at boundaries where transactions justify the overhead. Market competition tunes this boundary.

**Business agents separate competence from performance.** Simple objects survive in complex markets by delegating resource management to shared business agents, just as they delegate core functions to subcontractors. An object can be simple in what it does while sophisticated in how it manages costs, because the sophistication lives in shared infrastructure.

**Prices tell agents what to do, not how hard to work.** Quoting Hayek: "the chief guidance which prices offer is not so much how to act, but *what to do*." Price signals in computational markets do not make software "sweat" — they guide objects toward actions that create value as judged by the system as a whole.

**Positive reputation through bonded commitment.** New objects establish trust by posting cash bonds guaranteeing performance, enforced by third parties. This resolves the reputation bootstrap problem and enables software entities to make enforceable commitments — contradicting the assumption that software cannot commit.

**Charge-per-use eliminates composition barriers.** Charge-per-copy creates pathological cost summation when software is composed from components. Charge-per-use enables low-volume users to access expensive software, eliminates switching costs, and makes it profitable to write and reuse small components.

**Intelligence without consciousness or unified will.** Intelligence — the capacity to achieve a range of goals through complex information processing — can be separated from individuality, consciousness, and will. A market system exhibits intelligence when it achieves goals set by participants using resources they provide, regardless of whether any component is individually conscious.

## Key Quotes

> "Like all systems involving goals, resources, and actions, computation can be viewed in economic terms."
> — Abstract (Section 0)

> "Turing-equivalence describes the *abilities* of a system, but security rests on inabilities — on the inability to violate certain rules. Adding an interpreter on top of a system cannot subtract abilities from the system itself."
> — Section 4.1

> "In short, motivated by the need for decentralized planning and division of labor, computer science has reinvented the notion of property rights."
> — Section 3.2

> "The idea of intelligence may thus be separated from the ideas of individuality, consciousness, and will."
> — Section 6.2

> "On a small scale, central planning makes sense; on a larger scale, market mechanisms make sense. Computer science began in a domain where central planning made sense, and central planning has thus been traditional."
> — Section 8

## Limitations

The paper assumes market mechanisms naturally distribute power through competition but does not address platform monopolies, network externalities, or winner-take-all dynamics that have characterized actual software markets. The principal problem in complex delegation chains — whose interests are served when agents delegate to sub-agents? — is not addressed here, though Miller developed this in his 2005 and 2006 work. The paper's solution to commons problems is pure privatization; Ostrom's alternative governance approach (published two years later) provides a complementary path the paper does not anticipate.

## Influence

This paper established the intellectual framework that led to Miller's object-capability model and the E programming language. The "agoric systems" concept directly influenced smart contract design, decentralized computation, and the capability-based security approach adopted in systems from KeyKOS to the Caja JavaScript sandbox. The Hayek-to-computation pipeline articulated here — distributed knowledge, spontaneous order, price-guided coordination — became a foundational argument for decentralized systems including blockchain architectures.

## Sources

- Miller, M. S. and Drexler, K. E. (1988). "Markets and Computation: Agoric Open Systems." In Huberman, B. (editor), *The Ecology of Computation*, North-Holland. Retrieved from Wayback Machine archive of agorics.com.
- Full text across 10 HTML pages (aos.0.html through aos.10.html) at the canonical URL.

## Relations

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
	- Miller and Drexler's "security rests on inabilities" argument provides the theoretical foundation for least authority as a design pattern. Allen's least authority is a design principle; Miller's 1988 formulation explains why it must be a foundational constraint.

- relates_to::[[Allen (2021) Principal Authority]]
	- The paper's framework of objects owning resources and delegating to agents establishes the ownership-and-delegation model that Allen's principal authority concept applies to identity systems. Both treat authority as originating from a source and flowing through delegation chains.

- relates_to::[[Human Authority Over Augmentation Systems]]
	- The paper's separation of intelligence from consciousness and unified will informs the augmentation principle: a multi-agent system can be intelligent without any component being autonomous. Authority comes from the principal-agent relationship, not from the system's intelligence.

- relates_to::[[Authority Flows from the Person]]
	- Miller and Drexler's encapsulation-as-property-rights argument parallels the property-to-agency shift in identity. Both treat protected spheres and delegable authority as the structural foundation for coordination.

- relates_to::[[Miller (2006) Robust Composition]]
	- The 1988 paper contains the intellectual seed of the object-capability model formalized 18 years later. The three rules for obtaining access, the argument about security through inabilities, and the connection between encapsulation and property rights all appear here in early form.

- relates_to::[[Miller, Tulloh & Shapiro (2005) The Structure of Authority]]
	- The 1988 paper's framework of ownership and delegation directly leads to the 2005 paper's formal analysis of authority structure. The principal problem latent in the 1988 paper becomes the central concern of the 2005 work.

- relates_to::[[Mark S. Miller]]
	- Co-author. Written while Miller was at Xerox Palo Alto Research Center. The paper represents the earliest published articulation of ideas that became his object-capability model and later informed smart contract design.
