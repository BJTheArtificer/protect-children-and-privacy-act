# Bill Text

This directory contains the legislative text of the Arkansas Protects Our Children and Our Privacy Online Act in two versions, both preserved deliberately.

## Files

**`full-bill-text-v2.md`** — the current draft. This is the version intended for filing and the version other states should fork from unless they have a specific reason to use v1. It includes all provisions described in the manifesto, including the multiple-independent-issuers requirement and the explicit limitation of the program to adult-side determination.

**`full-bill-text-v1.md`** — the prior draft, preserved for reference. This version includes all the privacy-preserving architecture (boolean output, no persistent identifiers, no issuer callback, segregation from advertising, sunset clause, fee caps, narrowed strict liability, kinship caregivers, two-thirds threshold for intermediary remedy, research carve-out, coordinated vulnerability disclosure, eighteen-month implementation runway) but does not yet include the multiple-issuers requirement or the affirmative limitation on minor-side functionality.

## What changed between v1 and v2

The substantive additions in v2 are:

- **§ 4-88-1311(k)** — A new subsection requiring the Office of State Technology to maintain a roster of not fewer than three (3) independent approved issuers in active operation in this state, drawn from at least two distinct categories (brick-and-mortar retail, online or mail-order, government office, or other authorized category). Includes a common-control limit preventing one corporate parent from holding multiple issuer slots, geographic distribution requirements, anti-gatekeeper rules, and contingency procedures if the minimum cannot temporarily be maintained.

- **§ 4-88-1314** — A new section limiting the program to adult-side determination. Prohibits any person from using the program, the state-certified interface, or any credential to identify, profile, monitor, restrict, or behaviorally control minors. Preserves independent parental control features that operate outside the state-certified interface. Requires affirmative legislative authorization for any future extension of the program to minor-side functionality. Requires the Office of State Technology to certify compliance with this section in each annual report.

- **Two new legislative findings** in § 4-88-1302(a), supporting the multi-issuer and adult-side-only architectural commitments.

- **Two new statements of intent** in § 4-88-1302(b), supporting the same.

- **Updated title block** to reflect the two new substantive commitments.

- **Cross-reference updates** throughout the bill, extending all `§§ 4-88-1306 — 4-88-1313` ranges to `§§ 4-88-1306 — 4-88-1314` so the new section is properly inside the scope, the AG enforcement authority, the rulemaking authority, the safe harbor presumption, and the sunset clause.

## Why both versions are preserved

Three reasons:

**Auditability.** Anyone reviewing the legislative process should be able to see how the bill evolved, which provisions were added in response to which concerns, and whether the drafting was done transparently.

**Forkability.** Other states adapting this work may have reasons to start from v1 — perhaps their state already has multi-issuer requirements in adjacent law, or perhaps the political moment requires a leaner first draft with fewer simultaneous fights. Preserving v1 lets adapters choose their starting point.

**Demonstrating that ideas matured into provisions.** The manifesto in `manifesto.md` includes twelve principles. v1 of the bill embodied ten of them. v2 closes the gap. Future contributors can see that the bill is built to enforce a published architecture, not assembled ad hoc.

## Which version is the bill

The version intended for filing and for ongoing development is **v2**. v1 is preserved for reference only. Pull requests, issues, and forks should target v2 unless they specifically address the v1-to-v2 evolution.
