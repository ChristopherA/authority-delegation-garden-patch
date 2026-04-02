---
part_of: "[[Allen (2023) Least and Necessary Design Patterns]]"
role: analysis
created: 2026-03-29
brief_summary: "Primary source analysis of Allen (2023) on six security design patterns: least privilege, least authority, least access, and their inside-out counterparts — necessary privilege, necessary authority, necessary access. Traces intellectual lineage from Saltzer/Schroeder through Miller to Allen's own extension into data access and the inversion methodology."
---

- is_a::[Citation Form](../forms/Citation%20Form.html)
- has_status::[Budding Stage](../forms/Budding%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

part_of::[Allen (2023) Least and Necessary Design Patterns](Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)

# Analysis: Allen (2023) Least and Necessary Design Patterns

## The Intellectual Lineage: From Privilege to Access

Allen traces a clear intellectual lineage through three generations of security thinking:

1. **Saltzer and Schroeder (1975)**: The Principle of Least Privilege — limit each user, program, or system component to the minimum permissions required for its function. The design pattern originated in the military and intelligence communities and focused on protecting information assets.

2. **Mark S. Miller (2006)**: The Principle of Least Authority — extends least privilege by recognizing transitive authority. A user might lack direct privilege to access a resource but hold privilege to access a program that itself holds privilege to access the resource. Miller's contribution is seeing privileges as a web of interconnected grants, not isolated permissions.

3. **Allen (2023)**: The Principle of Least Access — extends both prior patterns into the domain of digital data, particularly self-sovereign identity and verifiable credentials. Where least privilege and least authority focus on permissions to do things, least access focuses on permissions to see data, and specifically on minimizing correlation opportunities across the data ecosystem.

This lineage is not just historical. Each stage adds a dimension the prior stage was blind to: isolated permissions, then transitive authority webs, then data access across ecosystems. Allen positions himself as extending a tradition, not founding a new one.

## The Inside-Out Methodology

The article's most distinctive contribution is the "inside-out" or inversion methodology. Allen states directly: "Once I discover a useful design pattern, I often find utility in turning it inside out." The method works by:

1. Take an established restrictive design pattern (minimize X)
2. Invert the orientation: instead of asking "what to restrict," ask "what to enable"
3. The resulting pattern provides new design insights that the original pattern's framing obscured

Applied to the security design patterns:

| Restrictive Pattern | Inside-Out Pattern | Shift in Perspective |
|---|---|---|
| Least Privilege | Necessary Privilege | What permissions does the user need? |
| Least Authority | Necessary Authority | What authority web does the user need? |
| Least Access | Necessary Access | What data does the system need to operate? |

Allen argues the inversion is not merely semantic. The "necessary" framing shifts the design task from "enumerate and block all possible abuses" (potentially endless) to "enumerate and provide what is needed" (bounded). This is a meaningful shift for designers because it resets the design boundary: instead of playing defense against an open-ended threat surface, you define the positive requirements and everything else is excluded by default.

The practical claim is that necessary-framing systems are more scalable, more adaptable, and create better user experiences because users never encounter unexpected barriers — they have everything they need from the start.

## Selective Correlation as Demonstration

Allen provides one non-security example of the inversion methodology: turning selective disclosure inside-out produces "selective correlation." Selective disclosure asks "what data should I minimize to avoid correlation?" Selective correlation asks "what data should I purposefully disclose to enable correlation?"

This is more than a rhetorical flip. Selective correlation acknowledges that correlation is not always harmful — sometimes it is the security objective (fraud detection, accountability, continuity of identity across sessions). The inside-out pattern isolates the cases where correlation serves the user rather than threatens them.

This demonstration matters because it shows the inversion methodology is a general-purpose design tool, not specific to the privilege/authority/access family.

## Necessary Access and the Credential Negotiation Model

Allen's most practically significant extension is "necessary access" applied to credential systems. The argument runs:

1. Current credential systems ask users to release data (data minimization perspective)
2. Necessary access inverts this: define what data each system needs to operate
3. This creates a foundation for negotiation — the user knows exactly what data is requested and can decide whether the exchange is worthwhile
4. The negotiation model treats data exchange as bilateral, not unilateral

This is directly relevant to verifiable credential architectures. Instead of a verifier requesting whatever data it wants and the user trying to minimize disclosure, the system declares its data needs upfront. The user then has complete information for a consent decision.

The coercion scenario is particularly telling: Allen suggests that if a citizen's datastore refuses to grant a law enforcement officer access to information they shouldn't have, the threat of coercion is "negated." This is a strong claim about architectural coercion resistance — the system's design prevents improper access regardless of the social power dynamics at play.

## The Dignity Framing

Allen opens by stating that he prioritizes "the protection of individuals, who are uniquely due respect and dignity, and who are likely to be more vulnerable and less resilient than groups such as tribes, corporations and governments." This framing distinguishes his approach from the military-origin tradition of least privilege, where the concern is asset protection, not individual dignity.

The shift from asset protection to dignity protection changes what counts as a security failure. In an asset-protection frame, a security failure is unauthorized access to a resource. In a dignity-protection frame, a security failure is the violation of an individual's autonomy, privacy, or informed consent — even if no "resource" was technically breached.

This framing connects directly to Allen's self-sovereign identity work. The design patterns are not just technical security tools — they are implementations of a normative commitment to individual dignity.

## Second-Order Analysis: What the Article Omits

**No implementation examples.** Allen describes six design patterns but provides no concrete implementation. How would a verifiable credential system implement "necessary access" in practice? What does a "necessary authority" system look like in code? The article stays at the conceptual level.

**No tension analysis between least and necessary.** The article presents the two families as complementary, but they could conflict. A least-access analysis might identify data that should be restricted; a necessary-access analysis of the same system might identify that same data as required for the system to function. The article does not address how to resolve this tension.

**Transitive authority is acknowledged but not analyzed for data.** Miller's key insight was that authority is transitive — a user might gain access through intermediaries. Allen mentions this in the context of least authority but does not fully explore transitive data access in the least access or necessary access patterns. For example: if a system "needs" data to function, and that data flows to a third-party analytics provider, is the third party's access covered by "necessary access"? The ecosystem implications are acknowledged ("looks at the whole data ecosystem") but not developed.

**The coercion resistance claim is architecturally interesting but socially naive.** Allen argues that if a datastore refuses to reveal improperly requested data, coercion is negated. But coercion in practice operates outside the data system — confiscation of devices, legal compulsion to decrypt, social pressure. Architectural coercion resistance is one layer; it does not negate coercion as a whole.

## The Six Patterns as a Taxonomy

The article's lasting structural contribution is a clean 2x3 taxonomy:

|  | Privilege | Authority | Access |
|---|---|---|---|
| **Least** (restrictive) | Minimize permissions | Minimize permissions + transitive authority | Minimize data access + transitive authority |
| **Necessary** (enabling) | Provide needed permissions | Provide needed permissions + transitive authority | Provide needed data access + transitive authority |

This taxonomy is compact, memorable, and extensible. The two axes (restrictive vs. enabling; privilege vs. authority vs. access) can be applied to future design pattern families. The taxonomy itself is a design tool.
