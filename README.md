# Authority Delegation Garden Patch

A [garden patch](glosses/Garden%20Patch%20as%20Composable%20Knowledge%20Fragment.html) exploring authority delegation across boundaries — published for a conversation between Christopher Allen and Mark S. Miller about naming the kinds of authority that flow through non-hierarchical agent systems.

## Why This Patch Exists

Mark, I built this for our conversation. You'll recognize the territory — it's the lineage from your Club System through Robust Composition to Horton, set alongside my work on progressive trust and self-sovereign identity. I've been running a system where AI agents delegate to sub-agents, grounded in Gordian Clubs and personal LLMs that run locally. Inside the system, attenuation works and is well named. At the boundaries — when agents cross into foreign access models, and especially when two sovereign systems need to build trust without either adopting the other's model — I don't have the words yet.

I think your vocabulary is what I need. This patch organizes what I've been thinking so you can see where I am and where the gaps are.

It's also, in a way, a descendant of Xanadu. Typed nodes with labeled relationships, selective sharing from a private garden to a public projection, self-contained structure that doesn't depend on the source system. I'm already doing cross-patch exchange with other people who maintain their own knowledge systems — different naming conventions, different architectures, same conceptual territory — and the interoperability question we're navigating is itself the sovereign-to-sovereign problem I want to discuss with you.

## Where to Start

### The Three Layers

The conversation has a natural arc from solved to unsolved:

**Layer 1: Inside the estate — attenuation works.** Start with [Authority Flows from the Person](principles/Authority%20Flows%20from%20the%20Person.html), then [Authority Conferral Chain](models/Authority%20Conferral%20Chain.html), then [Delegated Decision Authority Spectrum](boundaries/Delegated%20Decision%20Authority%20Spectrum.html). Personal LLMs running locally, interlocking key infrastructure, delegation through progressively narrower scope. This is the warm-up — the question here is quick: does the cryptographic club model satisfy your OCap critique of the original?

**Layer 2: Outward through alien access models.** When an agent crosses from key-based sovereign authority to someone else's system — SSH to GitHub, OAuth to an API — it holds a credential in a foreign access model. I have infrastructure for sovereign key discovery and coordination (described in the brief I sent). The OCap vocabulary for this crossing is what I want from you.

**Layer 3: Sovereign-to-sovereign progressive trust.** Two people, each running their own agent system with their own keys and trust criteria. TOFU bootstraps first contact. [Progressive trust](citations/Allen%20(2022)%20Progressive%20Trust/Allen%20(2022)%20Progressive%20Trust.html) builds confidence through repeated interactions. But the vocabulary for achieving this cryptographically across sovereign boundaries and heterogeneous designs isn't well defined. Neither side should adopt the other's model. This is the hard question — [Progressive Trust as Agent Delegation Model](inquiries/Progressive%20Trust%20as%20Agent%20Delegation%20Model.html) frames it as an open inquiry.

### The Horton Bridge

Your [Horton paper](citations/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems.html) bridges all three layers. Responsibility as authority coupled with accountability, layered on the capability substrate without modifying it — that's the architectural move I'm trying to extend. Blockchain Commons has building blocks Horton doesn't (cryptographic bearer proofs, self-contained objects, sovereign key discovery), and Horton has pieces we haven't built yet (the proxy/stub accountability layer, inductive trust bootstrapping). The [interposition pattern](glosses/Accountability%20as%20a%20Layer%20Not%20a%20Replacement.html) — adding coordination between systems without modifying either side — generalizes to the cross-garden problem this patch itself embodies.

The Horton citation dossier includes [analysis](citations/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems%20—%20Analysis.html) and [insights](citations/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems%20—%20Insights.html) connecting the protocol to agent delegation architecture. I'd be curious how these land — whether the connections hold up to the person who designed the protocol.

### Sovereignty as Membrane

These two conviction nodes ground the sovereignty framing:

- **[Dignity Requires Sovereignty and Sovereignty Is a Membrane](convictions/Dignity%20Requires%20Sovereignty%20and%20Sovereignty%20Is%20a%20Membrane.html)** — sovereignty is not absolute control but selective permeability
- **[Sovereignty Is Selective Permeability Not Absolute Control](convictions/Sovereignty%20Is%20Selective%20Permeability%20Not%20Absolute%20Control.html)** — the membrane metaphor: what passes through, what doesn't, and who decides

