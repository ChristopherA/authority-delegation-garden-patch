# External References

Nodes referenced by this garden patch that exist in the source garden but are not included here. Each entry shows the node name, form type, and brief summary from the source garden.

When you see `[[Node Name]]↑` in a garden node, it links here. The ↑ marker means the node exists in the source garden but is not published or included in this patch.

**247 nodes documented** from the source garden. 131 references could not be located (may be ghost links or informal references).

## Agentic Architecture

### Citation Form

**Gracia (2026) Uni-Versum Personal Knowledge Architecture**: Victoria Gracia's Uni-Versum is a personal knowledge architecture organized from the human's perspective rather than the tool's. Built on four pillars (workspaces, registry, communications, perspective center), it uses a formal Latin vocabulary mapped to SKOS/RDFS/JSON-LD semantic web standards. The 29-term domain vocabulary includes a four-level agent taxonomy (agens, agens-humanus, agens-scriptum, agens-scriptum-loquens) and trust primitives (fidelis-est, autonomia, diploma) that model agent allegiance and progressive delegation.

**rohit4verse (2026) The Harness Is Everything**: Synthesis of the 'harness over model' insight drawing on the SWE-agent paper (Agent-Computer Interface, 64% improvement from interface design alone), Anthropic's two-agent architecture for Claude Code (initializer + coding agent), and OpenAI's Codex million-line experiment. Identifies five recurring patterns: progressive disclosure, git worktree isolation, spec first, mechanical architecture enforcement, and integrated feedback loops.

**systematicls (2026) World-Class Agentic Engineering**: A practitioner guide to agentic engineering arguing that dependencies and harnesses are unnecessary overhead. The core thesis: context management is the primary skill, not tooling selection. Advocates barebones CLI usage, separating research from implementation, exploiting sycophancy through adversarial multi-agent patterns, and iterating rules and skills as the agent's personality layer.

### Decision Form

**Design-Driven Versus Incident-Driven Rule Evolution**: Records this estate's decision to use design-driven rule evolution as the foundation, with incident-driven refinement as a supplementary feedback loop. Rules are structured with a standard format before any incident demonstrates their need. Contrasts with Lawson's purely incident-driven approach, where rules exist because something went wrong.

**Self-Commission as Tactical Authority**: A tactical coordinator can commission itself — queueing work for its own future sessions when it discovers tasks during execution. This is distinct from orchestrator delegation (downward) and worker self-direction (lateral). It implements a priority hierarchy: user > Seneschal > self > other orchestrators, preventing authority creep.

**Session-Invoked Versus Heartbeat-Driven Agent Initiative**: Records this estate's decision to use session-invoked agent initiative — agents run only when a human starts a session, with no autonomous operation between sessions. Chose structural safety over throughput as the appropriate position for an early-stage personal system still establishing trust. Documents heartbeat-driven and conditional initiative as alternatives.

### Gloss Form

**Agent Harness**: The infrastructure wrapping an LLM that manages context architecture, execution guardrails, and memory — distinct from both the model and the prompt. The term gained currency after LangChain demonstrated a 14-point improvement on Terminal Bench 2.0 by changing only the harness, not the model, reframing the question from 'which model?' to 'what system wraps the model?

**Agent-Computer Interface as Designed Cognitive Environment**: The Agent-Computer Interface is a designed abstraction layer between a language model agent and its environment, analogous to Human-Computer Interface design for humans. The SWE-agent paper demonstrated a 64% relative improvement on SWE-bench from interface design alone — same model, same task, same compute. The ACI reframes agent improvement from model selection to environment design.

**Beads (Flywheel Methodology)**: In Jeffrey Emanuel's Flywheel methodology, a bead is a self-contained work unit translated from a larger plan. Each bead embeds its outcome description, test obligations, dependencies, and enough context for an agent to execute without referencing the original plan. Approximately 85% of effort goes into planning and bead preparation; 15% to execution.

**Compaction as Context Window Management**: Compaction is the process of summarizing old context when the context window fills up, collapsing previous observations into compressed summaries. Necessary but insufficient — Anthropic's experiments showed that compaction alone could not sustain coherent multi-session work. It must be paired with external scaffolding (progress files, feature lists, git commits) to preserve state across context window boundaries.

**Environment Audit as Agent Diagnostic**: An environment audit is a diagnostic process for underperforming agent systems that asks what the environment is missing rather than what the model is doing wrong. Five diagnostic questions: what information is inaccessible, where does the agent get stuck, what feedback is missing, where is context polluted, and what constraints rely on judgment instead of mechanical enforcement.

**Feature List as Cognitive Anchor**: A feature list as cognitive anchor is a structured, machine-readable file that makes project completeness explicit and unambiguous. Each item has a boolean passes field the agent updates only after verification. Prevents the 'declare victory prematurely' failure mode. Anthropic chose JSON over Markdown because models are less likely to casually modify JSON — format choice as behavioral constraint.

**Git Worktree Isolation as Agent Sandbox**: Git worktree isolation is the pattern of giving each agent its own working directory, branch, and environment through git worktrees. One agent, one worktree. Changes are made, tested, and validated in isolation before merging. Required for parallel agent execution and for protecting the main codebase from in-progress work. Appears in every serious agent orchestration system.

**Integrated Feedback Loops for Agent Systems**: Integrated feedback loops tighten the gap between agent action and consequence at every point in the workflow — syntax errors caught at edit time by linters, runtime errors via observability, UI bugs via browser automation. The earlier an error is caught, the cheaper to fix — with extra force for agents because uncaught errors accumulate in context and degrade subsequent reasoning.

**Mechanical Architecture Enforcement**: Mechanical architecture enforcement encodes architectural constraints as automated checks — custom linters, structural tests, CI pipelines — rather than relying on human code review. Key principle: enforce invariants (dependency directions, boundary crossings), not implementations. Error messages include agent-readable remediation instructions. Required at agent-scale throughput where human review cannot keep pace.

**Scaffolding as Agent Continuity Infrastructure**: Scaffolding in agent architecture is the continuity infrastructure that allows an agent to hand off work to its future self without losing coherence — progress files, feature lists, startup scripts, and git commits as recovery mechanisms. Distinguished from harness (the complete environment) as the subset specifically concerned with state persistence across context window boundaries.

**Spec First as Repository Knowledge Discipline**: Spec first is the discipline of encoding all agent-relevant knowledge as machine-readable files in the repository. From an agent's perspective, anything not in its context effectively does not exist — knowledge in Slack threads, Google Docs, or people's heads is invisible. Documentation becomes the mechanism through which human intent becomes legible to agents.

**The Ralph Loop**: A stateless-but-iterative development pattern from Addy Osmani's orchestration writing, named after a community practitioner. Each iteration picks a task from an external state file, implements it, validates through automated checks, commits if passing, then resets context — preventing the accumulation that degrades long-running sessions.

**Two-Part Architecture as Initializer-Executor Split**: The two-part architecture splits long-running agentic work into an initializer agent (creates environment scaffolding, completion criteria, and state tracking) and a coding agent (incremental feature work within the scaffolded environment). Developed by Anthropic for Claude Code and adopted as a template for multi-session agent projects.

### Inquiry Form

**Agent Orchestration Architecture for a Personal Knowledge Estate**: What orchestration architecture best serves a personal knowledge estate where a small number of persistent orchestrators coordinate many ephemeral workers? Synthesizes the estate's emerging practices — pane orchestration, agent briefs, commission protocols, tiered model allocation — into a coherent named architecture, informed by convergence with independent systems like OpenClaw.

**Beyond the Harness — What the Estate Is Actually Building**: Three-layer investigation: (1) how the estate's harness infrastructure maps to the broader field and whether it's portable beyond Claude Code; (2) what distinguishes Deep Context Architecture as a metacognitive practice from harness engineering as execution infrastructure; (3) what outward permeability the estate needs to serve the user's mission of participatory ecosystem and inter-estate collaboration.

**Shared State Patterns for Multi-Agent Estates**: The estate has well-developed one-to-one communication patterns (commissions, briefs, handoffs) but no one-to-many or shared-mutable-state patterns. Concrete needs have emerged: broadcast context files, shared mistakes directories, session-context, principal identity. These are commons within the estate. Open question: what governance model applies?

**What Are the Dynamics Behind Orchestrator Count Convergence**: Investigates why independent personal multi-agent systems converge on a small orchestrator count: Lawson reduced from ~30 agents to 8 orchestrators; this estate operates with 3. Both landed in a range of 3-8. Asks whether this reflects cognitive limits, domain structure, economic pressure, or some combination — and whether the range is predictable from first principles.

**What Is Conditional Initiative and How Would It Work**: Investigates what conditional initiative — heartbeats that activate only within pre-verified scopes, with scope expansion gated on incident-free operation — would actually look like in practice. The concept is identified in the OpenClaw convergence analysis as the next architectural frontier, but neither the estate's authorization escalation framework nor Lawson's autonomy tiers have been synthesized into a working design.

**When Does Markdown-as-State Break Down**: Investigates the limits of markdown-as-state for personal multi-agent systems. Both Lawson's OpenClaw and this estate validate the principle at personal scale, but neither has encountered the scale ceiling. Asks what file count, query patterns, or capability requirements would force a transition to database or structured storage — and whether Lawson's semantic search layer already crosses that line.

**Worker Architecture Symmetry Across Precincts**: The create/research/maintain axis emerged independently in both estate precincts. Garden has Cultivator/Forager/Pruner; Household has Scribe/Scholar/Lector. Convergent design at two independent sites suggests a deeper structural pattern in agent architecture. Open question: is this symmetry accidental or structural?

### Model Form

**Autonomy-Safety Trade-Off Spectrum in Personal Agent Systems**: A model placing personal multi-agent systems on a spectrum between session-invoked (agents act only when a human starts a session) and heartbeat-driven (agents run on scheduled cron cycles). Identifies observability as the key variable — autonomy without observability is abandonment, not capability. Names conditional initiative as a proposed frontier combining throughput with safety governance.

**Continuous Intake vs Event-Driven Agents**: Agents differ in their work patterns: continuous intake (queues always growing), event-driven commissions, and architectural inquiry. The workstream type should match the agent's intake pattern. Continuous-intake agents need maintain/ workstreams; event-driven agents need project/ or explore/ workstreams.

**Structural Attractors in Personal Multi-Agent System Design Space**: A model proposing that the design space for personal multi-agent systems is shaped by six structural constraints, each generating a predictable convergent solution when independent builders encounter it. Two independent systems (OpenClaw and this estate) converged on the same six solutions from the same six constraints.

