---
part_of: "[[Allen (2023) Least and Necessary Design Patterns]]"
role: insights
created: 2026-03-29
brief_summary: "Extraction candidates from Allen (2023) on least and necessary design patterns: the inside-out methodology, six-pattern taxonomy, necessary access as credential negotiation foundation, and dignity-framing for security design."
---

- is_a::[Citation Form](../forms/Citation%20Form.html)
- has_status::[Budding Stage](../forms/Budding%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

part_of::[Allen (2023) Least and Necessary Design Patterns](Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)

# Insights: Allen (2023) Least and Necessary Design Patterns

## Lens Perspectives

**Why this matters for the garden:** The article provides a named methodology (inside-out design patterns) that Allen uses across his corpus. Understanding this methodology as a reusable tool helps interpret other Allen articles where he applies similar inversions (data minimization to selective disclosure, authority to autonomy, restriction to enablement).

**Why this matters for self-sovereign identity:** The six patterns form a taxonomy that any credential system designer can use as a checklist. The "necessary access" pattern in particular provides the conceptual foundation for negotiation-based credential exchange — the verifier declares what it needs, the holder decides whether to participate.

## Garden Node Candidates

**Extract as Pattern:**

- [Inside-Out Methodology as Design Pattern Innovation](../../glosses/Inside-Out%20Methodology%20as%20Design%20Pattern%20Innovation.html) — Allen's general-purpose method for discovering new design patterns by inverting the orientation of established ones. Take a restrictive pattern (minimize X), invert it to an enabling pattern (provide necessary X), and the resulting pattern reveals design insights the original framing obscured.
  - [source: direct from article]
  - **Extracted** as gloss.

- [Necessary Access](../../glosses/Necessary%20Access.html) — the inside-out of least access: instead of asking what data to restrict, ask what data a system needs to operate. Creates a foundation for bilateral negotiation in credential systems, where the user has complete information for consent.
  - [source: direct from article]
  - **Extracted** as gloss.

- [[Selective Correlation]]↑ — the inside-out of selective disclosure: purposefully disclose data to enable beneficial correlation rather than minimize data to avoid harmful correlation. Acknowledges that correlation is sometimes the security objective.
  - [source: direct from article]
  - Ghost link: [[Selective Correlation]]↑

**Extract as Model:**

- [[Least and Necessary Taxonomy]]↑ — the 2x3 taxonomy of security design patterns: two orientations (restrictive least, enabling necessary) across three scopes (privilege, authority, access). Compact, memorable, and extensible to future pattern families.
  - [source: direct from article]
  - Ghost link: [[Least and Necessary Taxonomy]]↑

**Extract as Principle:**

- [Dignity Not Asset Protection as Security Design Frame](../../glosses/Dignity%20Not%20Asset%20Protection%20as%20Security%20Design%20Frame.html) — Allen's reframing of security from asset protection (military tradition) to individual dignity protection. A security failure is not just unauthorized access to a resource but violation of an individual's autonomy, privacy, or informed consent.
  - [source: direct from article, combined with Allen's broader values framework]
  - **Extracted** as gloss.

**Extract as Gloss:**

- [[Transitive Authority]]↑ — Mark Miller's concept that privileges form a web: a user who can access a program that can access a resource effectively has authority over the resource, even without direct privilege. The gap between "privilege" and "authority."
  - [source: article crediting Miller 2006]
  - Ghost link: [[Transitive Authority]]↑

## Ghost Links (Nodes Not Yet in Garden)

- [Principle of Least Privilege](../../glosses/Principle%20of%20Least%20Privilege.html) — Saltzer and Schroeder's foundational 1975 design pattern
- [[Mark S. Miller]]↑ — key figure in capability-based security
- [[Capability-Based Security]]↑ — the broader paradigm Miller works in; needs a Reference or Model
- [[Data Minimization]]↑ — Allen's prior article on the topic; likely a separate citation
- [[Credential Negotiation]]↑ — the bilateral model where verifier declares needs and holder decides participation
- [[Architectural Coercion Resistance]]↑ — the claim that system design can prevent improper data access regardless of social power dynamics

## Connections to Existing Garden Nodes

**Connects to [Allen (2024) Progressive Trust](../citations/Allen%20(2024)%20Progressive%20Trust/Allen%20(2024)%20Progressive%20Trust.html):**
Progressive trust is the operational mechanism for implementing necessary access — trust and data disclosure increase incrementally based on demonstrated need. The necessary access pattern provides the theoretical justification; progressive trust provides the interaction model.
[source: garden-level inference]

**Connects to [Allen (2021) Principal Authority](../citations/Allen%20(2021)%20Principal%20Authority/Allen%20(2021)%20Principal%20Authority.html):**
Principal authority defines who gets to make decisions about data. Necessary access defines what data is needed for a given function. Together they form a two-part test: does this principal have authority to request this data, and is this data necessary for the function?
[source: garden-level inference]

**Connects to [[Allen (2023) Origins of Self-Sovereign Identity]]↑:**
The dignity framing in this article connects directly to the self-sovereign identity origins. Self-sovereign identity is the identity-domain expression of the broader commitment to individual dignity over institutional control.
[source: garden-level inference]

**Connects to [[Allen (2025) How My Values Inform Design]]↑:**
The dignity-first framing is the values-level commitment; the least and necessary patterns are the design-level implementation. "Respect and dignity" as the root motivation for security design is the values article's thesis expressed as architecture.
[source: garden-level inference]

## Key Tensions for Garden Exploration

**Implementation gap.** The six patterns are cleanly described conceptually but have no worked implementation examples. A garden inquiry could ask: what does a verifiable credential system implementing "necessary access" look like concretely?

**Least vs. necessary conflict resolution.** When a least-access analysis and a necessary-access analysis of the same system produce conflicting answers, how is the conflict resolved? The article presents them as complementary but does not address the case where they disagree.

**Transitive data access is underexplored.** The article acknowledges the ecosystem dimension of data access but does not fully develop how transitive authority applies to data flows through third parties, analytics providers, and aggregators.

## Extraction Targets

1. ~~Inside-out methodology~~ → **Extracted**: [Inside-Out Methodology as Design Pattern Innovation](../../glosses/Inside-Out%20Methodology%20as%20Design%20Pattern%20Innovation.html) (Gloss)
2. ~~Necessary access~~ → **Extracted**: [Necessary Access](../../glosses/Necessary%20Access.html) (Gloss)
3. Selective correlation → [Pattern Form](../forms/Pattern%20Form.html) named [[Selective Correlation]]↑
4. Six-pattern taxonomy → [Model Form](../forms/Model%20Form.html) named [[Least and Necessary Taxonomy]]↑
5. ~~Dignity as security objective~~ → **Extracted**: [Dignity Not Asset Protection as Security Design Frame](../../glosses/Dignity%20Not%20Asset%20Protection%20as%20Security%20Design%20Frame.html) (Gloss)
6. Transitive authority → [Gloss Form](../forms/Gloss%20Form.html) named [[Transitive Authority]]↑
