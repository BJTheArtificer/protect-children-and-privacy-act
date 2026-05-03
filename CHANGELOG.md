# Changelog

All notable changes to this repository will be documented here. The bill is a working legislative draft and may continue to evolve through committee, floor consideration, and post-enactment refinement. This file tracks substantive changes to the legislation and to the supporting materials.

## v2 — current draft

### Bill text changes

**Added § 4-88-1311(k) — Multiple independent approved issuers required.** A new subsection requiring the Office of State Technology to maintain a roster of not fewer than three approved issuers in active operation in this state, drawn from at least two distinct categories. Includes:

- A common-control limit preventing one corporate parent or controlled subsidiary group from holding multiple issuer slots
- Geographic distribution requirements ensuring reasonable physical access for residents of urban, suburban, and rural areas
- Anti-gatekeeper requirements including prohibitions on exclusive-dealing arrangements and tied-product conditioning
- Standards prohibiting an issuer from charging more than the statutory retail cap
- Procedures for the Office of State Technology to monitor concentration and refer matters to the Attorney General
- Contingency procedures if the minimum cannot temporarily be maintained

This provision implements principle 10 of the foundational manifesto, which had not previously been codified.

**Added § 4-88-1314 — Scope limited to adult-side determination — no default minor-side functionality.** A new standalone section limiting the program to its core purpose. Includes:

- A scope limitation prohibiting use of the program, the state-certified interface, or any credential to identify, profile, monitor, restrict, or behaviorally control minors
- Preservation of independent parental control features (Apple Screen Time, Google Family Link, Microsoft Family Safety, and similar tools) that operate outside the state-certified interface and do not rely on age-assurance data collected under this subchapter
- A requirement that any future extension of state-certified age-assurance infrastructure to minor-side functionality be authorized only by separate act of the General Assembly
- A construction rule requiring the section to be construed broadly in favor of limiting the program and against extension
- An annual certification reporting requirement

This provision implements principle 11 of the foundational manifesto, which had not previously been codified.

**Added two new legislative findings in § 4-88-1302(a).** Findings (15) and (16) support the multi-issuer and adult-side-only architectural commitments.

**Added two new statements of intent in § 4-88-1302(b).** Items (8) and (9) support the same.

**Updated title block.** The act's title now reflects the two new substantive commitments.

**Cross-reference updates throughout.** All instances of `§§ 4-88-1306 — 4-88-1313` and `§§ 4-88-1306 through 4-88-1313` have been extended to include the new § 4-88-1314, so the new section is properly inside the scope of covered implementations, the rulemaking authority, the AG enforcement authority, the safe harbor presumption, and the sunset clause.

### Repository structure changes

**Added `bill/full-bill-text-v1.md`** — the prior draft preserved for reference and forkability.

**Renamed bill file** from `bill/full-bill-text.md` to `bill/full-bill-text-v2.md` for version clarity.

**Added `bill/README.md`** explaining the two versions and which to use for what purpose.

**Added `manifesto.md`** at the repository root — the foundational document the bill is built to enforce.

**Added authorship and credits section to README.md** describing the lead author's process, the AI assistance used, and the disclosure norm we recommend for adapters.

### Supporting materials updates pending

The following materials may need updating in subsequent commits to reflect the v2 changes:

- `plain-english/plain-english-explanation.md` — should be extended to cover § 4-88-1311(k) and § 4-88-1314 in the same plain-language style as the rest of the document.
- `fiscal/fiscal-note.md` and `fiscal/fiscal-note-methodology.md` — the multi-issuer requirement may slightly affect retailer onboarding cost projections (more independent retailers to onboard, but more total throughput to amortize across), and the scope limitation has no direct fiscal impact but should be acknowledged.
- `letters/*.md` — the sponsor outreach letters may benefit from reference to the multi-issuer and adult-side-only provisions, particularly for representatives whose framing emphasizes anti-monopoly or anti-surveillance concerns.

## v1 — initial public draft

The first publicly committed version of the bill. Included:

- The boolean `is_18_plus` output as the only lawful external age signal
- The retail credential model with state or federal ID
- One-time credentials that expire on use
- The professional and hobbyist permit carve-out
- Five-year sunset clause
- Statutory fee caps with CPI indexing
- Strict liability narrowed to core data-misuse provisions
- Kinship-caregiver protections in the credential-to-minor prohibition
- Two-thirds threshold for compelled-intermediary remedies
- Research and journalism carve-out
- Coordinated vulnerability disclosure safe harbor
- Eighteen-month implementation runway
- Notice-and-cure procedure with extended cure for systemic technical violations
- Affirmative defense for security breaches with reasonable controls
- Federal-law savings clause

The v1 draft embodied ten of the twelve manifesto principles. v2 closes the remaining gap by adding the multi-issuer requirement (manifesto principle 10) and the adult-side-only limitation (manifesto principle 11).
