---
created: 2026-04-02
author: Christopher Allen
brief_summary: "Allen reframes security design from protecting information assets (the military tradition) to protecting individuals who are uniquely due respect and dignity. This changes what counts as a security failure — not just unauthorized access, but violation of autonomy, privacy, or informed consent."
tagline: "Security design protects people with dignity, not assets with classifications"
---

- is_a::[Gloss Form](../forms/Gloss%20Form.html)
- has_status::[Seed Stage](../forms/Seed%20Stage.html)
- in_domain::[Self-Sovereign Identity](../domains/Self-Sovereign%20Identity.html)
- in_precinct::[[Garden Precinct]]↑

# Dignity Not Asset Protection as Security Design Frame

The security design tradition descends from military information classification. Its question is: how do we protect assets from unauthorized access? Assets have classifications. Access has clearances. The model works when the thing being protected is a document in a vault.

Allen reframes the question. The thing being protected is not an asset — it is a person. People are not classified; they are "uniquely due respect and dignity." This reframing changes what counts as a security failure. In the asset model, failure is unauthorized access. In the dignity model, failure includes violation of autonomy, violation of privacy, and denial of informed consent — even when access was technically "authorized" by the system's rules.

The reframing has architectural consequences. A system designed to protect assets minimizes exposure — least privilege, least access, least everything. A system designed to protect dignity must also ensure agency — the person must have the information and authority to make meaningful choices about their own data. This is why the necessary pattern family matters: least access without necessary access produces a system that minimizes data exposure while denying the person the ability to understand what is being asked of them and why.

The dignity frame also explains why architectural coercion resistance matters. If the system protects assets, coercion is someone else's problem — the vault is secure, what happens outside is policy. If the system protects people, coercion resistance is a design requirement. A datastore that refuses improper requests is protecting the person, not just the data.

This is not a philosophical nicety layered on top of engineering. It is a design constraint that produces different architectures. Systems designed for dignity build in consent mechanisms, progressive disclosure, bilateral negotiation, and exit rights. Systems designed for asset protection build in walls, gates, and guards. The same data, the same threat model, different architectures — because the thing being protected is different.

## Sources

- [Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html) — the article where the dignity framing is explicitly stated as the motivating principle
- [Allen (2016) The Path to Self-Sovereign Identity](../citations/Allen%20(2016)%20The%20Path%20to%20Self-Sovereign%20Identity/Allen%20(2016)%20The%20Path%20to%20Self-Sovereign%20Identity.html) — the ten principles of self-sovereign identity, grounded in the same dignity commitment
- [Allen (2021) Principal Authority](../citations/Allen%20(2021)%20Principal%20Authority/Allen%20(2021)%20Principal%20Authority.html) — agency law as a framework for dignity-respecting delegation

## Relations

- relates_to::[Sovereignty Is Selective Permeability Not Absolute Control](../convictions/Sovereignty%20Is%20Selective%20Permeability%20Not%20Absolute%20Control.html)
  - Sovereignty-as-membrane is what dignity looks like in architecture — not walls that isolate, but membranes that enable exchange while protecting autonomy.

- relates_to::[Dignity Requires Sovereignty and Sovereignty Is a Membrane](../convictions/Dignity%20Requires%20Sovereignty%20and%20Sovereignty%20Is%20a%20Membrane.html)
  - The conviction that grounds the dignity frame — from dignity to sovereignty to membrane to design obligation.

- relates_to::[Values Precede Technical Decisions](../convictions/Values%20Precede%20Technical%20Decisions.html)
  - Dignity-first security is the specific instance of values-preceding-technology in the security design domain.

- relates_to::[Principle of Least Access](Principle%20of%20Least%20Access.html)
  - Least access is the restrictive pattern motivated by the dignity frame — minimizing data exposure to protect the person, not the asset.

- relates_to::[Necessary Access](Necessary%20Access.html)
  - Necessary access is the enabling pattern that the dignity frame demands — without it, the person cannot exercise informed consent.

- relates_to::[Allen (2023) Least and Necessary Design Patterns](../citations/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns/Allen%20(2023)%20Least%20and%20Necessary%20Design%20Patterns.html)
  - The source article that explicitly positions the dignity frame against the military asset-protection tradition.

- relates_to::[Inside-Out Methodology as Design Pattern Innovation](Inside-Out%20Methodology%20as%20Design%20Pattern%20Innovation.html)
  - The inside-out methodology is itself dignity-driven — inverting from "what to restrict" to "what to enable" shifts the design orientation from protecting assets to empowering people.