And this model describes the working system where those principles actually operate — how self-sovereign identity patterns organize agent delegation inside the estate and enable commons across estates:

- **[The Self-Sovereign Estate Persona Architecture](models/The%20Self-Sovereign%20Estate%20Persona%20Architecture.html)** — the same membrane that organizes a person's agents enables collaboration across sovereign systems

## Your Papers in This Patch

I did deep reads of eight of your papers — each has a citation dossier with analysis and insights exploring how the source connects to progressive trust and sovereign-to-sovereign coordination:

- **[Saltzer & Schroeder (1975)](citations/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems.html)** — the paper that named the Principle of Least Privilege
- **[Miller & Drexler (1988) Comparative Ecology](citations/Miller%20%26%20Drexler%20(1988)%20Comparative%20Ecology/Miller%20%26%20Drexler%20(1988)%20Comparative%20Ecology.html)** — computational markets and agent design origins
- **[Miller & Drexler (1988) Markets and Computation](citations/Miller%20%26%20Drexler%20(1988)%20Markets%20and%20Computation/Miller%20%26%20Drexler%20(1988)%20Markets%20and%20Computation.html)** — market mechanisms as coordination architecture
- **[Miller, Tribble, Pandya & Stiegler (1995) The Open Society and its Media](citations/Miller%2C%20Tribble%2C%20Pandya%20%26%20Stiegler%20(1995)%20The%20Open%20Society%20and%20its%20Media/Miller%2C%20Tribble%2C%20Pandya%20%26%20Stiegler%20(1995)%20The%20Open%20Society%20and%20its%20Media.html)** — Popperian epistemology as discourse architecture
- **[Miller, Tulloh & Shapiro (2005) The Structure of Authority](citations/Miller%2C%20Tulloh%20%26%20Shapiro%20(2005)%20The%20Structure%20of%20Authority/Miller%2C%20Tulloh%20%26%20Shapiro%20(2005)%20The%20Structure%20of%20Authority.html)** — "security is not a separable concern"
- **[Miller (2006) Robust Composition](citations/Miller%20(2006)%20Robust%20Composition/Miller%20(2006)%20Robust%20Composition.html)** — the dissertation that formalized POLA and object capabilities
- **[Miller, Donnelley & Karp (2007) Delegating Responsibility in Digital Systems](citations/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems/Miller%2C%20Donnelley%20%26%20Karp%20(2007)%20Delegating%20Responsibility%20in%20Digital%20Systems.html)** — the Horton protocol: accountability layered on capabilities
- **[Miller (2019) Architectures of Robust Openness](citations/Miller%20(2019)%20Architectures%20of%20Robust%20Openness/Miller%20(2019)%20Architectures%20of%20Robust%20Openness.html)** — robust social systems open to strangers

## My Published Work

The articles grounding the progressive trust and self-sovereign identity side:

- **[Allen (2016) The Path to Self-Sovereign Identity](citations/Allen%20(2016)%20The%20Path%20to%20Self-Sovereign%20Identity/Allen%20(2016)%20The%20Path%20to%20Self-Sovereign%20Identity.html)** — where this thinking started
- **[Allen (2021) Principal Authority](citations/Allen%20(2021)%20Principal%20Authority/Allen%20(2021)%20Principal%20Authority.html)** — agency law principles applied to digital identity
- **[Allen (2022) Progressive Trust](citations/Allen%20(2022)%20Progressive%20Trust/Allen%20(2022)%20Progressive%20Trust.html)** — trust as graduated disclosure, not binary grant
- **[Allen (2024) Progressive Trust](citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html)** — the updated version with practical patterns
- **[Allen (2024) Building Trust in Gradients](citations/Allen%20(2024)%20Building%20Trust%20in%20Gradients/Allen%20(2024)%20Building%20Trust%20in%20Gradients.html)** — architectural implications

### Where This Goes

