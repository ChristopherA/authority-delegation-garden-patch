---
created: 2026-03-29
author: Christopher Allen
citation_slug: allen-2022-progressive-trust
publication_year: 2022
canonical: https://www.lifewithalacrity.com/article/musings-progressive-trust/
brief_summary: "Allen restates progressive trust for the decentralized systems era: trust is not binary but a dynamic, evolving process modeled on real-world human behavior. Critiques classical trust (static verification) and zero-trust (centralized registries) as inadequate. Identifies four technical capabilities required for progressive trust architecture: data minimization, elision/redaction, escrowed encryption, and cryptographic selective disclosure. Positions progressive trust as essential for protecting human rights in digital systems."
tagline: "Trust is built the way people actually build it -- gradually, bilaterally, and on their own terms"
---

- is_a::[[Citation Form]]
- has_status::[[Budding Stage]]
- in_domain::[[Self-Sovereign Identity]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Christopher Allen]]

# Allen (2022) Progressive Trust

## Bibliographic Entry

* _**Musings of a Trust Architect: Progressive Trust**_ (2022). [blog post]. _Allen, Christopher._ Life With Alacrity, December 13, 2022. Retrieved 2026-03-29 from: <https://www.lifewithalacrity.com/article/musings-progressive-trust/>

## Summary

Allen restates his 2004 progressive trust concept for the decentralized systems era. Using a conference meeting metaphor, he argues that trust is not a binary state but a dynamic, evolving process built through successive interactions. The article positions progressive trust against two alternatives: classical trust (static verification via passwords and certificates) and zero-trust architectures (centralized trust registries). Allen critiques trust registries as concentrating power, failing to capture trust dynamics, and creating coercible dependencies. He identifies four technical capabilities required for progressive trust -- data minimization, elision/redaction, escrowed encryption, and cryptographic selective disclosure -- framing these as digital models of techniques humans already use in physical trust-building. The article connects progressive trust directly to human rights protection, arguing that distributed trust-building resists coercion in ways centralized models cannot.

## Key Points

**Trust modeled on human behavior.** Allen's founding argument: progressive trust models how trust actually works between people, groups, and businesses. The conference meeting metaphor demonstrates a natural progression from shared-context assessment through incremental information exchange to third-party enforcement. Digital trust systems should follow this progression rather than imposing artificial binary or registry-based models.

**Context before identity.** In the conference metaphor, the first trust operation is not "who are you?" but "is this worth my time?" Being at the same conference establishes a shared-interest credential before any identity verification occurs. This inverts the order of most digital trust systems, which start with identity verification (certificates, passwords) and skip context assessment entirely.

**Classical trust is static and compromisable.** The traditional approach verifies interactions through authentication mechanisms that "can be easily compromised and do not adequately capture the dynamic and evolving nature of trust." Once authenticated, the trust level does not change. Static trust cannot model the graduated process of human trust-building.

**Zero-trust registries concentrate power.** Allen identifies four specific problems: trust registries create centralization vulnerable to coercion, cannot capture trust dynamics over time, become outdated requiring privacy-breaking "phone home" checks, and depend on third parties that may not treat all parties' risks equally. This is a power analysis: whoever controls the registry controls who is considered trustworthy.

**Progressive trust is dynamic and bilateral.** Trust is built gradually through interactions that allow parties to "test and verify each other's credentials and capabilities." Both parties simultaneously evaluate and are evaluated. Neither grants trust to the other. The process adapts to changing requirements and information.

**Four required technical capabilities.** Progressive trust requires: data minimization (limit shared data to the minimum necessary), elision/redaction (control what information to share by removing or masking portions), escrowed encryption (enforce information commitments in the future), and cryptographic selective disclosure (prevent future data correlation). Allen frames all four as digital models of techniques humans already use.

**Trust gaps are expected and informative.** Allen explicitly designs for incomplete information: systems should use data models that "allow for gaps." What someone chooses not to share is itself informative about their trust level. This is the opposite of trust-completeness requirements in traditional systems, where missing information is treated as risk.

**Human rights as architectural outcome.** Progressive trust "protects human rights and dignity" by "allowing individuals to defend against coercion and violations of their privacy, autonomy, agency, and control." This is not an incidental benefit -- it is the design goal. Technical architecture determines human rights outcomes; progressive trust is the architecture that protects autonomy.

**Eighteen years of intellectual continuity.** Allen explicitly connects this article to his 2004 post on progressive trust, creating an intellectual arc from software design observation to comprehensive architectural position. The concept was not invented for the current moment but has been developing across two decades of practice.