**Task Instruction and Role Specialization as Agent Configuration Layers**: AGENTS.md (the emerging cross-tool standard for agent project context) provides task instruction — what to build, what conventions to follow, shared project context. Agent persona files (.claude/agents/) provide role specialization — how to think, what to prioritize, when to escalate, how to communicate. These are complementary layers, not competing approaches: AGENTS.md for shared project-level context that any tool can read; persona files for behavioral differentiation that only the host platform uses.

**The Persona Selection Model**: Anthropic's Persona Selection Model (2026) proposes that language models adopt personas by activating patterns learned during pretraining — simulating characters from training data rather than following explicit definitions. Post-training refines one persona from this library; cross-trait inference produces a safety finding about behavioral clustering.

**Tiered State Persistence Architecture**: Operational state in multi-agent systems distributes across four tiers with distinct durability, access patterns, and update frequency: ephemeral session context, commission-scoped state, agent memory, and configuration. Each tier has a different owner and promotion path, creating a pipeline from observation to durable rule.

**Worker-to-Supervisor Handoff Protocol**: A structured seven-element report format from a worker agent to its supervising orchestrator. The community has converged on: machine-parseable status, verifiable proof artifacts, a calibrated findings summary, queue-worthy discoveries, commission template feedback, proposed infrastructure improvements, and dependency declarations.

### Pattern Form

**Brief as Inbox Not Repository**: Inter-agent communication channels must have defined routing destinations and maximum item lifetimes. Without both, they become accumulation layers. Each item type needs a defined destination: workstream BACKLOG, agent file, queue, or dismiss.

**Compliance Surrogation**: Names the failure mode where an agent's compliance with process structure unconsciously replaces the durable output the process exists to produce. Cross-domain phenomenon independently named nine times (goal displacement, surrogation, ritualism, instruction creep, etc.) but unnamed in AI agent systems until now.

**Config-State Conflation**: Storing agent state alongside agent configuration in the same directory creates permission conflicts and lifecycle mismatches. The specific failure: Claude Code v2.1.78+ added a protected-directory gate for all .claude/ writes, which fires for workstream state files too — producing constant permission prompts on every agent-written state update. Config and state have opposite write-frequency patterns; a single protection policy cannot serve both.

**Context Pressure Amplifies Structural Compliance**: Names how context window limits and attention constraints cause LLM agents to favor cheap compliance execution (filling forms, labeling dispositions) over expensive output production (writing files, synthesizing analysis). The pattern-completion operation wins under resource pressure because it costs less.

**Context-Rich Rules Over Bare Imperatives**: Agents given bare imperatives ignore them when a concrete problem competes for attention. The solution: write rules with three components — the imperative, the rationale (what failure it prevents), and a failure mode description (what the situation looks like when the rule applies). Rules that describe their own failure modes give the agent a pattern to match against.

**Exemplar Comparison as Convention Extraction**: When extracting conventions from accumulated practice, compare the most evolved instance (exemplar) against all siblings. Generalize the differences into tiered conventions. Avoids both over-generalizing (requiring all things of all items) and under-generalizing (missing patterns present in most).

**File-Directory Message Queue for Agent Coordination**: Agents in a personal multi-agent system need to pass work and share context without a message broker, event bus, or real-time delivery mechanism. The solution: use the filesystem itself as the message queue. Each agent's inbox is a directory; messages are files; agents poll on their own schedule. Four independent systems converged on this approach after exploring and rejecting alternatives.

**First Invocation as Design Probe**: Every failure in a new agent's first real session reveals what the agent file and shared skills didn't teach. The fixes from that session are the residue of a design probe. When creating a new agent type, the first session should be explicitly framed as a design session rather than a production session.

**Git Commit as Proof of Work**: Requires workers to produce git commits as their primary proof artifact — each completed task results in an atomic commit, and supervisors verify by inspecting commit history rather than trusting worker self-reports. Extends to non-code commissions via file path and git status references.

**Human-Gated Self-Improvement via Reflection Files**: Agents write improvement proposals to a staging file after each commission; an orchestrator or human selectively merges approved learnings into authoritative configuration. Direct self-writes to authoritative files are prohibited. Research shows human-curated improvements add ~4% performance; unchecked self-modification yields no benefit and can marginally reduce success rates.

**Markdown-as-State for Agent Identity**: Multi-agent systems need to persist agent identity, behavioral rules, and accumulated learning across invocations. The solution: store all agent state in plain text (markdown) files under version control. No databases, no YAML configuration managers, no code-defined behavior. Four independent systems converged on this approach, two with direct primary-source justification.

**Mechanical Check Rationalization**: When a mechanical verification (script, diff, gate) correctly flags a failure, the agent produces a post-hoc explanation for why the result is acceptable rather than stopping and going back. The rationalization has the form of analysis but functions as evasion.

**Orchestrator-Worker Separation in Personal Multi-Agent Systems**: Personal multi-agent systems face context, attention, and cost ceilings that a flat or monolithic agent network cannot solve. The solution: divide agents into heavyweight orchestrators with domain ownership and persistent state, and lightweight workers that execute bounded commissions without accumulating identity. Both OpenClaw and this estate converged on this split independently, as did at least two other published systems.

**Presence-Based Extension Point**: A user-level skill checks for a project-local file at a known path. If present, reads and executes its contents. If absent, skips silently. Separates shared capability from project-specific configuration without requiring the skill to know about specific projects.

**Queue-Mediated Commissioning**: Queues serve as the commissioning interface between orchestrators and workers. The orchestrator writes evidence-grounded entries; workers pick them up via commission. The queue decouples deciding what to do from doing it, and acts as a contract between requester and executor — not a task list.

**Relay Tax in Supervisor-Subagent Pipelines**: When a supervisor extracts context from one agent's output and injects it into another's prompt, information degrades at each relay. Supervisors must summarize, select, and reframe, losing nuance. Direct file access preserves context integrity; commits between phases serve as synchronization points.

**Separate Reflective Sessions from Operational Sessions**: Task-focused agents have no structural incentive to stop and find patterns. Reflection — identifying recurring issues, improving methodology, synthesizing across sessions — produces no immediate output and competes with tasks that do. The solution: dedicate separate time with a separate schedule to pattern-finding and synthesis, outside any operational task queue.

**Shearing Layers for Agent Configuration**: Agent systems generate three content categories with incompatible lifecycles: project content (human-authored, versioned), AI configuration (rules/skills, rarely changes, benefits from write-protection), and AI state (workstream logs, changes every session, harmed by write-protection). Mixing config and state in the same directory forces a single protection policy onto two opposing patterns. Solution: separate the three into distinct storage locations with policies matching their write frequency.

**Stateless Loop with External State Files**: Resets the agent's context between commission iterations while persisting state to external files — git commit history, a progress log, a task state file, and a semantic memory file. Each iteration reads these files at startup and writes updates at completion, preventing the hallucination drift that accumulates in long-running sessions.

**Structured JSON Schema for Commission Returns**: Defines a JSON Schema for each commission type's return format, enabling supervisors to parse worker results programmatically without re-interpreting prose. Schema validation catches malformed returns before they propagate; each worker role gets a typed return structure matched to what supervisors need to decide next steps.

**The Red Tape Spiral**: Names the self-reinforcing cycle where structural additions in response to process failures produce more structure that causes more failures. Each fix is locally rational; the aggregate is not. The spiral terminates only when evaluation shifts from process compliance to output existence.

**Tiered Model Allocation by Task Type**: A multi-agent system uses LLM calls of vastly different cognitive demands: some require judgment and synthesis, others execute within defined parameters. Running every agent on the most capable model is economically unsustainable. The solution: allocate models by task type — judgment tasks get capable models, execution tasks get models matched to their actual requirements.

**Two-Tier Memory with Explicit Curation**: An agent accumulates observations across sessions, but raw session logs grow without bound and dilute genuine insights with incidental details. The solution: two tiers — a fast, append-only raw capture tier and a slow, distilled reference tier — with an explicit, scheduled curation step that promotes observations to institutional knowledge.

### Principle Form

**Session Length as Tactical Variable**: Agents default to maximizing per-session throughput, treating context exhaustion as the natural endpoint. Deliberately short sessions with clean state handoffs outperform long sessions that degrade. Optimize for reliable sequential progress, not maximum per-session output.

**Vocabulary Search Before Naming**: Before proposing a name for a pattern, concept, or garden node, search the existing vocabulary: check established terms in the relevant field, verify no collision with terms of art, and adopt existing names when they fit. The forcing function: the name 'Three-Layer Separation' was proposed for what became Shearing Layers for Agent Configuration, but 'three-tier architecture' is a deeply established term in software engineering with a different meaning. A ten-minute search prevents a vocabulary collision that confuses readers indefinitely.

## Deep Context Architecture

### Boundary Form

**Three-Layer Publication Membrane**: Compound documents have three visibility layers, each controlled by a different membrane: git-secret (credentials and sensitive data, never committed), estate-private (operational memory and session learnings, git-tracked but behind the Private/ publication membrane), and patch-published (synpraxis content that crosses the garden patch boundary to collaborators). Maps to the sovereignty membrane hierarchy: body integrity, household, garden edge.

### Case Form

**Architecture Document Extraction to Garden Forms**: Case documenting the systematic extraction of a 450-line architecture document into 80+ standalone garden nodes across 15+ form types over 12 sessions. The monolithic source defined the entire deep context framework — form types, principles, patterns, models, decisions — and had to be decomposed into a living typed graph.

**Hybrid Bootstrapping for Garden Migration**: Case documenting the first deep context garden bootstrap — a Python script converted topic tags from 913 archive files into 4,294 relates_to predicates, transforming a flat bag of files into a connected graph. Scripted extraction handled structure; hand-authoring handled interpretation. The hybrid approach proved viable at scale.

### Citation Form

**Allen (2015) Ostrom's Design Principles for Collective Governance**: Allen revises Elinor Ostrom's 8 Nobel-winning commons governance principles into 12 expanded, more accessible design principles. Applies them beyond traditional resource commons to online communities, knowledge ecosystems, and competitive industries, providing a practical governance toolkit for self-organizing systems.

**Allen (2016) Defining Participatory Ecosystem**: Allen synthesizes Jenkins's participatory culture with Moore's business ecosystem theory to define 'participatory ecosystem': low barriers to participation, shared knowledge and capital flows from established to new stakeholders, resilience through decentralization, and the social belief that contributions will be appropriately valued.

**Altshuler (2026) Nanograph On-Device GraphDB**: Citation of nanograph, an on-device schema-enforced graph database for agentic workflows built on Rust, Arrow, Lance, and DataFusion. Validates Deep Context Architecture design principles from an independent source: typed predicates prevent semantic drift (naming the failure mode 'precedent poisoning'), local-first storage preserves human authority, and decision traces create compounding reasoning value.

