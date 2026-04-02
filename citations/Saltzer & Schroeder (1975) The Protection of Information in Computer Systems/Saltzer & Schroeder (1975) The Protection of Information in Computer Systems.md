---
created: 2026-04-01
author: Christopher Allen
citation_slug: saltzer-schroeder-1975-protection-of-information
publication_year: 1975
canonical: https://bitstreamllc.com/assets/documents/the-protection-of-information-in-computer-systems-saltzer-schroeder.pdf
brief_summary: "Saltzer and Schroeder's 1975 IEEE tutorial defines eight design principles for protection mechanisms in computer systems, including the Principle of Least Privilege. Three-part structure: basic principles with design criteria, technical architecture of capability and access control list systems, and state of the art in 1975."
tagline: "The 1975 paper that named the Principle of Least Privilege and seven companion design criteria"
---

- is_a::[[Citation Form]]
- has_status::[[Seed Stage]]
- in_domain::[[Agentic Architecture]]
- in_precinct::[[Garden Precinct]]
- cites_work_by::[[Jerome Saltzer]]
- cites_work_by::[[Michael Schroeder]]

# Saltzer & Schroeder (1975) The Protection of Information in Computer Systems

## Bibliographic Entry

* _**The Protection of Information in Computer Systems**_ (1975). [journal article]. _Saltzer, Jerome H. and Schroeder, Michael D._ Proceedings of the IEEE, Vol. 63, No. 9, September 1975, pp. 1278–1308. Originally presented at the Fourth ACM Symposium on Operating System Principles (October 1973); revised version in Communications of the ACM 17, 7 (July 1974). Retrieved from: <https://bitstreamllc.com/assets/documents/the-protection-of-information-in-computer-systems-saltzer-schroeder.pdf>

## Summary

Saltzer and Schroeder survey the mechanics of protecting computer-stored information from unauthorized use or modification, focusing on architectural structures in hardware and software. The paper develops in three parts: Section I defines desired functions, eight design principles, and examples of elementary protection and authentication mechanisms. Section II examines the principles of modern protection architectures and the relation between capability systems and access control list systems. Section III reviews the state of the art and current research directions as of 1975. The eight design principles — economy of mechanism, fail-safe defaults, complete mediation, open design, separation of privilege, least privilege, least common mechanism, and psychological acceptability — have remained the foundational checklist for protection system design for fifty years.

## Key Points

**Least privilege names a constraint that was already implicit.** The principle — "every program and every user of the system should operate using the least set of privileges necessary to complete the job" — formalizes what careful system designers had been doing informally. By naming it, Saltzer and Schroeder made it auditable: a system can be evaluated against the criterion, and violations can be identified and justified or corrected. The military's "need-to-know" rule is cited as an existing instance of the same principle.

**Fail-safe defaults invert the burden of justification.** Rather than asking "under what conditions should access be denied?" the principle asks "under what conditions should access be permitted?" A design mistake in a permission-granting mechanism tends to fail by refusing access — a safe failure detected immediately. A design mistake in a denial mechanism tends to fail by granting access — an unsafe failure that may go unnoticed in normal use. The asymmetry between these failure modes is the reason to prefer permission-based defaults.

**Complete mediation prevents caching from becoming a vulnerability.** Every access to every protected object must be checked against current authorization, not cached prior authorization. This principle forces a system-wide view of access control that includes initialization, recovery, shutdown, and maintenance — not just normal operation. Performance optimizations that remember prior authorization results must be designed so that any change in authority invalidates the cached result.

**Open design shifts the security burden to keys.** The mechanism should not depend on the ignorance of potential attackers, but on possession of specific, more easily protected keys or passwords. This decoupling allows mechanisms to be examined by many reviewers without concern that review itself compromises the safeguards. The principle also acknowledges that secrecy cannot be maintained for any system that receives wide distribution — a practical argument as important as the theoretical one.

**Separation of privilege requires two independent keys.** A protection mechanism that requires two keys to unlock is more robust and flexible than one requiring only a single key. Once locked, the two keys can be held by physically separate parties or programs; no single accident, deception, or breach of trust suffices to compromise the protected information. The bank safe-deposit box and the nuclear weapons authorization system are non-computer examples. In software, this applies wherever two independent conditions must be met before access is permitted.

