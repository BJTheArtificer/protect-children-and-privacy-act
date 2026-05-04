# Bill Text

This directory contains the legislative text of the Arkansas Protects Our Children and Our Privacy Online Act in three versions, all preserved deliberately for auditability and forkability.

## Files

**`full-bill-text-v3.md`** — the **current draft**. This is the version intended for filing and the version other states should fork from unless they have a specific reason to use an earlier version. Includes all provisions in earlier drafts plus several v3 improvements documented in the inline changelog at the top of the file.

**`full-bill-text-v2.md`** — the prior draft, preserved for reference. Includes the multiple-issuers requirement (§ 4-88-1311(k)) and the adult-side scope limitation (§ 4-88-1314), and the percentage-based pricing structure (§ 4-88-1307(i)), but does not yet include the v3 improvements.

**`full-bill-text-v1.md`** — the original publicly committed draft, preserved for reference. Includes the privacy-preserving architecture (boolean output, no persistent identifiers, no issuer callback, segregation from advertising, sunset clause, hardcoded fee caps, narrowed strict liability, kinship caregivers, two-thirds threshold for intermediary remedy, research carve-out, coordinated vulnerability disclosure, eighteen-month implementation runway) but does not yet include the multi-issuer requirement, the adult-side scope limitation, or the percentage-based pricing structure.

## What changed between versions

The high-level evolution:

**v1 → v2:**
- Added § 4-88-1311(k) — multi-issuer requirement (manifesto principle 10)
- Added § 4-88-1314 — adult-side scope limitation (manifesto principle 11)
- Added two new legislative findings and two new statements of intent supporting both
- Updated cross-references throughout

**v2 → v3:**
- Replaced § 4-88-1307(i) with percentage-based pricing structure including cost-recovery anchor, three-tier retailer compensation (physical card, sustained receipt activation, startup receipt activation), 36-month per-retailer startup incentive, school surplus distribution coordinated with the Department of Education, and three-year persistent-surplus price-review trigger
- Corrected § 4-88-1303(24)(C) Miller test from "AND" to "OR" to conform to *Miller v. California*, 413 U.S. 15 (1973)
- Added § 4-88-1304(g)(7) and (g)(8) — explicit non-extraterritoriality clauses addressing dormant Commerce Clause concerns under *National Pork Producers Council v. Ross*
- Added § 4-88-1307(i)(4)(G)–(J) — five-year program review and renewal mechanism for the startup receipt-activation share
- Added § 4-88-1314(g) — procedural protection of scope limitation, including single-subject requirement, separate committee hearing requirement, recorded vote requirement, public statement of effect requirement, fiscal and privacy impact statement requirement, and a companion rules mechanism requesting that each chamber adopt parallel procedural rules
- Tightened § 4-88-1314(d)(1)(A) — closed a loophole where the previous language could have been read to authorize a separate minor-specific signal
- Expanded Section 9 from a federal-law savings clause to a federal-law savings AND severability clause, with explicit findings that the privacy-protection provisions serve independent and severable purposes from the underlying age-verification duty

The v3 file includes an inline changelog at the top documenting these changes within the bill itself, in addition to the broader CHANGELOG.md at the repository root.

## Why all versions are preserved

**Auditability.** Anyone reviewing the legislative process should be able to see how the bill evolved and which provisions were added in response to which concerns.

**Forkability.** Other states adapting this work may have reasons to start from an earlier version — perhaps their state already has multi-issuer requirements in adjacent law and they don't need v2's contribution, or perhaps the political moment requires a leaner first draft. Preserving all versions lets adapters choose their starting point.

**Demonstrating that ideas matured into provisions.** The manifesto in `manifesto.md` includes twelve principles. v1 of the bill embodied ten of them. v2 closed two principle gaps. v3 added constitutional refinement, Commerce Clause hardening, procedural protection, and surplus-distribution architecture. Future contributors can see that the bill is built to enforce a published architecture, not assembled ad hoc.

## Which version is the bill

The version intended for filing and for ongoing development is **v3**. v1 and v2 are preserved for reference only. Pull requests, issues, and forks should target v3 unless they specifically address inter-version evolution.

## Companion resolutions

The v3 bill at § 4-88-1314(g)(7) requests that the House of Representatives and Senate each adopt parallel procedural rules implementing the scope-limitation procedural framework. The text of those rules is in `/companion-resolutions/chamber-rules-companion.md` and should be filed contemporaneously with the bill.