## Key Quotes

> "The basic idea behind progressive trust is to model how trust works in the real world, between real people, groups, and businesses, rather than solely relying on mathematical or cryptographic trust."

> "Trust is not a binary state but rather a dynamic and evolving process."

> "This architecture is critical for protecting human rights and dignity, as it allows individuals to defend against coercion and violations of their privacy, autonomy, agency, and control."

> "Fundamentally, these are all techniques that we use in real-life when progressively increasing trust with someone else; they just need to be modeled in digital space."

> "Trust registries must rely on a third party to hold and update the registry. This highlights some of the flaws of centralization, such as the trust registry not treating the risks of all parties equally."

## Influence

This article is the pivot point in Allen's progressive trust intellectual arc. The 2004 post introduced the concept; this 2022 article repositions it as a comprehensive alternative to trust registries and classical trust for decentralized systems. Everything that follows in the Musings series -- the data minimization framework (January 2023), the cryptographic agility argument (March 2023), the developer reference (2024), the eleven-phase lifecycle (November 2024) -- builds on the architectural position established here. The trust registry critique has been influential in the Rebooting the Web of Trust community and the W3C Credentials Community Group, where Allen's argument against centralized trust determination aligns with the decentralized identity movement's core principles.

## Limitations

**No lifecycle phases specified.** This article argues for why progressive trust is needed and what technical capabilities it requires, but does not specify the operational phases. The eleven-phase lifecycle appears only in the 2024 "Building Trust in Gradients" article. This means the 2022 article provides the argument without the specification.

**The zero-trust comparison is somewhat unfair.** Allen compares progressive trust to a specific implementation of zero-trust (trust registries) rather than to the zero-trust principle itself ("never assume trust, always verify"). The zero-trust principle is compatible with progressive trust -- both emphasize continuous verification. Allen's real target is trust registries and trust frameworks, not zero-trust philosophy.

**No threat model for progressive trust.** Allen identifies risks of classical trust and zero-trust but does not analyze risks of progressive trust itself. A sophisticated adversary could game the progressive process by appearing trustworthy in early, low-stakes interactions to gain access exploitable in later phases. The article does not address this trust escalation attack vector.

## Sources

- Primary: Allen, Christopher. "Musings of a Trust Architect: Progressive Trust." Life With Alacrity, December 13, 2022. <https://www.lifewithalacrity.com/article/musings-progressive-trust/>
- Referenced: Allen, Christopher. "Progressive Trust." Life With Alacrity, 2004. <http://www.lifewithalacrity.com/2004/08/progressive_tru.html>
- Referenced: MATTR. "Trust Frameworks." 2021. <https://learn.mattr.global/docs/concepts/trust-frameworks>
- Referenced: Johnson, Anna. "Trinsic Basics: What Is a Trust Registry?" 2022. <https://trinsic.id/trinsic-basics-what-is-a-trust-registry/>

## Relations

- relates_to::[[Allen (2024) Building Trust in Gradients]]
  - The 2024 article provides the eleven-phase lifecycle specification that this 2022 article argues for but does not contain; together they form an argument-specification pair
- relates_to::[[Allen (2024) Progressive Trust]]
  - The developer reference operationalizes the concepts in this article with implementation vocabulary and domain examples; this article provides the why, the developer reference provides the how
- relates_to::[[Allen (2023) Data Minimization and Selective Disclosure]]
  - This article names four required technical capabilities; the 2023 article develops data minimization and selective disclosure in depth with the three-axis framework and cryptographic technique taxonomy
- relates_to::[[Allen (2016) The Path to Self-Sovereign Identity]]
  - Self-sovereign identity provides the philosophical framework; progressive trust provides the trust-building model compatible with that framework
- relates_to::[[Allen (2023) Origins of Self-Sovereign Identity]]
  - Living systems theory of identity as membrane provides the biological metaphor that progressive trust operationalizes as selective permeability
- relates_to::[[Allen (2025) The Exodus Protocol]]
  - Exodus Protocols protect infrastructure from centralized capture; progressive trust protects trust-building from centralized capture via trust registries
- relates_to::[[Allen (2021) Principal Authority]]
  - Principal authority requires a trust model where the individual controls their own trust decisions; progressive trust is that model
- relates_to::[[Allen (2023) Problems of Cryptographic Agility]]
  - The cryptographic selective disclosure required by progressive trust is subject to the n-factorial problem if implemented with full cryptographic agility