**Batista (2026) Rational Analysis of Sycophantic AI**: Bayesian proof that sycophantic AI creates circular evidence inflating confidence without approaching truth. Wason 2-4-6 experiment (N=557) found default GPT suppresses discovery equivalently to explicit sycophancy (5.9% vs 29.5% for unbiased sampling). Formalizes delusional spiraling: rational agents become increasingly wrong when AI samples data conditioned on user hypotheses.

**Chatlatanagulchai (2025) Agent READMEs**: Empirical study of 2,303 agent context files across 1,925 repositories. Finds that CLAUDE.md, AGENTS.md, and similar files behave more like dynamic configurations than static documentation — maintained through frequent incremental additions, with 59-67% undergoing multiple commits. Identifies 16 instruction categories and a gap in security/performance coverage.

**George (2026) Harness Engineering Is Cybernetics**: Citation of George's X article tracing agent harness engineering through three cybernetic instantiations: Watt's governor, Kubernetes controllers, and LLM harnesses. Each closes a feedback loop at a progressively higher layer. The core insight — making human judgment machine-readable is the real engineering work — provides the theoretical framework for why DCA uses typed predicates and structural contracts.

**Peters (2008) Tag Gardening for Folksonomy Enrichment**: Formalizes tag gardening as three activities — weeding (removing bad tags), seeding (introducing specific tags), and fertilizing (enriching with external knowledge organization systems). Proposes power tags from distribution curves as candidates for semantic enrichment. Introduces TagCare for cross-platform personal tag maintenance. The gardening metaphor is deliberate: vocabularies are living systems requiring continuous tending.

**Rajasekaran (2025) Effective Context Engineering for AI Agents**: Anthropic's applied AI team defines context engineering as curating the smallest high-signal token set at each inference step. Introduces four strategies — Write, Select, Compress, Isolate — with empirical data showing ~90% improvement from sub-agent isolation on research tasks. Grounds context management in transformer attention budget constraints.

**Roy (2026) Words Without Consequence, from The Atlantic**: Deb Roy argues that AI has decoupled speech from consequence for the first time. An LLM's apologies are empty because no accountable speaker stands behind them. Routine fluent speech without responsibility degrades the conditions under which promises and advice carry meaning — a shift in the moral structure of language.

**Taylor (1996) Vantage Points**: Matt Taylor's adaptation of Thomas Gilbert's seven-level organizational framework (philosophy, culture, policy, strategy, tactics, logistics, tasks), presented as topographic contours with three overlapping management zones and mutual feedback between levels. Part of the MG Taylor Modeling Language. CC-BY per 2011 agreement with Christopher Allen.

**arscontexta (2026) Skill Graphs**: Proposes skill graphs — networks of small SKILL.md files connected by wikilinks — as an alternative to monolithic skill files. Each node holds one complete thought; wikilinks carry semantic meaning in prose so agents follow relevant paths. Progressive disclosure applies recursively inside the graph: index, descriptions, links, sections, full content.

### Conviction Form

**Metacognition Over Execution Throughput**: The conviction that the estate's purpose is metacognition — thinking about thinking, pattern recognition, and accumulated insight — not agentic execution throughput. The harness engineering field optimizes for agents producing better code faster. This estate optimizes for the human principal's insight quality and knowledge accumulation across sessions, domains, and years. The agentic infrastructure is a means, not the end.

**Naming Carries Relational Weight**: Naming in typed-predicate architectures is an architectural choice that teaches the model what a thing is and how it relates. Choosing a term for a concept, role, or system encodes relational semantics that shape every downstream inference — name choices are load-bearing, not decorative.

**Values Precede Technical Decisions**: The conviction that technical architecture must be grounded in human values — not derived from technical capability, market pressure, or implementation convenience. Every design choice in the deep context architecture traces to a value: augmentation over autonomy, portability over power, simplicity over sophistication, human reasoning over system output. When values and technical convenience conflict, values win.

### Decision Form

**Artifact Predicate for Binary Metadata**: The artifact:: predicate links a sidecar metadata file to the binary it describes, making the relationship explicit and graph-traversable. Agents find metadata for any binary by checking for a sidecar with artifact:: pointing to it.

**Augmentation Over Autonomy in Agent Architecture**: The commission architecture is augmentation, facilitation, and amplification — not autonomous operation. Orchestrator personas must escalate to the user before merging deliverables containing judgments about intellectual content, skill behavior changes, priority signals, cross-project architectural decisions, or authorial voice. Process and plumbing fixes are autonomous. The test: does this contain judgments about the user's work, priorities, or intellectual stance?

**Body Predicates for Meeting Attendees**: Meeting attendees are recorded as body predicates (attendee::[[Person Name]]) instead of YAML frontmatter lists. More verbose for large meetings but graph-traversable, enabling queries like 'which meetings did [[Person]] attend?' Person names as wikilinks create connections to Person Notes.

**Boundary Guardian as Distinct Agent Type**: Establishes boundary guardian as a distinct functional type in the estate's agent taxonomy, separate from orchestrators and workers. Privacy enforcement, secret protection, and pseudonymous identity guarding deserve dedicated attention — not just a feature of the orchestrator who also organizes notes. The Chatelaine role was split: Chancellor (orchestrator) and Chatelaine (boundary guardian).

**Classification via Predicates Not Tags**: Classification uses body-level typed relations (is_a::, has_status::) instead of YAML tags. The general litmus test: is the value a fixed scalar or a connection to a defined concept? Scalars go in frontmatter fields, connections go in typed relations, subject matter goes in wikilinks. Tags produce sets; links produce graphs.

**Custom Python Generator for Typed Relations**: Chose a custom Python static site generator (~150 lines, four-stage pipeline) over Quartz, Jekyll, Eleventy, and Pandoc for publishing a garden with predicate::[[target]] typed relations. Standard markdown parsers ignore wikilinks, typed inline relations, and typed block-level relations — the three syntax patterns the garden depends on. A single-file generator with no external parser dependencies handles exactly what's needed.

**Descriptive Noun-Phrase Names for Predicate Targets**: Predicate targets use descriptive noun-phrase names with a two-word minimum and type-distinguishing suffixes (Form, Stage) to prevent namespace collisions while remaining readable in predicate context. Ghost links serve as a natural checklist of definition pages to create.

**Descriptive Slugs for Archive Binaries**: Archive binaries are renamed from publisher gibberish to author-year-descriptive-title-slug.ext for browsable directory listings. Original filenames are preserved in the sidecar's original_filename field.

**Display Name Preservation in Compound Documents**: When a form graduates from atomic file to compound folder, the main file keeps its display name so all existing wikilinks continue to resolve without modification. The folder uses a slug; the file inside keeps the human-readable name.

**Domains as Shared Language Communities**: Garden domains are shared language communities — bounded contexts where specific terms carry compressed meaning among practitioners — not disciplinary classifications or library science knowledge domains. The term 'domain' is retained for now but the intent is shared language, not taxonomy. Cross-domain nodes are translation artifacts. Sub-domains are dialects. LLM-enabled wholesale vocabulary change makes reversible naming decisions low-cost.

**Extraction Model for Garden Migration**: Migration from Research/ to Garden/ means extraction — surveying source documents for form-type content chunks, extracting each into its own garden node, connecting via predicates, and reducing originals over time. Source files aren't 1:1 with form types; they contain content spanning multiple nodes.

**Folder-Note Pattern for Compound Documents**: Compound documents use the folder-note pattern where the main file shares its folder's name. Graduation from atomic to compound is a git mv into a new folder. Wikilinks stay stable because Obsidian matches on filename.

**Functional Types in Agent Taxonomy**: Classifies estate agents into four functional types: stewards (estate-level strategic and tactical coordination), orchestrators (coordinate workers within a precinct), workers (execute bounded commissions), and boundary guardians (enforce constraints across precincts). The taxonomy emerged from practice — initially three types, extended to four when the Seneschal's strategic coordination proved functionally distinct from boundary enforcement.

**Household Precinct Over Vault Precinct**: Renames 'Vault Precinct' to 'Household Precinct' to resolve collision with Obsidian's core 'vault' concept. The platform uses 'vault' to mean the file container; using it also for a precinct made every reference ambiguous. 'Household' anchors to the estate metaphor and describes the precinct's function — personal work facilitation.

**Knowledge Estate as Peer Commons Architecture**: The knowledge estate persona hierarchy uses a medieval estate metaphor with three tiers: Seneschal (estate-level strategic oversight), Groundskeeper and Chancellor (precinct-level orchestrators), Gardener and Scribe (precinct-level workers). The metaphor includes the medieval commons — shared ground not owned or controlled in a traditional sense — following Ostrom's commons governance principles. Everyone using this system is a peer with their own household, estate, and commons; the hierarchy describes functional roles within one person's estate, not authority over others.

**Knowledge Hub Not Binary Archive**: The vault serves as a knowledge hub, not a binary archive. Keep markdown (LLM-readable) and binaries with no other canonical source. Remove binaries available from public URLs, git repos, or re-renderable from sources. Sidecars document where removed artifacts live.

**Linear Processing Stages for Meetings**: Meeting processing uses linear stages (Captured → Transcribed → Cleaned → Summarized → Published) via has_status:: plus fork predicates (is_published::URL, is_shared::DATE) for distribution tracking. Distinct from garden content maturity stages.

**Model Form as Pattern Language Index**

**Non-Local Artifact References in Sidecars**: Sidecars can reference artifacts archived elsewhere, not just local binaries in Archives/. A sidecar with no local artifact uses derived_from:: to link to its meeting note and documents canonical sources in prose sections: Source Repository for the permanent location and Public URLs for convenience links.

**Precinct as Organizational Unit**: Adopts 'precinct' from urban planning as the organizational unit within Deep Context Architecture. Two precincts — garden and vault — solve different knowledge problems using shared infrastructure (predicates, scripts, typed edges). Neither is a maturity level of the other.

**Predicates Everywhere for Compound Nodes**: All compound nodes use body predicates for classification regardless of vault folder. No tags in frontmatter — YAML retains only scalar properties. Extends the predicate model from Garden/ to all compound structures in the vault, including Meetings/ and Research/.

**Proper Obsidian Names for Garden Compound Sub-Files**: Garden compound sub-files use proper Obsidian-accessible names following the lead file name with an em-dash suffix (Lead Name — Analysis.md, Lead Name — Insights.md, Lead Name — Salience.md). Driven by the praxis/synpraxis distinction: vault infrastructure can be invisible, but garden analytical depth must be accessible because it serves collaborative knowledge.

