# Changelog

All notable changes to this repository will be documented here. The bill is a working legislative draft and may continue to evolve through committee, floor consideration, and post-enactment refinement. This file tracks substantive changes to the legislation and to the supporting materials.

## v3 — current draft

### Bill text changes

**Replaced § 4-88-1307(i)** — Pricing and retailer compensation now uses a percentage-based, cost-recovery-anchored structure rather than hardcoded dollar amounts. The new structure includes:

- Cost-recovery purpose anchor preventing use as general revenue source
- Maximum retail sale price set by rule with CPI-only routine adjustment, statutory authorization required for larger increases
- Recommended initial price of approximately $6.00 as a non-binding legislative finding
- Three-tier retailer compensation: physical card share, sustained receipt-printed activation share, startup receipt-printed activation share
- Mandatory relative weighting (sustained receipt > physical, startup receipt > sustained receipt)
- 36-month per-retailer startup incentive period commencing on each retailer's integration certification
- Recommended initial percentages of 1/6, 1/4, and 1/3 of the retail sale price (non-binding)
- Reasonable reserve requirement maintained by OST in coordination with DFA
- Surplus distribution mechanism for Arkansas public schools (computer technology, K-6 STEM curriculum, classroom supplies), coordinated with Department of Education distribution formulas
- Three-year persistent-surplus trigger requiring price review and reduction
- Annual accountability reporting on fund balance, reserve target, surplus disposition, written findings, and recommended adjustments
- Five-year program review and renewal mechanism for the startup receipt-activation share
- No-surcharge construction clause and no-property-right construction clause for retailer shares

**Corrected § 4-88-1303(24)(C)** — Changed the Miller LAPS test from "literary, artistic, political, AND scientific value" to "literary, artistic, political, OR scientific value" to conform to *Miller v. California*, 413 U.S. 15 (1973).

**Added § 4-88-1304(g)(7) and (g)(8)** — Explicit non-extraterritoriality clauses clarifying that Arkansas does not require any covered implementation to apply Arkansas standards to users located in another state, and that the uniform-application safe harbor is permissive only. Addresses dormant Commerce Clause concerns under *National Pork Producers Council v. Ross*.

**Added § 4-88-1314(g)** — Procedural protection of scope limitation. New subsection imposing single-subject requirement, separate committee hearing requirement (14 days notice), recorded vote requirement, public statement of effect requirement, and fiscal and privacy impact statement requirement on any future bill that would amend or extend the scope limitation. Includes a companion rules mechanism requesting that each chamber adopt parallel procedural rules. Procedural requirements apply by force of statute regardless of whether chambers adopt the requested rules.

**Tightened § 4-88-1314(d)(1)(A)** — Closed a drafting loophole. The previous language ("returning a boolean age response indicating that the user is not an adult") could have been read to authorize a separate minor-specific signal. Revised language requires that any false response to a minor be returned "in the same manner as for any other user under § 4-88-1304(b), without distinguishing minors from unauthenticated adults in the response."

**Expanded Section 9** from a federal-law savings clause to a federal-law savings AND severability clause, with explicit findings that the privacy-protection provisions serve independent and severable purposes from the underlying age-verification duty. The privacy architecture survives even if § 4-88-1304(a) or any other age-verification duty is held invalid, unconstitutional, preempted, enjoined, or otherwise unenforceable.

**Updated title block** to disclose the new pricing structure, the school surplus distribution, and the procedural protection of scope limitation.

### New repository content

**Added `companion-resolutions/` directory** containing:
- `chamber-rules-companion.md` — Parallel House and Senate procedural rules resolutions implementing the procedural framework requested in § 4-88-1314(g)(7), including point-of-order enforcement, two-thirds suspension threshold, and severance provision for non-compliant omnibus bills.
- `README.md` — Documentation of the chamber rules architecture and how to file the resolutions.

**Replaced `plain-english/plain-english-explanation.md`** with a more comprehensive v3-aware everyman summary covering all sections, including the new procedural protection framework, Commerce Clause additions, and severability expansion. Each section now includes both a "plain-English explanation" and a shorter "everyman summary."

### Repository structure changes

The `bill/` directory now contains three versions: v3 (current), v2 (prior), and v1 (original), all preserved for auditability and forkability.

The `bill/README.md` has been updated to reflect the three-version history.

The repository-level `README.md` file tree has been updated to reflect the new directory structure.

## v2

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

The v1 draft embodied ten of the twelve manifesto principles. v2 closed the remaining gap by adding the multi-issuer requirement (manifesto principle 10) and the adult-side-only limitation (manifesto principle 11). v3 added constitutional refinement, Commerce Clause hardening, procedural protection, and surplus-distribution architecture.