The scenario node describes where this all points — thousands of independent gardens, each tended by sovereign agents running locally, exchanging nodes peer-to-peer through progressive trust:

- **[Thousand Gardens with Autonomous Trust](scenarios/Thousand%20Gardens%20with%20Autonomous%20Trust.html)** — what happens when gardens become autonomous cryptographic objects that trust each other progressively

## Open Questions

The garden hosts questions it can't answer alone:

- **[Progressive Trust as Agent Delegation Model](inquiries/Progressive%20Trust%20as%20Agent%20Delegation%20Model.html)** — where POLA and progressive trust might converge
- **[Federated Agent Governance Across Sovereign Estates](inquiries/Federated%20Agent%20Governance%20Across%20Sovereign%20Estates.html)** — coordination without centralization
- **[Personal Sovereignty as a Membrane](inquiries/Personal%20Sovereignty%20as%20a%20Membrane.html)** — the biological metaphor applied to digital identity boundaries

## What Is a Garden Patch?

A garden patch is a curated projection of selected nodes from a personal knowledge garden, published for a specific audience and conversation. It is not a wiki, not documentation, and not a static paper. It is a typed knowledge graph rendered as a navigable website.

This is the third garden patch. The [first](https://christophera.github.io/persona-garden-patch/) was published for a Thursday conversation about persona architecture — different audience, different slice of the same garden, but the same typed-node infrastructure underneath. The mechanism is still a prototype. I'm figuring out what works by doing it, and each patch teaches me something about what cross-garden exchange actually requires. The [scenario node](scenarios/Thousand%20Gardens%20with%20Autonomous%20Trust.html) describes where I think this goes — thousands of independent gardens sharing nodes peer-to-peer through progressive trust, each tended by sovereign agents running locally. We're a long way from that. But the patches are the first proof that the basic unit works: fork a slice, add your own connections, publish it for a conversation.

Every page in this patch is a **garden node** — a markdown document with typed predicates (labeled directed edges) that connect it to other nodes. The predicates form a traversable graph: `relates_to::[[Target Node]]` is not a tag or a category — it is a structural relationship with an annotation explaining *how* the two nodes relate.

For more on the garden patch concept, see [Garden Patch as Composable Knowledge Fragment](glosses/Garden%20Patch%20as%20Composable%20Knowledge%20Fragment.html).

## How to Read Garden Nodes

### Link Markers

| What You See | What It Means |
|---|---|
| \[\[Node Name\]\] | **Grafted node** — copied from the source garden into this patch. Click to navigate. |
| \[\[Node Name\]\]↑ | **Upstream node** — exists in the source garden but was not grafted into this patch. |
| \[\[Node Name\]\] *(unlinked)* | **Ghost link** — a reference to a node that does not exist yet. A stake in the ground marking where a node could grow. |

### For AI Agents

If you are an AI agent preparing your human for a conversation, start with [AGENT.md](AGENT.md). It explains how to read garden nodes and suggests a reading path.

## By the Numbers

- 3 [principles](principles/) — what should always be true
- 2 [models](models/) — how elements relate
- 2 [convictions](convictions/) — beliefs with grounding
- 13 citation compounds (40 files) in [citations](citations/) — deep reads of published work (5 Allen, 7 Miller, 1 Saltzer & Schroeder)
- 10 [glosses](glosses/) — concept definitions and vocabulary bridges
- 1 [boundary](boundaries/) — where responsibility changes hands
- 1 [decision](decisions/) — architectural choice with rationale
- 1 [scenario](scenarios/) — where this architecture leads
- 3 [inquiries](inquiries/) — open questions the garden hosts
- 3 [domains](domains/) — knowledge area definitions
- 35 [form type definitions](forms/) — structural contracts governing every node

See the [Node Directory](NODES.md) for the complete inventory.

---

**Author**: Christopher Allen
**Source garden**: [Deep Context Architecture](domains/Deep%20Context%20Architecture.html) — the source for grafted nodes. The full garden is in progress and will be published at [DeepContext.com](https://deepcontext.com).
**Status**: This entire garden patch is at Seed Stage — initial creation, intended to grow through dialogue.
**License**: Content is available under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) unless otherwise noted.