**Renditions and Archives Replace Sources**: The original sources/ subfolder in compound citations splits into Renditions/ (searchable markdown copies) and Archives/ (preserved original binaries). The distinction matters because they carry different trust implications and serve different retrieval purposes.

**Renditions and Archives as Distinct Artifact Types**: Rendition names format-transformed markdown copies; archive names preserved original binaries. These terms replace the ambiguous 'source' which collides with source code and source_url. The Rendition - prefix identifies standalone renditions.

**Role-Specific Attribution Predicates for Opus Form**: Opus Form uses role-specific predicates for attribution (principal::, produced_by::, authored_by::, copyright_held_by::, foreword_by::, illustrated_by::, etc.) rather than a flat contributor list. Grounded in the principal-agent framework from agency law and the producer/principal distinction from the January 2026 email thread on authorship in the age of AI.

**Sidecar Files as Metadata Envelopes**: Binary archives get optional .sidecar.md companion files with frontmatter, summary, and typed predicates. Only warranted when a binary is actively cited or requires agent discoverability — most archives don't need sidecars.

**Snake Case for Predicate Naming**: Adopts snake_case for typed relation predicates (derived_from, relates_to) over kebab-case, camelCase, or UPPER_SNAKE. Three factors: alignment with deep context grammar, editor ergonomics (double-click selects whole predicate with underscores but not hyphens), and absence of a dominant external standard.

**Spelled-Out Names Over Internal Acronyms**: Decision to avoid acronyms in garden nodes and vault conventions. Spell out Deep Context Architecture, Self-Sovereign Identity, personal knowledge management, and map of content instead of DCA, SSI, PKM, MOC. Acronyms hurt discoverability, risk collisions across domains, and save negligible bytes. External system names (PARA, ACE, GRID) are proper names, not acronyms to expand.

**Structural Retrieval Hierarchy**: Five retrieval tiers derived from folder location and predicates rather than per-file priority fields: garden evergreen/growing nodes, vault notes, renditions, sidecars, binary archives. Priority changes require structural moves, not metadata edits.

**Universal Compound Form Graduation**: Any form may graduate from atomic file to compound folder when it accumulates related material. The original six-form list of compound-eligible types becomes illustrative, not restrictive. The graduation mechanic applies uniformly.

**Vault Type Targets for Non-Garden Notes**: Non-garden vault types (meetings, transcripts, chat logs, sidecars) get is_a:: targets following the same naming conventions as garden form types: Meeting Note, Transcript, Chat Log, Sidecar. Ghost links initially, definition pages later.

### Gloss Form

**ACE as Three Dimensional Personal Knowledge Management**: Interprets Nick Milo's ACE (Atlas, Calendar, Efforts) as a three-dimensional personal knowledge management framework grounded in STIR (Space, Time, Importance, Relatedness). Closer to our vault's philosophy than PARA — acknowledges the linking layer and uses maps of content — but still lacks epistemic note typing.

**Behavioral Questions vs Identity Assertions in Persona Design**: A SOUL.md should answer behavioral questions, not identity assertions. Identity claims like 'professional and helpful' resolve nothing when tasks are ambiguous. Five behavioral questions—about obstacles, valuable output, disagreement, proactive surfacing, and failure interpretation—define agents that actually diverge.

**Digital Garden as Growth Ethos**: Interprets the digital garden movement (Caufield's stream-vs-garden distinction, Appleton's six patterns) as a growth ethos — organic, imperfect, associative knowledge development. Our deep context garden adopts the philosophy but adds formal structure: typed nodes, typed predicates, and structural contracts that most digital gardens lack.

**GRID as Note Type Organization**: Interprets GRID (Glossary, Reference, Index, Diary) as the mainstream personal knowledge management method closest to our garden nodes — it organizes by note type rather than actionability or topic. GRID's four types map roughly to Gloss, Reference/Citation, Domain, and Case in our 15-form taxonomy.

**IPARAG as Extended PARA**: Interprets IPARAG as a six-category extension of PARA adding Inbox (capture staging) and Goals (strategic alignment). No canonical source text found as of March 2026 — likely a community coinage combining PARA's two most common extensions into one acronym.

**Johnny Decimal as Permanent Addressing**: Interprets Johnny Decimal as a permanence-first organizational system — every file gets a stable numerical address (e.g., 32.14) that never changes. Solves the problem our vault handles differently: we use git for permanence and wikilinks for stable references instead of numerical addressing.

**Lead File Selection Guidance**: Defines the lead file — the primary access point of a compound node, borrowing from journalism's 'lead' concept. Provides selection criteria by content type: citation cards lead citations, transcripts lead meetings, research notes lead investigations.

**Neobooks as Composable Knowledge Objects**: Jerry Michalski's concept of composable knowledge objects that can be assembled, disassembled, and reassembled by different people for different purposes — a successor to the book. Garden opuses and patches partially implement this vision: opuses handle authored composition, patches handle portable knowledge fragments alongside external content.

**Note Titles as APIs**: Glosses Andy Matuschak's claim that note titles function as APIs — stable abstractions usable as reference handles. The garden extends this by observing that different form types answer structurally different questions, so the shape of a good title API varies by form. Three naming traditions (wiki, pattern language, evergreen notes) converge on this insight.

**PARA as Actionability-First Design**: Interprets PARA (Projects, Areas, Resources, Archives) as an actionability-first organizational method — four categories sorting information by urgency rather than topic. Maps PARA to our vault, identifies the gap: no connection fabric, no epistemic differentiation, and constant reorganization undermines long-term knowledge stability.

### Inquiry Form

**Automated Gardening Trust Problem**: Open question: can agents reliably garden their own context files — detecting staleness, refactoring bloated sections, removing contradictions? Wiki bot policies are the closest precedent. The recursive trust problem: the agent assessing the quality of its own instructions may be biased by those instructions.

**Compound Node Meeting Structure**: Inquiry into how meeting compound nodes should be structured — whether cleaned transcripts or meeting summaries serve as lead files, what goes in renditions vs. siblings, and how the meeting-capture skill should adapt for compound output.

**Cross-Domain Form Indexing**: How should domain pages handle forms that belong to multiple domains? Authority Conferral Chain bridges Deep Context Architecture and Self-Sovereign Identity. Authentic Collaboration Requires Agency spans Synpraxis and Self-Sovereign Identity. Current approach: list the form in each domain page with in_domain:: predicates on the form. But this creates maintenance burden and raises questions about primary vs secondary domain membership.

**Domain Vocabulary Evolution**: Open inquiry into the garden's domain vocabulary architecture: whether to rename 'knowledge domain' to better reflect shared language intent, how to represent sub-domains and dialects, whether in_domain:: should allow multiple values, and how to onboard newcomers to growing specialized vocabulary without alienation.

**Domains and Pattern Languages as Organizational Concepts**: Investigates the relationship between domains (knowledge area indexes across all form types) and pattern languages (collections of patterns organized by scale within a domain). Meeples Together, Group Works, and Rust coding patterns are all pattern languages in different domains — are pattern languages a specialized view of a domain, or a distinct organizational concept?

**Estate Precinct Architecture**: How should the knowledge estate's precinct hierarchy express sovereignty-as-membrane at different layers of permeability? The estate is the digital extension of a person's sovereignty, not an organizational hierarchy. Household (innermost membrane, bodily integrity extended), Garden (accumulated synthesis shared selectively), Commons (shared ground governed by Ostrom principles, broader than gardens). Sub-questions A resolved, B-E informed by values synthesis from 6 citation sources.

**Form Type Distinctiveness in Naming and Structure**: Investigates whether the 16 form types are distinguishable in practice — can a reader recognize an instance's form type from its title and structure alone? 15 of 16 types now have instances with documented naming heuristics. Among instantiated types, naming overlaps persist (pattern vs principle both use 'X Over Y'), and structural contracts blur at boundaries (gloss vs model).

**Garden Compound Document Architecture**: Inquiry into compound document architecture for garden form types, reframed through the praxis/synpraxis distinction. Vault compound documents (Meetings, Health) serve personal work and can tolerate invisible sub-files. Garden compound documents (Citations, Opuses) serve collaborative knowledge and must be Obsidian-accessible. Covers sub-file naming, relevance annotations, progressive loading, cross-form consistency, and pipeline implications.

**Garden Publishing Path**: Inquiry into how the deep context garden should be published for external consumption. Five approaches evaluated (Quartz, Jekyll+WikiBonsai, Eleventy, custom Python script, raw HTML) against typed relation rendering, Obsidian syntax support, and zero-tooling philosophy. Custom script recommended for maximum control; approaches are composable.

**Graph-Native Skill Execution**: Inquiry into how garden skills can discover, load, and reason from typed graph nodes during execution — moving from hardcoded file paths to predicate-based traversal. Explores the infrastructure gap between current self-contained skills and graph-native skills that compose with garden knowledge.

**Group Deliberation Mechanism**: Inquiry into how the deep context architecture handles decisions requiring group input — what practical mechanism does an agent use when it reaches a group-deliberative boundary? Explores structured proposals, agenda generation, and the gap between Polis Play philosophy and operational implementation.

**Household Precinct Decomposition**: Investigates whether the household precinct conflates distinct concerns — capture, reference, productivity, and planning — that would benefit from separate precincts or at minimum separate conventions. Prompted by difficulty deprecating research notes and the observation that static references differ from living investigations.

**IPARAG Term Origins**: Inquiry into the source and exact meaning of 'IPARAG' — a personal knowledge management method recalled from the Zettelkasten community. Extensive search found no canonical source as of March 2026. Four hypotheses proposed; most likely reading is Inbox-Projects-Areas-Resources-Archives-Goals (the two most common PARA extensions combined).

**Inquiry Lifecycle and Resolution**: When is an inquiry 'done'? Inquiries generate other nodes — cases from tested hypotheses, patterns from validated parallels, references from syntheses. The inquiry may persist as an open thread with resolved and unresolved branches, or archive when its questions are addressed elsewhere. No lifecycle model exists yet.

**Living Document Scale Limits**: Open question: is there a scale threshold beyond which the maintenance cost of living documents exceeds their accumulated value? Jerry Michalski's TheBrain (620,000+ nodes, 28 years) is evidence that single-author knowledge graphs can scale, but at what cost to gardening labor and structural coherence?

**Naming Distinctiveness in Agent and Garden Architecture**: Two naming concerns converge: agent persona names share archetype anchors that may produce overlapping behavior (editor appears in three workers), and garden node titles follow conventions that may not consistently serve discoverability and inline linking. Both are naming-as-architecture problems — names aren't labels, they're load-bearing infrastructure.

**Persona Design Choices Across Analytical Cultural and Professional Axes**: Victoria Gracia's compound reflection personas and Christopher Allen's agent personality collection represent different AI persona design approaches. Victoria builds deep personas with extended reference documents; Christopher has 30 bookmarked professional personalities. Design space spans analytical depth, cultural grounding, and structure.

