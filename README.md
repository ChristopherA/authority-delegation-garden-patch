# Authority Delegation Garden Patch

A [garden patch](glosses/Garden%20Patch%20as%20Composable%20Knowledge%20Fragment.html) exploring authority delegation across boundaries — how authority flows from persons to agents, how it attenuates through delegation chains, and what happens when sovereign systems need to coordinate without anyone becoming the root authority.

## The Problem This Patch Addresses

I've been thinking about authority delegation for a long time — first through self-sovereign identity, then through progressive trust, and now through the lens of AI agent systems where a person delegates authority to agents who delegate to sub-agents.

The capability security community solved authority attenuation *inside* a system. Object capabilities, POLA, the principle that authority should be the minimum needed — these are well-understood. What's less well-understood is what happens *between* sovereign systems. When two people, each with their own agents, need to collaborate — that's not attenuation within a hierarchy. It's progressive trust across a boundary.

I think the interesting question isn't "how do we attenuate authority?" (solved) or "how do we model alien access?" (interesting). It's "how do sovereign systems build trust incrementally across heterogeneous architectures without anyone adopting anyone else's model?"

## What's in This Patch

### The Narrative Spine

Start here and follow the thread:

1. **[Authority Flows from the Person](principles/Authority%20Flows%20from%20the%20Person.html)** — the foundational principle. All legitimate authority traces back to a person's sovereign choice.

2. **[Authority Conferral Chain](models/Authority%20Conferral%20Chain.html)** — how authority moves through delegation: person → agent → sub-agent, with attenuation at each step.

3. **[Delegated Decision Authority Spectrum](boundaries/Delegated%20Decision%20Authority%20Spectrum.html)** — where does delegated authority end? The boundary conditions.

4. **[Progressive Trust as Agent Delegation Model](inquiries/Progressive%20Trust%20as%20Agent%20Delegation%20Model.html)** — the open question: can progressive trust govern agent delegation the way POLA governs capability attenuation?

### Sovereignty as Membrane

These two conviction nodes ground the sovereignty framing:

- **[Dignity Requires Sovereignty and Sovereignty Is a Membrane](convictions/Dignity%20Requires%20Sovereignty%20and%20Sovereignty%20Is%20a%20Membrane.html)** — sovereignty is not absolute control but selective permeability
- **[Sovereignty Is Selective Permeability Not Absolute Control](convictions/Sovereignty%20Is%20Selective%20Permeability%20Not%20Absolute%20Control.html)** — the membrane metaphor: what passes through, what doesn't, and who decides

### Published Work

My articles grounding these concepts:

- **[Allen (2021) Principal Authority](citations/Allen%20(2021)%20Principal%20Authority.html)** — agency law principles applied to digital identity
- **[Allen (2022) Progressive Trust](citations/Allen%20(2022)%20Progressive%20Trust.html)** — trust as graduated disclosure, not binary grant
- **[Allen (2024) Progressive Trust](citations/Allen%20(2024)%20Progressive%20Trust.html)** — the updated version with practical patterns
- **[Allen (2024) Building Trust in Gradients](citations/Allen%20(2024)%20Building%20Trust%20in%20Gradients.html)** — architectural implications
- **[Allen (2016) The Path to Self-Sovereign Identity](citations/Allen%20(2016)%20The%20Path%20to%20Self-Sovereign%20Identity.html)** — where this thinking started

### Open Questions

The garden hosts questions it can't answer alone:

- **[Progressive Trust as Agent Delegation Model](inquiries/Progressive%20Trust%20as%20Agent%20Delegation%20Model.html)** — where POLA and progressive trust might converge
- **[Federated Agent Governance Across Sovereign Estates](inquiries/Federated%20Agent%20Governance%20Across%20Sovereign%20Estates.html)** — coordination without centralization
- **[Personal Sovereignty as a Membrane](inquiries/Personal%20Sovereignty%20as%20a%20Membrane.html)** — the biological metaphor applied to digital identity boundaries

### Capability Security Foundations

Citation dossiers for the foundational work on capability security and least authority — the lineage from least privilege through object capabilities to authority delegation:

- **[Saltzer & Schroeder (1975) The Protection of Information in Computer Systems](citations/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems/Saltzer%20%26%20Schroeder%20(1975)%20The%20Protection%20of%20Information%20in%20Computer%20Systems.html)** — the paper that named the Principle of Least Privilege
- **[Miller & Drexler (1988) Comparative Ecology](citations/Miller%20%26%20Drexler%20(1988)%20Comparative%20Ecology/Miller%20%26%20Drexler%20(1988)%20Comparative%20Ecology.html)** — computational markets and agent design origins
- **[Miller & Drexler (1988) Markets and Computation](citations/Miller%20%26%20Drexler%20(1988)%20Markets%20and%20Computation/Miller%20%26%20Drexler%20(1988)%20Markets%20and%20Computation.html)** — market mechanisms as coordination architecture
- **[Miller, Tribble, Pandya & Stiegler (1995) The Open Society and its Media](citations/Miller%2C%20Tribble%2C%20Pandya%20%26%20Stiegler%20(1995)%20The%20Open%20Society%20and%20its%20Media/Miller%2C%20Tribble%2C%20Pandya%20%26%20Stiegler%20(1995)%20The%20Open%20Society%20and%20its%20Media.html)** — Popperian epistemology as discourse architecture
- **[Miller, Tulloh & Shapiro (2005) The Structure of Authority](citations/Miller%2C%20Tulloh%20%26%20Shapiro%20(2005)%20The%20Structure%20of%20Authority/Miller%2C%20Tulloh%20%26%20Shapiro%20(2005)%20The%20Structure%20of%20Authority.html)** — "security is not a separable concern"
- **[Miller (2006) Robust Composition](citations/Miller%20(2006)%20Robust%20Composition/Miller%20(2006)%20Robust%20Composition.html)** — the dissertation that formalized POLA and object capabilities
- **[Miller (2019) Architectures of Robust Openness](citations/Miller%20(2019)%20Architectures%20of%20Robust%20Openness/Miller%20(2019)%20Architectures%20of%20Robust%20Openness.html)** — robust social systems open to strangers

Each includes analysis and insights sub-files exploring how the source connects to progressive trust and sovereign-to-sovereign coordination.

## What Is a Garden Patch?

A garden patch is a curated projection of selected nodes from a personal knowledge garden, published for a specific audience and conversation. It is not a wiki, not documentation, and not a static paper. It is a typed knowledge graph rendered as a navigable website.

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
- 12 citation compounds (37 files) in [citations](citations/) — deep reads of published work (5 Allen, 6 Miller, 1 Saltzer & Schroeder)
- 9 [glosses](glosses/) — concept definitions and vocabulary bridges
- 1 [boundary](boundaries/) — where responsibility changes hands
- 1 [decision](decisions/) — architectural choice with rationale
- 3 [inquiries](inquiries/) — open questions the garden hosts
- 3 [domains](domains/) — knowledge area definitions
- 35 [form type definitions](forms/) — structural contracts governing every node

See the [Node Directory](NODES.md) for the complete inventory.

---

**Author**: Christopher Allen
**Source garden**: [Deep Context Architecture](domains/Deep%20Context%20Architecture.html) — the source for grafted nodes. The full garden is in progress and will be published at [DeepContext.com](https://deepcontext.com).
**Status**: This entire garden patch is at Seed Stage — initial creation, intended to grow through dialogue.
**License**: Content is available under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) unless otherwise noted.