**Least common mechanism limits information paths between users.** Every mechanism shared by more than one user is a potential information path between them and must be designed to prevent unintentional compromise of security. The principle counsels minimizing such shared mechanisms. When a function can be implemented either as a shared supervisor procedure or as a library procedure handled within the user's own environment, the latter is preferred, even at some cost in efficiency or convenience.

**Psychological acceptability determines whether the mechanism is actually used.** Protection mechanisms must be designed so that users routinely and automatically apply them correctly. If the mental model a user must maintain to use the mechanism matches their model of their protection goals, mistakes are minimized. Mechanisms that require users to translate their goals into radically different specification languages produce systematic errors. The failure mode from poor usability is not user frustration but security violation.

**The principles function as warnings, not absolute rules.** Saltzer and Schroeder explicitly characterize the eight principles as guidelines that serve best as warnings: if some part of a design violates a principle, the violation is a symptom of potential trouble, and the design should be carefully reviewed to ensure the trouble has been accounted for or is unimportant. A design that knowingly violates a principle is not necessarily insecure, but it requires explicit justification.

## Key Quotes

> "Every program and every user of the system should operate using the least set of privileges necessary to complete the job. Primarily, this principle limits the damage that can result from an accident or error." [Section I-A-3, Principle f]

> "Base access decisions on permission rather than exclusion. This principle, suggested by E. Glaser in 1965, means that the default situation is lack of access, and the protection scheme identifies conditions under which access is permitted." [Section I-A-3, Principle b]

> "Every access to every object must be checked for authority. This principle, when systematically applied, is the primary underpinning of the protection system. It forces a system-wide view of access control, which in addition to normal operation includes initialization, recovery, shutdown, and maintenance." [Section I-A-3, Principle c]

> "The design should not be secret. The mechanisms should not depend on the ignorance of potential attackers, but rather on the possession of specific, more easily protected, keys or passwords." [Section I-A-3, Principle d]

> "It is essential that the human interface be designed for ease of use, so that users routinely and automatically apply the protection mechanisms correctly. Also, to the extent that the user's mental image of his protection goals matches the mechanisms he must use, mistakes will be minimized." [Section I-A-3, Principle h]

> "As is apparent, these principles do not represent absolute rules — they serve best as warnings. If some part of a design violates a principle, the violation is a symptom of potential trouble, and the design should be carefully reviewed to be sure that the trouble has been accounted for or is unimportant." [Section I-A-3, concluding remark]

## Influence

The eight design principles have become a standard reference in computer security education and system design. Allen cites Saltzer and Schroeder in [[Allen (2023) Least and Necessary Design Patterns]] as the origin of the least privilege lineage, tracing from this 1975 paper through Mark Miller's Principle of Least Authority (2006) to the principle of least access for self-sovereign identity contexts. The principles remain current in agentic computing contexts: least privilege governs what tools and permissions an agent should hold; complete mediation governs whether every agent action is checked against authorization; separation of privilege supports multi-party approval for high-consequence agent actions. The paper's three-way taxonomy of security violations — unauthorized release, unauthorized modification, and unauthorized denial of use — continues to structure threat modeling in modern systems.

## Sources

- Primary: Saltzer, Jerome H. and Schroeder, Michael D. "The Protection of Information in Computer Systems." Proceedings of the IEEE, Vol. 63, No. 9, September 1975. <https://bitstreamllc.com/assets/documents/the-protection-of-information-in-computer-systems-saltzer-schroeder.pdf>
- Web version originally created by Norman Hardy.

## Relations

- relates_to::[[Allen (2023) Least and Necessary Design Patterns]]
  - Allen's 2023 article traces the design pattern lineage from this paper through Miller and extends it to data access in self-sovereign identity contexts

- relates_to::[[Principle of Least Privilege]]
  - This citation is the origin source for the Principle of Least Privilege as a named, formal design criterion

- relates_to::[[Principle of Least Authority]]
  - Least authority (Miller 2006) extends least privilege by recognizing transitive authority webs; this paper is the upstream source in that lineage

- relates_to::[[Human Authority Over Augmentation Systems]]
  - Complete mediation and fail-safe defaults apply directly to agentic systems: every agent action should be checked against current authorization, not prior assumptions

- relates_to::[[Allen (2021) Principal Authority]]
  - Principal authority in agency law and least privilege in computer security share the same constraint: delegates receive the minimum authority needed, not the full authority of the principal