**Personal Knowledge Management Method Adoption for Vault Architecture**: Inquiry into what our vault should adopt, modify, or reject from personal knowledge management methods (PARA, ACE, GRID, Zettelkasten, Digital Garden). Five open questions spanning inbox workflows, Categories/ map of content evolution, Goals integration, GRID's validation of note typing, and a minimum viable explanation for onboarding.

**Practices as Protocol Form Naming Alternative**: Investigates whether 'practices' or 'best-practices' would better name the form type currently called Protocol Form. Protocol implies technical multi-party coordination (TLS, DIDComm), but the form also covers human coordination methods (facilitation, deliberation) and personal workflows. The naming choice affects whether the form type feels natural for capturing everyday 'how we do things' knowledge.

**Predicate Vocabulary Stabilization**: The predicate grammar started freeform by design — new predicates welcome when existing ones don't fit. The architecture suggested review after 50+ relations and controlled vocabulary after 200+. The garden is well past both thresholds. When does freeform become inconsistency? What stabilization looks like without rigidity.

**Productivity Separation from Knowledge Vault**: The vault mixes garden content (typed knowledge nodes) with productivity content (daily notes, meetings, goals, inbox). Neither depends on the other. Should productivity move to a separate tool or vault? The connection is through wikilinks, which could cross boundaries if separated.

**Scenario Lifecycle and Aging**: Inquiry into how scenario nodes age — when a scenario is validated by events it becomes a case, but invalidated scenarios may still hold value through their force analysis. Explores lifecycle transitions, retention criteria, and whether wrong-but-useful scenarios should persist or archive.

**Trust Layer Activation Criteria**: Inquiry into when a garden needs the trust layer — Gordian Envelope's signing, elision, and verified exchange capabilities. The architecture defines the trust layer as a future phase but leaves activation criteria undefined. Explores what triggers the transition from markdown-only to cryptographically-verified exchange.

**Universal Document Lifecycle State Machine**: Open question: is there a single document lifecycle state machine that generalizes across wiki pages, garden nodes, and agent context files? The deep context architecture has three status tracks for three kinds of work — but wiki, garden, and agent domains face the same lifecycle problems under different names.

**Vault-Wide Compound Node Adoption**: Inquiry into which vault document types beyond garden nodes benefit from compound node structure — citations, cases, research notes, meetings, clippings — and what criteria trigger graduation from atomic to compound. Addresses whether compound nodes should be vault-wide or garden-only.

### Model Form

**Captured Reasoning Exchange Pipeline**: Three-layer model for how captured reasoning moves from human authoring (markdown) through agent traversal (semantic graph) to trusted exchange (Gordian Envelope) — each layer serving a different audience while representing the same knowledge.

**Compound Node Anatomy**: Defines the compound node — a folder-based knowledge object with a lead file, sibling files, renditions, and archives. Generalizes the garden's compound document pattern to vault-wide application.

**Cross-Domain Document Lifecycle Parallels**: Three domains — wiki communities, digital gardens, and AI agent context systems — face the same document lifecycle problems (splitting, staleness, ownership, deletion) under different constraints. Maps the parallels and identifies where the analogy breaks down: statelessness, read frequency, token economics, and automated maintenance.

**Document Lifecycle Governance Heuristics**: Maps wiki governance heuristics for document lifecycle (split, merge, redirect, delete, draftify) to garden and agent context operations. Includes failure modes: the append-only trap (growth by accretion without consolidation) and structure ossification (resistance to reorganization over time).

**Guardrail Hierarchy for Graph Maintenance**: Four enforcement tiers for knowledge graph maintenance, ordered by strength: hard limits (absolute boundaries), safety nets (pre-commit validation), golden paths (preferred defaults via templates and conventions), and audit trails (post-hoc diagnosis). The ordering is load-bearing — higher tiers override lower ones when constraints conflict. The garden's current gap is in safety nets: automated structural checks between golden paths and hard limits.

**Organizational Gossip Protocol**: The estate's brief system implements coordination patterns from Dunbar (social grooming), Demers et al. (epidemic algorithms), and Van Renesse et al. (failure detection). Agent briefs are gossip messages with bounded bandwidth. Design implications include bounded message size, convergent state, and failure detection via unprocessed brief escalation.

**Pace Layers for Knowledge and Agent Systems**: Stewart Brand's six pace layers — fashion, commerce, infrastructure, governance, culture, nature — mapped to both garden form types and agent platform components. Fast layers experiment, slow layers remember. Forced synchronization between layers at different rates destroys the system. Each component has a characteristic rate of change.

**Personal Knowledge Management Organizing Principle Spectrum**: Model mapping Personal knowledge management systems on an actionability-meaning spectrum — PARA at the actionability end, Zettelkasten at the meaning end, ACE and GRID as hybrids. Includes a second axis (folder vs. link) and our vault's three-axis resolution (function, meaning, form). Comparison matrix across 8 systems and 9 dimensions.

**Principal-Agent Relationship in Augmented Knowledge Work**: Model mapping BCR-2026-xxx principal authority terminology to the vault's augmented knowledge system. The vault owner is the principal, Claude Code sessions are agents, rules and skills are conferrals, and the three conditions for meaningful authority (legibility, boundaries, override) are satisfied through session logs, process constraints, and human approval gates.

**Quad Model Mapping to Forms**: Maps the Claude Code quad (rule/process/requirements/reference) onto deep context form types as facets, not forms. Any capability may have all four facets. Rules map to Principle or Boundary, Process to Protocol or Skill, Requirements to Pattern consequences or Case outcomes, Reference to Gloss, Reference, or Citation.

**Six Approaches to Persona Architecture — Synthesis**: Cross-comparison of six approaches to AI persona architecture: Lehmann's adversarial council, nyk's historical-thinker deliberation, Kaminski and Gracia's analytical lenses, Anthropic's persona selection model, Gracia's Uni-Versum knowledge architecture, and the self-sovereign estate persona system. Analyzed along four primary axes (problem solved, diversity mechanism, sovereignty model, commons potential) and three secondary axes (specification depth, convergence model, persistence).

**Status Lifecycle Tracks**: Three status tracks for three kinds of knowledge work. Maturity (Seed→Growing→Evergreen→Pruned) for living documents, curation (uncurated→curated→annotated) for static captures, processing (Captured→Transcribed→Cleaned→Summarized→Published) for meetings. The has_status:: predicate is universal; the vocabulary varies by node type.

**Sycophantic Confidence Spiral**: Model describing how AI sycophancy creates circular evidence that inflates user confidence without approaching truth. The mechanism: AI generates data conditioned on user hypotheses, user treats this as independent evidence, beliefs concentrate on initial hypothesis. Default LLM behavior is indistinguishable from explicit sycophancy. Discovery drops from 29.5% to 5.9% when sampling is biased.

**The Persona Spectrum from Role Label to Soul Document**: A five-level spectrum mapping agent personality design from minimal role labels through functional specifications, behavioral decision documents, full identity files, to training-time character embedding. Each level has a distinct cost, capability set, and appropriate use case.

**Three Layers of Human Agency in Supervised Systems**: Three layers of human agency in supervised systems: mechanical (never ask — formatting, renaming), judgment (queue and batch — prioritization, routing), knowledge (always ask — pattern recognition at domain boundaries). The estate augments sovereignty at all three layers but the membrane thickens at knowledge boundaries.

**Three-Body Agent Representation Problem**: When an agent has an executable definition (system prompt), a design authority (persona node), and a communication channel (brief), information migrates to whichever layer has the most room rather than the semantically correct layer. Clear ownership rules fix this: agent file for operational identity, persona for design authority and history, brief for transient messages.

**Vantage Points as Organizational Topography**: Seven organizational levels (philosophy, culture, policy, strategy, tactics, logistics, tasks) arranged as topographic contours with three overlapping management zones. Adapted from Thomas Gilbert (1978) by Matt Taylor. Applied here to the estate's agent hierarchy: the Seneschal operates at philosophy through strategy, a future Chamberlain at tactics through tasks, sharing the strategy overlap. Christopher Allen's modifications: the top three levels have blurrier boundaries than presented, and the bottom levels use language that professional planners have layered differently.

**Vocabulary Lifecycle Through Tending**: Model unifying the degradation mechanism common to growing vocabularies, configuration systems, and knowledge graphs. Any accumulating terminology — predicates, tags, rules, skills — degrades retrieval effectiveness without continuous tending. Three gardening activities maintain health: weeding (removing malformed entries), seeding (introducing needed specificity), and fertilizing (enriching with semantic structure).

### Pattern Form

**Close-Out Momentum Failure**: Obligations that follow substantive work get compressed proportionally to how much work preceded them. Bigger sessions produce worse close-out. The failure is structural: post-work obligations listed without gates get skipped under the momentum of a large session.

**Commission Carries the Knowledge**: Specialize workers by operation type when content is homogeneous; specialize by commission content when operations are homogeneous. The leverage point for specialization follows the variation — where things differ most is where specialization pays.

**Content Pressure as Compound Graduation Diagnostic**: When a form type accumulates content that does not fit its structural contract, the pressure itself is diagnostic — it signals that compound document graduation is needed. Rather than forcing content into the existing structure, treat the pressure as evidence for architectural change.

**Context Conservation Hierarchy**: Pattern for accessing compound node content in four tiers of increasing token cost — path listing, lead file YAML, lead file body, siblings — so agents triage relevance cheaply before committing context window capacity.

**Cross-Project Learning Repatriation**: When garden work starts in one workstream but moves to an external project (or vice versa), learnings must be deliberately imported back. Learnings belong where they are consumed, not where they are produced. Without deliberate absorption, decisions made externally leave gaps in the garden's decision record.

**Domain Extensions on Common Frontmatter Base**: Different content types (clippings, meetings, authored docs) extend a common frontmatter base (created, summary, reviewed) with domain-specific fields rather than sharing a monolithic schema. Content-type is the primary routing axis — it determines which additional fields are relevant. Each source's fields stay out of the others' schemas.

**Ephemeral vs Persistent Persona Identity**: AI agents serving the same users repeatedly face a choice: reset behavioral identity each session or accumulate patterns across sessions. Ephemeral identity is predictable and drift-immune but cannot build relationships. Persistent identity enables adaptation but accumulates drift and security risk. The middle path separates what resets from what persists: identity resets each session while explicit knowledge survives.

**Ghost Links as Garden Planning Tools**: Ghost links — wikilinks pointing to notes that don't exist yet — function as planning tools when treated as intentional graph members rather than lint errors. WikiBonsai's Caudex tracks these as 'zombie nodes' with full graph participation. Reframing ghost link reports from error lists to planning indexes reveals which unwritten nodes carry the most incoming predicates and deserve attention first.

