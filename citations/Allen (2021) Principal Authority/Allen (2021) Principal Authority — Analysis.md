---
part_of: "[[Allen (2021) Principal Authority]]"
role: analysis
created: 2026-03-22
brief_summary: "Primary source analysis of Allen (2021) Principal Authority: the legal architecture choice, the tripartite rights/duties structure, the critique of current platforms, and open questions requiring legal expertise."
---

part_of::[[Allen (2021) Principal Authority]]

# Analysis: Allen (2021) Principal Authority

## The Core Architectural Choice

Allen's key move is selecting Laws of Agency rather than property law as the legal foundation for self-sovereign identity. This is not a technical choice but a constitutional one about how the state relates to individual identity.

Property law creates a sovereign grant relationship: the state issues property rights and retains ultimate authority through eminent domain and asset forfeiture. If digital identity were property, a government could theoretically seize or reclaim it — violating the very existence and control principles SSI requires.

Agency law creates a different structure. When a Principal delegates authority to an Agent, the state's role is to recognize, respect, and enforce that relationship — not to be a party to it. The state acts as infrastructure (courts, enforcement) without becoming an authority over the identity itself. Wyoming's 28-word definition accomplishes this structurally by saying a natural person has "principal authority" over their digital identity, not that they "own" it.

## The Tripartite Structure

Allen reorganizes the original 10 SSI principles into three legally differentiated categories:

**Category 1 — Rights of self-sovereign authority** (implicit in being a Principal): existence, control, persistence, consent. These don't require new legislation; they derive automatically from recognizing someone as a Principal with authority.

**Category 2 — Duties of identity agents** (require explicit codification): access, transparency, portability, interoperability, minimization, protection. These describe what agents holding identity data must do for their principals. Allen notes these are "best practices" that "need to be better codified to become true duties."

**Category 3 — Duties from Agency law** (may be imported automatically): specificity, responsibility, representation, fidelity, disclosure. These are established Agency law duties that Wyoming's definition might import without needing explicit statement, because they attach to any agency relationship under common law.

The distinction between Category 2 and Category 3 is significant. Category 3 duties have centuries of jurisprudence; Category 2 duties are new and must be developed as digital identity customs — a generational project.

## The Platform Critique

Allen's critique of banks, Facebook, and Google is precise: they are not bad actors so much as structurally misaligned. They were never structured as agents of their users; they are service providers, which carry no duty to act in the user's best interest. The problem is architectural, not behavioral.

Under Agency law, these platforms would be prohibited from:
- Selling identity data (secret profit from delegated authority)
- Monetizing inferred demographic data without disclosure (violation of transparency duty)
- Operating without opt-in rather than opt-out (violation of specificity duty)

GDPR and CCPA address some of this but through a data protection framework, not an identity governance one. Allen's argument is that the duty-based Agency framework is structurally superior: rights require individuals to assert them; duties require entities to fulfill them regardless.

## Delegation as Core Mechanism

The delegation structure is what makes Agency law work for SSI. When others exert Principal Authority over identity data, "they are doing so only as agents of the Principal." This creates:

- A clear hierarchy (Principal → Agent)
- Revocability at any time (fundamental to Agency law)
- Specific scope (agents authorized only for instructed tasks)
- Audit obligation (agents must report actions back to the Principal)

The revocability principle maps directly to portability: if a principal can revoke delegation at any time, agents cannot create lock-in. This goes further than GDPR's data portability right by making it an ongoing duty rather than a claim individuals must assert.

## Open Questions Allen Raises

Allen poses several questions requiring legal expertise he disclaims:

- Whether additional duties (fiduciary, trust law) should apply to identity agents
- Whether decentralized systems (no identifiable agent) can satisfy Agency duties
- How private keys should be protected as a unique artifact combining property, identity, and authority
- Whether market power imbalances can be addressed through Agency duties (analogous to common carrier obligations)
- Whether "crimes of authority" — theft of private keys enabling impersonation — deserve distinct legal treatment

These are not rhetorical questions; they mark the boundary of what the article claims versus what requires follow-on legal scholarship.

## Custom Development as Long Arc

Allen's most sober observation: Agency law is built on Laws of Custom, which develop through common law over generations. Digital identity is too new to have such customs. The path from Wyoming's legislation to a mature body of digital identity law runs through:

1. Case precedents from courts ruling on identity duty violations
2. Industry standards evolving into expected customs
3. Multi-stakeholder processes like Wyoming's Digital Identity Working Group
4. Academic scholarship proposing and critiquing duty frameworks

This process is explicitly generational. The article positions Wyoming's legislation as a foundation, not a solution. Anyone reading this as a complete legal framework misreads the closing acknowledgment: "it's still just a starting point."