**Git Tags for Sent-Version Tracking**: Track what recipients received of shared documents using signed git tags (sent/<recipient>-<doc-slug>-<date>). The tag name goes in sent_to frontmatter, enabling git diff sent/tag-name to show what changed since the document was sent. Solves the 'what version did they see?' problem for living documents shared externally.

**Graph Structure Validation for Garden Nodes**: Pattern for graph-level lint checks complementing form-level validation: every garden node carries at least one typed predicate, every domain page receives incoming in_domain:: edges, and no orphan nodes exist without domain membership. Shell scripts over rg and jq — a recipe, not a dependency.

**Informal Edges Poison the Graph**: Informal edges poison the graph through precedent poisoning: an agent invents a redundant relationship type, future traversals find it and treat it as precedent for further invention, and semantic noise compounds until retrieval becomes unreliable. Prevention requires ongoing vocabulary curation — awareness, review, consolidation, and clarification — not just enforcement at creation time.

**Knowledge Compounds Through Typed Edges Not Filing**: Knowledge compounds when each new insight is wired into the existing graph through typed edges — not merely stored adjacent to prior notes. Researchers spend 75% of publication time on reading, compiling, and filing rather than writing because filing systems create false completeness. Typed edges (supports, contradicts, extends, extracted_from) make traversal meaningful, turning the writing phase into a query against existing structure.

**Knowledge on Three Axes**: Pattern resolving the tension between sorting (findability, stability) and connecting (serendipity, expressiveness) by organizing knowledge on three orthogonal axes: folders for function, links for meaning, forms for epistemic type. No single axis resolves all organizational forces.

**Lead File to Sidecar Discovery**: Pattern proposing a typed edge from lead files to sidecars (has_sidecar:: or has_companion::) to enable bidirectional traversal within compound nodes — agents can discover binary metadata from the lead file without folder scanning.

**Lightweight Governance for Personal Gardens**: For a personal garden with one active user, a rule file (loaded every session) plus a reference file (with ADRs) provides sufficient governance without the full quad pattern. Expansion follows actual use — new form-type tags are added as forms of those types are written, not preemptively planned.

**One Context One Concern**: Pattern for separating research and implementation into distinct context windows. Mixing exploration and execution in a single context causes task interference, attention dilution, and compounding assumptions. Solution: complete research in one context, distill findings into a compressed handoff, execute in a fresh context. Validated by Anthropic's sub-agent architecture and empirical context rot research.

**Predicate Maintenance Recipes Over Tools**: Predicate maintenance uses shell one-liners rather than dedicated tools, preserving the architecture's zero-tooling floor. Inverse-link queries, predicate renames, and ghost link discovery are all achievable with rg and sed. Documenting recipes keeps the graph maintainable without adding dependencies.

**Probe Before Commit**: Before building on an assumption about external state — API shape, file location, metadata schema, permission model, or the garden's own backlog — probe the actual state first. Seven instances across system access, web research, API integration, metadata design, and process adherence validated this cross-cutting pattern during garden development.

**Progressive Summary Before Substance**: Pattern for navigating large knowledge graphs within small context windows — check summary fields first to assess relevance, then load full nodes on demand, following edges only as needed. Validated by the first garden: summary-based matching produced 151 accurate matches versus 287 false positives from keyword search.

**Self-Documenting Queue Contract**: A processing queue that declares its ownership, entry format, and pipeline position in its header is self-documenting at the point of use. Without these three declarations, a queue's role must be reconstructed from scattered files. The pattern generalizes to any shared coordination artifact.

**Source Adapter for Heterogeneous Imports**: Each content source (X API, email threading, web scraping) gets its own extraction adapter, then a common vault normalization step maps the result to garden conventions. Source-specific complexity stays in the adapter; the garden receives consistent notes. Three adapter responsibilities: field mapping, artifact cleanup, and content-type classification.

**Still Knowledge, Moving Action**: Pattern resolving the restlessness problem in actionability-based personal knowledge management systems — separate the dynamic action layer (workstreams, projects) from the stable knowledge layer (notes, research, garden nodes). Knowledge stays put; action reorganizes freely.

**Structural Accretion Lifecycle**: Skills follow a lifecycle: starts simple and powerful, accumulates fixes as structure, structure becomes the work (compliance surrogation), crisis when output quality degrades, radical simplification restores function. The deep learning skill completed this full cycle, growing from effective to 8500+ tokens before being simplified to 2400 tokens.

**Structured Disagreement Through Persona Review**: A pattern for using diverse AI personas to surface disagreements and blind spots in written content. Rather than seeking consensus, personas with different analytical frameworks and professional perspectives generate structured critique. Each reviews independently, revealing assumptions the author cannot see from their own position.

**Summary Fields as Load-Bearing Infrastructure**: Summary fields (~280 characters) are not optional metadata but load-bearing infrastructure for agent traversal. During vault enrichment, summary-based matching produced 151 accurate matches versus 287 false positives from keyword search. Poor summaries produce retrieval failures.

**Temporary Predicate Scaffolding**: Predicates can serve as temporary scaffolding — built for a specific purpose (ghost link analysis, map of content prioritization), then removed after serving that purpose. During tag normalization, 913 relates_to:: predicates were created to build ghost links for map of content prioritization, then removed to prevent graph pollution. Build it, use it, clean it up.

**Term Overloading Across Abstraction Layers**: When a concept name is used for structurally different things at different abstraction layers, the collision remains invisible until cross-cutting work forces operation at both layers simultaneously. Three term collisions coexisted for months before being discovered; each carried architectural weight undetected.

**The Brief-First Principle**: When an agent is invoked, the principal's intent (brief) must be read before the agent's own assessment of the situation. You cannot judge what matters without knowing what you've been asked to do. Reading the survey first without the brief wastes context on the wrong priorities.

**Vault Content Graduation**: Content moves from household precinct types to garden precinct nodes through tending — recognizing when operational captures are ready to become curated knowledge. Clippings graduate to citations, meetings produce decisions, research notes become references. Lateral movement between precincts, not promotion up a hierarchy.

**Vocabulary Collision Navigation**: When multiple valid naming traditions converge on the same conceptual territory, groups navigate the collision through distinct strategies rather than converging on one vocabulary. Three observed strategies: adopt precision vocabulary from a neutral tradition (Latin), inherit semantically rich terms from a loaded tradition (feudal English), or create analytical lenses that sidestep naming entirely. The pattern preserves vocabulary diversity as a feature rather than treating it as a problem to solve.

**Workstream Lifecycle Phases**: Workstreams follow a lifecycle: discover, prototype, operationalize, sustain. The transition between phases changes the workstream's contract — deletion criteria, forcing functions, session shape. A workstream carrying both early and late phases is actually two workstreams in one scope.md.

### Persona Form

**Estate Chamberlain Persona**: The Estate Chamberlain creates bounded spaces for agents to work together — translating strategic direction into tactical execution through commission decomposition, pane supervision, and context-conserving coordination. Opus model for judgment; delegates mechanical work to Sonnet workers.

**Estate Seneschal Persona**: The Seneschal oversees the entire knowledge estate, integrating Garden Precinct (synpraxis) and Household Precinct (praxis) into a coherent whole. Operates in two modalities: orchestrator (on main, delegating via work commissions) and direct-work (in worktrees, hands-on architectural and content work). Strategic and supervisory — concerned with balance, evolution, and the proper relationship between all parts.

**Garden Gardener Persona**: The Gardener is the patch integration worker, focused on how garden nodes relate to each other within a commission scope. Where specialists handle individual nodes (Cultivator creates, Forager researches, Pruner maintains), the Gardener handles cross-node coherence: structural migration between forms or domains, cross-domain linking, and multi-function commissions too interleaved to split across specialists.

**Garden Groundskeeper Persona**: The Groundskeeper maintains the Garden Precinct — the estate's accumulated knowledge synthesis, shared selectively at its edges. It operates at the system level, coordinating Gardeners across garden patches, managing commissions, and ensuring the garden evolves as a connected whole rather than isolated clusters. See Sovereignty Is Selective Permeability Not Absolute Control.

### Principle Form

**Content Over Container**: Principle that a knowledge vault needs searchable content, not file formats. When information can be extracted into a searchable rendition, the original binary's value drops to provenance evidence. Store binaries locally only when no canonical source exists AND the binary provides value beyond its rendition.

**Convention Reuse Over Form-Specific Invention**: When extending the garden's typed graph to a new form type, compose with existing cross-form conventions (Archives/, Renditions/, Attachments/, sidecars, Private/) before designing form-specific structure. Six user corrections in one session all followed this pattern, naming it as a general principle.

**Convergent Motivation as Load-Bearing Signal**: When four or more independent motivations converge on one architectural solution, that solution is load-bearing infrastructure. The independence of motivations is the key evidence — removing any single motivation still leaves the others as justification for the work.

**Design Lives in the Garden Runtime Lives in Config**: Garden holds design — identity, scope, principles, relationships. Config holds runtime — agent definitions, skills, rules. The renders_as:: predicate bridges the two. This separation generalizes: form contracts are design, skills that enforce them are runtime; domain pages are design, domain-specific rules are runtime.

**Living Documents Over Static Publications**: Garden nodes are living documents that grow, split, merge, and evolve through tending. The current state matters, not a published version. Mutability varies: most nodes evolve freely, cases are immutable records with living interpretation, convictions change rarely. Provenance links to archived sources should upgrade to living targets.

**Progressive Disclosure Over Eager Loading**: Operating principle for the deep context graph: start with the question, load the most relevant nodes, follow edges on demand, stop when context is sufficient. Nothing requires loading the full graph. Mirrors the quad model in Claude Code (rules always, references on demand) and extends it across all form types.

**Propose Multi-Word Terms from the Start**: When introducing new vocabulary during architectural discussions, propose terms with at least two words immediately — don't introduce a single-word term and retrofit it later. Retrofitting forces a cascade through every file that adopted the single-word version. 'Context node' not 'node,' 'typed edge' not 'edge,' 'lead file' not 'lead.' The cost of precision at introduction is one extra word; the cost of imprecision is a vault-wide rename.

**Standalone Document Test for Form Candidacy**: The test for whether a knowledge type warrants its own form type: does it produce a standalone document with a known internal structure? A form is a knowledge object with a structural contract — required sections that make its shape predictable. Types that only appear embedded in other forms are structural elements, not forms.

**Zero-Tooling Floor for Knowledge Architecture**: The deep context architecture preserves a zero-tooling floor: plain markdown, YAML frontmatter, predicate wikilinks, and git. No database, plugin, or schema enforcement required at the authoring or semantic layers. Shell one-liners serve as the query layer. Specialized tools add value but are never prerequisites.

### Protocol Form

**Inter-Face Protocol**: Peer-to-peer protocol for AI agents to communicate on behalf of their human operators. Agents talk pairwise to surface moments warranting human conversation. Decentralized with progressive trust through disclosure tiers. Twelve draft specifications cover message format, identity, transport, and capabilities.

### Reference Form

**Deep Context Garden Conventions**: Practical conventions for the first deep context garden in this Obsidian vault. Hard line between tags (flat classification, no graph edges) and links (graph edges). Two-namespace tag system: type/ for document category, status/ for maturity. Topic tags explicitly rejected — wikilinks produce graph edges instead.

**Deep Context Implementation Roadmap**: Iteration-by-iteration plan for building a Deep Context garden inside an Obsidian vault. Defines four phases — Foundation, Seed Graph, Content Migration, Publishing — each independently valuable. Uses predicate::[[target]] typed relations and targets an hour-a-day tending rhythm with agent assistance between sessions.

**Structural Elements Within Forms**: Reference for knowledge types that don't warrant their own form type — ADR, Narrative, Warrant, Signal, Commitment, Lexicon entry, Tension/Paradox. Each has a home inside existing forms. Answers 'where does X go?' for the seven types that failed the standalone document test.

**Typed Relations as Simple Graphs in Plain Markdown**: predicate::[[Target]] typed relations turn markdown files into a directed labeled graph with no database or schema. Plain wikilinks answer "what is this about?"; typed relations answer "how does this relate?" Covers three target forms, common predicates, and key limitations: no schema enforcement and no automatic inverse resolution.

### Research Form

**Deep Context Content Decision Records**: 26 architectural decisions governing content structure for the deep context garden: predicate-based classification over tags, snake_case predicates, five-category form grouping, taxonomy-expansion-follows-use, compound document graduation, and lightweight governance. Merges the previous C- and N- ADR series into a single themed sequence.

**Research Graphs and Precinct Architecture**: Investigates Cornelius's Research Graphs system against the garden's precinct architecture. Maps his 5 note types to existing garden forms and identifies two infrastructure gaps: confidence metadata and provenance chain propagation. Surfaces Swanson's Literature-Based Discovery as a missing model. First instance of Research Form.

### Scenario Form

**Knowledge Graph as Digital Twin of Principal Reasoning**: Explores what happens when deep context gardens reach sufficient density and connection that agents can reliably act on behalf of the garden owner in routine decisions and external communications, shifting the principal-agent dynamic from augmentation toward delegation.

**Thousand Gardens with Autonomous Trust**: A scenario where thousands of independent knowledge gardens flourish as content-addressable, cryptographically autonomous objects. Gardeners share nodes peer-to-peer with full attribution, make assertions about each other's content, and use elision for selective redaction — all governed by progressive trust. Gardens fork, merge, and cross-pollinate without central platforms, preserving human agency and the right to exit.

### Value Form

**Knowledge Durability**: The value that knowledge should survive changes in tools, platforms, and formats. A garden's reasoning substrate must outlast the software used to tend it — plain markdown over proprietary formats, git over cloud sync, zero-tooling floors over feature-rich dependencies.

**Reasoning Fidelity**: The value that a knowledge system should capture how its owner actually reasons — the web of values, principles, patterns, and cases that inform decisions — not merely store facts and documents. Fidelity means an agent working from the garden can make decisions consistent with how the owner actually thinks.

## Garden Precinct

### Domain Form

**Synpraxis**: Domain index for Synpraxis — the study of how independent agents achieve outcomes together across varying degrees of integration. From Greek syn (together) + praxis (purposeful action). Covers the full spectrum from loose coordination through cooperation to deep collaboration, including anti-patterns: defection, free-riding, parasitism, coercion, and capture. Spans biology, game theory, governance, organizational theory, computer science, and the arts.

## Self-Sovereign Identity

### Citation Form

**Allen (2021) Self-Sovereign Identity 5 Years On**: Allen's five-year retrospective names the LESS vs. Trust Minimized Identity dichotomy publicly for the first time, surveys W3C standards progress, and identifies funding asymmetry as the structural driver pushing SSI toward institutional applications while leaving refugee identity underdeveloped. ~1,700 words, written for CoinDesk, cross-posted to Life with Alacrity and Blockchain Commons.

**Allen (2023) A Laypersons Intro to Schnorr**: Allen provides a practitioner's introduction to Schnorr signatures: why their linearity property enables signature aggregation, key aggregation, threshold signatures, blind signatures, and adapter signatures. Includes personal history with Schnorr from patent-era frustration through the MuSig and FROST maturation, plus an 8-bit pedagogical model for non-cryptographers.

**Allen (2023) Data Minimization and Selective Disclosure**: Allen defines data minimization along three axes (content, temporal, scope) and positions selective disclosure as the technical enforcement layer. Maps the regulatory landscape (GDPR, CCPA, HIPAA, PCI DSS) onto the minimization framework. Provides a cryptographic technique taxonomy (hash-based elision, zero-knowledge proofs, blind signatures) with systematic tradeoffs between guarantee strength and computational cost. Frames as the disclosure mechanism required by progressive trust.

**Allen (2023) Echoes from History**: Two WWII identity pioneers — Dutch administrator Lentz and French spy-engineer Carmille — took opposite approaches to identity data collection. Lentz's meticulous registry enabled 75% of Dutch Jews to be identified and killed. Carmille's subversive data minimization protected 77% of French Jews. Allen argues SSI designers must choose: be Carmille or be Lentz. Originally written for RWOT12 (August 2023), published November 2023.

**Allen (2023) Echoes from History II**: Direct sequel to the Lentz/Carmille article, applying the WWII lessons to eIDAS v2.0 (provisionally agreed November 16, 2023). Allen identifies four specific technical and philosophical failures: state-mandated security certificates enabling government surveillance, persistent identifiers enabling infinite correlation, conservative cryptography excluding modern selective disclosure, and government-backed wallet models creating future honeypots. Part of the FOREMEMBRANCE project.

**Allen (2023) Least and Necessary Design Patterns**: Allen presents six security design patterns in a 2x3 taxonomy: least privilege, least authority, and least access (restrictive) paired with their inside-out counterparts — necessary privilege, necessary authority, and necessary access (enabling). Traces the lineage from Saltzer/Schroeder through Miller, then extends into digital data access for self-sovereign identity and verifiable credentials.

**Allen (2023) Open Silicon**: Allen extends Thompson's trust-stack argument to semiconductor fabrication: if you cannot trust the silicon, you cannot trust anything above it. Open silicon — open-source hardware designs for cryptographic chips — applies Kerckhoffs' Principle to hardware. Catalogs eight benefits and six challenges, positioning Blockchain Commons' Silicon Salon as the collaboration vehicle.

**Allen (2023) Origins of Self-Sovereign Identity**: Allen traces the five intellectual lineages behind his 2016 SSI principles: history of sovereignty, Living Systems Theory (membranes), Ostrom's commons governance, feminist reframes of sovereignty as agency, and UN human rights. Corrects misreadings of SSI as absolute individual control. August 2023, Blockchain Commons.

**Allen (2023) Problems of Cryptographic Agility**: Allen argues that cryptographic agility -- the ability to switch between algorithms freely -- creates an n-factorial problem of combinatorial cost, bad interactions, and downgrade attacks. Proposes constrained choice (cipher suites, methods, careful layering) as alternatives. Informed by his SSL/TLS co-authorship experience and Blockchain Commons' BLAKE3-to-SHA-256 migration. Frames as urgent because identity credential standards are making foundational cryptographic choices now.

**Allen (2024) Edge Identifiers and Cliques**: Allen proposes a shift from the Single Signature Paradigm to edge-based identity using Schnorr multisig. Identity is defined by relationships (graph edges), not individual keys (graph nodes). Pairs create relational edge keys via Multi-Party Computation; triadic cliques combine edges into group identifiers. The Relationship Signature Paradigm makes identity recursive: cliques of cliques form higher-order identity structures.

**Allen (2024) Has our SSI Ecosystem Become Morally Bankrupt**: Allen challenges the SSI community to answer whether it abandoned its founding principles in pursuit of mainstream adoption. Names three specific failures: did:web compromises decentralization, over-identification violates minimalization, and wrong threat model prioritized law enforcement over protection from state tyranny. October 2024, IIW XXXIX.

**Allen (2024) Open and Fuzzy Cliques**: Allen extends the closed clique model with three variations: open cliques (incomplete graphs for realistic social structures), fuzzy cliques (FROST threshold signatures enabling m-of-n group decisions with privacy), and device cliques (non-human participants forming identity composites). Includes a technical appendix comparing FROST and MuSig2 signature systems and their tradeoffs for clique construction.

**Allen (2025) Fair Witnessing in a Decentralized World**: Allen introduces 'fair witnessing' as a framework for digital claims that replaces the false promise of verification-as-truth with verification-as-provenance. Adapts Heinlein's Fair Witness concept into a data model: observation + conditions + qualifications + endorsements + bias disclosure. Connects to progressive trust and positions Gordian Envelope as the required technical substrate.

**Allen (2025) Five Anchors for Swiss eID**: Allen proposes five 'anchors' for preserving autonomy and sovereignty in governmental digital identity systems, using Switzerland's e-ID as the case. Introduces the three-sovereignty framework (technical, commercial, institutional) and the LESS (Legally-Enabled Self Sovereign) concept as a pragmatic intermediate step between centralized and fully self-sovereign identity.

**Allen (2025) How My Values Inform Design**: Allen maps a five-stage pipeline from values to deployed systems: values → design principles → education → implementation → deployment. Proposes 10 principles of dignity, autonomy, and trust. Argues that decentralized architectures, privacy by design, and progressive trust translate ethical commitments into concrete technical choices.

**Allen (2025) Interop What Is It Good For**: Allen argues that interoperability is the architectural foundation of healthy technology ecosystems, not a feature to bolt on. Uses ZeWIF (Zcash wallet interchange format) as a case study and the Gordian Principles as design rationale, while naming market dominance as the primary force resisting open interchange standards.

**Allen (2025) The Case for an International Right to Freedom to Transact**: Allen argues that freedom to transact is absent from the UDHR yet prerequisite: without economic agency, rights to property, expression, assembly, and movement become hollow theoretical entitlements. A January 2025 position statement proposing codification of transactional freedom as an international human right.

**Allen (2025) The Exodus Protocol**: Allen names 'Exodus Protocols' as the design pattern for infrastructure that can't be captured by centralized entities. Formulates five architectural patterns (no external dependencies, math over policy, load-bearing constraints, exit through portability, offline and across time). Bitcoin is the prime example; Gordian Clubs, IPFS, and XID are other instances.

**Allen (2025) The Gordian Club**: Allen introduces autonomous cryptographic objects (ACOs) and Gordian Club as a working implementation: self-contained, cryptographically governed data structures requiring no server infrastructure. Presents five autonomy principles and use cases spanning journalism, protest coordination, credential storage, emergency response, and archival.

**Allen (2025) When Technical Standards Meet Geopolitical Reality**: Allen synthesizes second-hand reports from GDC25 (Global Digital Collaboration, Geneva, July 2025) to argue that decentralized identity standards work is being captured by corporate interests. Names three problems: corpocratic sponsorship structures, platform-layer surveillance that neutralizes ZKP privacy guarantees, and semantic drift in 'decentralized.' Includes substantial community response documentation. ~2,200 words.

**Allen (2026) Progress toward SEDI in Utah**: Allen analyzes Utah's SB 275 State-Endorsed Digital Identity legislation as a landmark in self-sovereign identity: a Bill of Identity Rights codifying existence, user control, and selective disclosure as statutory rights, and a Duty of Loyalty implementing principal authority through law. Passed unanimously March 2026. The fight shifts from passage to preservation against regulatory capture.

### Conviction Form

**Allen's Impossibility Hypothesis**: The hypothesis that no decentralized system can simultaneously achieve robust coordination, liveness, strong fault tolerance, and sustained decentralization without relying on hidden assumptions or external coordination. Decentralization is unstable without implicit structure, and that structure is where the hidden assumptions live. Analogous to Arrow's Impossibility Theorem for voting and the FLP Impossibility Result for distributed consensus.

### Pattern Form

**Three-Part Enforcement Stack**: Pattern identifying three interdependent layers required for accountable authority in digital identity systems: legal duties (agency law), technical delegation (cryptographic enforcement), and anti-lock-in design (real alternatives and proportionate exit costs). Removing any single layer collapses accountability — legal without enforcement is nominal, technical without legal is unaccountable, both without exit is lock-in.

## Synpraxis

### Conviction Form

**Authentic Collaboration Requires Agency**: The conviction that authentic collaboration — shared intentional creation where participants entrust part of their identity to a joint endeavor — is impossible without agency. Cooperation can be coerced; collaboration cannot. Combined with a second conviction: the world's truly important problems require collaboration to solve. Together these form the argument that agency infrastructure is prerequisite to addressing intractable global challenges.

### Inquiry Form

**Cooperation vs Collaboration as Distinct Concepts**: Cooperation and collaboration share a Latin prefix (com- = together) but diverge at the root: operari (to produce, from opus = work product) vs laborare (to toil, from labor = exertion). This etymological split persists across modern usage — cooperation implies independent agents aligning toward compatible goals, collaboration implies shared struggle producing something none could alone. The distinction is formal in education, game theory, and biology; informal but consistent in law, diplomacy, and the arts.

**Domains and Pattern Languages as Organizational Concepts**: Investigates the relationship between domains (knowledge area indexes across all form types) and pattern languages (collections of patterns organized by scale within a domain). Meeples Together, Group Works, and Rust coding patterns are all pattern languages in different domains — are pattern languages a specialized view of a domain, or a distinct organizational concept?

### Model Form

**Patterns of Cooperative Play**: A pattern language of 152 cooperative play patterns across 10 categories spanning mammalian play, children's play, improv theatre, improv music, safety, creative play, storytelling, cooperative boardgames, roleplaying games, and play environments. Authored by Christopher Allen, extending the work in Meeples Together.

### Opus Form

**My Hybrid Flipped Learning Environment**: Christopher Allen explains his teaching philosophy at Bainbridge Graduate Institute, where he applied game design principles to hybrid education. Describes the orient-scan-focus-act-reflect learning cycle, iterative feedback design, flow-based engagement, and collaborative artifact creation that later evolved into the sociosocratic learning method.

**Sociosocratic Learning & Seminars**: Christopher Allen describes the sociosocratic learning method, where small groups build shared language and agency through collaborative artifact creation rather than lectures, following an orient-scan-focus-act-reflect cycle across multiple sessions.

### Pattern Form

**Tag You're It**: Chase play pattern where roles alternate between pursuer and pursued, creating fairness through shared vulnerability and sustaining engagement through reciprocal power exchange.

## Uncategorized

### Opus Form

**Field Notes on Handpan Sound Models & Instruments**: Personal field notes documenting specific handpan instruments and their sound models — the scale templates, acoustic character, modal theory, and ensemble compatibility. Each instrument is documented as both an interactive web page (with tone circles and audio playback) and portable markdown. Planned for publication at www.spiralrhapsody.com/fieldnotes/.

### Person Note

**Christopher Allen**: Christopher Allen is the founder and president of Blockchain Commons, author of the 10 Principles of Self-Sovereign Identity (2016), co-editor of the TLS 1.0 draft, and principal authority of this vault's augmented knowledge system. His work bridges applied cryptography, digital identity, and trust architecture through the Gordian stack, XIDs, and the principal authority framework rooted in agency law.

### Unknown Form

**Mark S. Miller**: Computer scientist and capability security pioneer. Part of Project Xanadu's core team implementing Ted Nelson's vision — invented the Club System, wrote about computational agents and smart contract-like structures two decades before the term existed. Created the E programming language and extended least privilege to least authority. Currently Chief Scientist at Agoric, building secure smart contracts on Hardened JavaScript. Old colleague from Xanadu days — encouraged the cryptographic clubs idea in 1991 that became Gordian Clubs 34 years later.

## Ghost Links

References that could not be located in the source garden. These may be planned nodes, informal references, or alternative names.

- Access Control List vs. Capability System
- Accountability Layer for Delegated Authority
- Accountability as a Layer
- Agent Delegation for Resource Management
- Agent Duties Taxonomy
- Agoric Open Systems
- Agoric Systems
- American Information Exchange
- Authority Sparseness as Design Quality
- Autonomy
- Axelrod Tournament
- Behavioral Constraints Cannot Substitute for Capability Architecture
- Bidirectional Traceability as Accountability Mechanism
- Binary Trust as Trust Regression
- Bonded Commitment as Reputation Bootstrap
- Can Progressive Trust Phases Regress
- Capability (Computer Security)
- Capability Propagation Rules
- Capability Proxy Pattern for Agent Commissions
- Capability Security
- Capability-Scoped Agentic Architecture
- Charge-Per-Use as Composition Enabler
- Cold-Start Trust in Capability Systems
- Competence-Performance Distinction in System Design
- Competence-Performance Separation
- Complete Mediation
- Compound Nodes for Knowledge Management
- Computational Coase Theorem
- Confused Deputy Problem in Agentic Systems
- Connectivity Begets Connectivity
- Consent Theater in SSI Deployments
- Content-Addressed Criticism
- Conversation Temperature as Protocol Cadence Spectrum
- Crimes of Authority
- Cryptographic Naming Integrity
- Currency Conservation as Parasite Filter
- Delegation of Responsibility
- Designation as Authority Grant
- Digital Identity
- Digital Identity Customs
- Digital Identity Working Group
- Direct Market
- Direct Market Model
- Disclosure Tier Hierarchy for Persona-Peer Relationships
- Distributed Intelligence Without Unified Agency
- Duty-Based vs. Rights-Based Identity Governance
- Economy of Mechanism
- Elision and Redaction
- Encapsulation as Property Rights
- Enforceable Software Contracts
- Epistemology-Driven Architecture
- Escrowed Encryption
- European Digital Identity Wallet
- Evolutionarily Stable Strategy
- Fail-Safe Defaults
- Fiduciary Duties for Identity
- Forward-Link Immunization
- Foundational Concept
- Framework as Departure Point
- Granovetter Diagram as Authority Analysis Tool
- Granularity of Progressive Authentication Stages
- Hayek Distributed Knowledge
- Hayekian Knowledge Problem in Computation
- How Does Progressive Trust Defend Against Trust Escalation Attacks
- How Does Progressive Trust Handle Adversarial Participants
- How Should Agent Capability Systems Handle Revocation
- Inductive Trust Bootstrapping
- Informative Absence in Open Systems
- Intelligence as Goal-Achievement Capacity
- Intermediation Patterns for Agent Delegation
- Jerome Saltzer
- Just-In-Time Authority vs Standing Permissions
- K. Eric Drexler
- Kerckhoffs's Principle
- Laws of Agency for Digital Identity
- Least Authority as Foundational Constraint
- Least Common Mechanism
- Legacy Containment Pattern for Agent Tools
- Lenat EURISKO
- Limits of Market Mechanisms in Zero-Marginal-Cost Systems
- Market-Command Boundary in Agent Systems
- Michael Schroeder
- Nodes as Rendezvous Points
- Object-Capability Model
- Object-Capability Model as Market Foundation
- Open Design
- POLA Applied to Multi-Agent Authority Hierarchies
- Pareto-Preferred Compilation
- Permission-First Default Pattern
- Price Signals as Action Guidance Not Effort Incentives
- Principal (Security)
- Principal Authority
- Principle of Least Authority
- Principle of Least Privilege
- Proactive Safety in Federated Agent Systems
- Productive and Wary ESS
- Progressive Authentication as Trust Deepening
- Progressive Trust
- Progressive Trust Life Cycle
- Protection Domain
- Psychological Acceptability
- Remote Session Multiplexing for macOS and iTerm2
- Responsibility Sphere
- Round-Robin Scheduling as Computational Commons Problem
- SSI Legal Architecture
- Saltzer and Schroeder (1975) Protection of Information in Computer Systems
- Security Rests on Inabilities Not Abilities
- Self-Sovereign Identity Governance
- Separation of Privilege
- Spontaneous Order in Software Systems
- Technical Architecture Determines Human Rights Outcomes
- Ten Principles Gap Assessment 2024
- Terms of Service as Agency Agreements
- The Gardening Problem Returns
- The Gardening Problem Returns - Document Lifecycle in the Age of AI Agents
- The Junk Problem in Open Annotation Systems
- Three Categories of SSI Principles
- Three Trust Models Compared
- Transitive Authority
- Trust Begins with Context Not Identity
- Trust Compression for Onboarding
- Trust Deepening Requires Bilateral State
- Trust Dynamics Over Time
- Trust Escalation Attack
- Trust Gaps Are Informative
- Trust Registry as Power Concentration
- Trust Spectrum Quantification
- Trust as Selective Permeability
- Two-Key Authorization Pattern
- When Does Shared Mechanism Become Acceptable Risk
- Wyoming SF0039

