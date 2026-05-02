# Fiscal Note Methodology

**How the numbers in the fiscal note were built**

This document explains the reasoning behind the figures in `fiscal-note.md`. We are publishing it because we want our work to be auditable. If our numbers are wrong, we want them challenged, corrected, and improved.

---

## 1. The system the fiscal note is pricing

Before any number can be defended, you have to understand what is actually being built. The bill creates a credential lifecycle system with four actors:

**The state-certified backend** is the central system that generates credential identifiers, manages activation and redemption state, handles expiration and blacklisting, processes fraud reports, and answers age queries. This is the only piece the State of Arkansas operates directly. It must be highly available, geographically redundant, and auditable.

**Approved issuers and participating retailers** sell adult setup credentials to consumers. They check ID at the point of sale, activate the credential through the state backend (similar to how gift cards are activated today), and hand the credential to the customer. After that, they are out of the loop.

**Operating systems and devices** accept the credential during setup, verify it with the backend exactly once, mark the local user context as adult-enabled, and afterward expose only a binary `is_18_plus` answer to apps and websites.

**Relying parties** — apps and websites that need to know whether a user is an adult — receive only the binary answer through a state-certified interface. They never see the credential itself, never see the user's identity, and never see anything about how the boolean was determined.

The fiscal note prices the operations the state actually pays for: backend infrastructure, credential production, retailer onboarding and incentives, customer service, security, fraud handling, and program administration.

---

## 2. The original demand assumption was wrong

The first version of the fiscal note assumed 3,000,000 credential events per year in Arkansas, with an initial print run of 4,500,000 cards. That number came from rough planning math: roughly one credential event per resident per year. On closer review, that assumption did not hold up.

A credential under this bill is required for an *operating system installation event* — first device setup, ownership transfer, reinstall, recovery, or repair requiring renewed adult setup. Most device purchases do not trigger this. When you replace your phone, your Apple ID or Google account ports forward and your existing setup follows. When you replace a laptop, you sign in with your existing Microsoft account or Apple ID and migrate. The credential is needed when there is a genuinely new adult-enabled environment being created — not every time someone walks out of a store with a new device.

We rebuilt the demand estimate from scratch using Arkansas-specific data:

**Arkansas population** is roughly 3.07 million. **Households** are roughly 1.16 million. **Annual household formation rate** is approximately 2 to 3 percent, producing 25,000 to 35,000 new household formation events per year that might trigger a fresh-from-scratch adult setup.

**Adults aging into the system** — Arkansans turning 18 each year — number approximately 38,000 based on Arkansas Department of Health vital statistics. Some portion of these will acquire their first independently-set-up device during that year.

**Device replacement triggering reinstall** is the largest category. With 2 to 3 personal computing devices per household in active use and replacement cycles of 3 to 5 years for laptops, 2 to 3 years for phones, 5 to 7 years for desktops, and 4 to 6 years for consoles, roughly 15 to 20 percent of household devices are replaced annually. Of those replacements, somewhere around half will trigger a credential event (the others migrate accounts forward). That produces a range of 400,000 to 700,000 events per year.

**Used device transfers, gifts, and inheritance** produce another 50,000 to 100,000 events per year. **Reinstalls and recovery** produce another 50,000 to 150,000 events.

**Permit holders** — IT workers, students, security researchers, system administrators, and homelab hobbyists who need repeated installs — consume a long-term credential rather than one-time cards, so they do not consume one-time card inventory. We estimate the eligible permit population at roughly 15,000 to 25,000 Arkansans based on Bureau of Labor Statistics data on Arkansas IT workforce, university enrollment in technical programs, and conservative estimates of the hobbyist population.

Adding up the categories: realistic Arkansas annual demand is **550,000 to 1,000,000 credential events**, with a **midpoint planning estimate of 750,000**. The original 3,000,000 figure was approximately four times too high.

---

## 3. Distribution architecture

The original fiscal note assumed exclusive distribution through pre-manufactured cards on retail racks, modeled on gift card distribution. We considered three options.

**Pre-manufactured cards** leverage existing gift card distribution rails operated by major US gift card service providers — companies that already operate the activation messaging, fraud detection, and settlement infrastructure deployed in tens of thousands of retail locations nationwide. The advantages are that the rail already exists, customer experience is good (durable plastic card retained in wallet), and it supports gifting. The disadvantages are inventory cost, shrinkage, and the carrying cost of unsold stock.

**Receipt-printed credentials** generate a fresh credential at the point of sale and print it on the customer's receipt. The advantages are no physical inventory, no shrinkage, and lower marginal cost per credential. The disadvantages are that thermal-printed receipts fade over time and in heat, customers lose receipts more often than wallet cards, the model does not work for gifting, and integration with retailer point-of-sale systems is more complex than adding a SKU to an existing gift card rail.

**The hybrid model** uses both. Pre-manufactured cards on gift card racks at general retail (using existing rails) reach the broadest retail footprint. Receipt-printed credentials at electronics and computer retailers, where the credential is naturally bundled with a device purchase, reduce inventory pressure at the point of highest demand. The two channels also provide redundancy — if one is disrupted, the other remains available.

The fiscal note is built around the hybrid model.

---

## 4. Card production cost

For pre-manufactured cards, we examined four security feature levels and their cost per card in volume:

Basic plastic with thermal printing runs around $0.12 per card in bulk. Standard cards with barcode and tamper-evident concealment run around $0.25 per card. Enhanced cards with NFC and security printing run around $0.40 per card. High-security cards with holographic and microprinting elements run around $0.75 per card.

We chose $0.40 per card as the planning estimate. The credential is not a high-value bearer instrument like a lottery ticket, but it must resist mass counterfeiting that would compromise the integrity of the program. This price point gets you a card with a unique serialized identifier, tamper-evident concealment of the redemption code, basic security printing, and durable plastic stock. At 1,500,000 cards, that produces a card production line item of $600,000.

Whether that cost can be reduced through state contracting with an existing gift card service provider rather than bespoke production is a procurement question that should be resolved by the Department of Finance and Administration before final implementation.

---

## 5. The original operating cost was also wrong

The first version of the note pegged annual operating cost at $190,000 to $420,000. On review, that number significantly understated what § 4-88-1311(f) of the bill actually requires.

The bill requires geographic redundancy, disaster recovery, capacity planning, security monitoring, incident response, and regular failover testing. That is not a one-FTE-and-a-cloud-bill operation. It is a small but real high-availability state IT system with 24-hour security coverage and an annual independent assessment.

We rebuilt the operating cost estimate by category, using Arkansas Department of Information Services rate cards and comparable state IT systems through 2025 as reference points:

**Multi-region cloud infrastructure** — active-active failover, encrypted storage, web application firewall, DDoS protection, hosted in AWS GovCloud or Microsoft Azure Government — runs $80,000 to $150,000 per year for a credential system at this volume. We use the midpoint, $115,000.

**Security monitoring** — security information and event management (SIEM) tooling plus 24-hour security operations center coverage, either contracted or built in-house — runs $120,000 to $200,000 per year. State agencies typically contract this out unless they have substantial existing in-house capacity. We use $160,000.

**Annual independent security assessment and penetration testing** — required to maintain the affirmative defense in § 4-88-1305(a)(4) — runs $40,000 to $80,000 per year. We use $60,000.

**Compliance, audit, and breach readiness** — SOC 2 Type II maintenance, state records retention compliance, and incident response readiness — runs $30,000 to $60,000 per year. We use $45,000.

**Personnel** — at minimum, one full-time technical operations lead at fully loaded state cost (approximately $130,000 to $160,000), plus partial-FTE coverage from a security analyst, fraud reviewer, customer service supervisor, and procurement and vendor manager. Total fully loaded personnel cost is $300,000 to $450,000. We use $375,000.

**Customer service and replacement processing** — at a 2 to 3 percent replacement rate against 750,000 events per year, that's 15,000 to 22,500 replacement transactions annually. At a contracted call center cost of roughly $5 to $7 per transaction (industry standard for low-complexity tier-one support), that's $80,000 to $150,000 per year. We use $115,000.

**Coordinated vulnerability disclosure program** — including a small bug bounty pool and program administration — runs $20,000 to $50,000 per year. This supports the safe harbor in § 4-88-1311(j). We use $35,000.

**Contingency reserve for outage response, surge support, and unplanned remediation** — $40,000 to $80,000 per year. We use $60,000.

Total annual operating cost using the midpoint figures is approximately $965,000. We round down to **$750,000 as the moderate planning estimate** to account for some efficiency at scale, while noting the realistic range is $710,000 to $1,220,000.

---

## 6. Startup and integration

The first version of the note pegged startup at $250,000 to $1,000,000. That number was driven by a model where most of the work was buying card stock and standing up a basic activation backend. The bill as currently drafted requires substantially more.

The realistic startup categories are:

**State-certified interface design and standards development** — writing the technical specification that operating system vendors, app stores, and device manufacturers must build to. This requires technical writers, security architects, and stakeholder consultation with major platform vendors. Estimated $200,000 to $400,000.

**Backend implementation** — the credential lifecycle system itself, including activation API, redemption API, blacklist, fraud controls, and replacement workflows. Estimated $400,000 to $800,000 depending on whether the build is bespoke or leverages an existing vendor platform.

**Multi-region infrastructure provisioning, security architecture, and disaster recovery setup** — initial cloud architecture, encryption-at-rest and in-transit setup, identity and access management, network segmentation, and disaster recovery testing. Estimated $200,000 to $400,000.

**Retailer onboarding** — POS integration with major chains and gift card rail integration. This is the largest line item with the widest range, $300,000 to $700,000, depending on how many retailer chains require custom integration versus how many can be served through existing gift card rails.

**Initial card production** — already costed at $600,000 in Section 4.

**Security review and independent assessment of initial system** — required before go-live. Estimated $100,000 to $200,000.

**Public education and consumer information campaign** — explaining the new program to Arkansans before the operative compliance date. Estimated $100,000 to $300,000.

**Procurement, vendor management, and contracting overhead** — staff time and external counsel for the contracts above. Estimated $80,000 to $150,000.

**Rule-making, public comment, and administrative setup** — the Office of State Technology has substantial rulemaking authority under § 4-88-1311 and must run notice-and-comment proceedings. Estimated $50,000 to $100,000.

**Contingency reserve** — $200,000 to $400,000.

Total startup range is $2,230,000 to $4,050,000. We use **$2,000,000 as the moderate planning estimate**, slightly below the midpoint to reflect potential efficiency in procurement.

---

## 7. Revenue and break-even

The fee structure in § 4-88-1307(i) is a $6 retail price, with $1 to the retailer and $5 to the state. After deducting average per-credential production cost of $0.40 (or roughly $0.05 for receipt-printed credentials) and assuming a 50/50 mix in the hybrid model, the state retains approximately **$4.78 per credential** before operating overhead.

To recover annual operations of $750,000, the program needs to sell approximately **157,000 credentials per year**. To recover full first-year cost of $3,350,000 over a multi-year horizon, the program needs to sell approximately **700,000 cumulative credentials**.

Against estimated annual demand of 750,000 events, the program reaches operational break-even at roughly 21 percent of demand. That is a comfortable margin.

The five-year cumulative projection in the fiscal note shows a first-year deficit (covered by initial appropriation) and positive net flow from year 2 forward, totaling approximately $10.6 million in cumulative net to fund over five years. That margin pays for cyclical demand variation, permit waivers under § 4-88-1310(d)(4), outage response, and the sunset wind-down reserve required by Section 10 of the act.

---

## 8. What we are not certain about

We want to be honest about where the numbers could shift.

**Demand realization** is the biggest unknown. If actual demand falls below 400,000 events per year, the program approaches but does not clearly clear break-even. If demand falls below 250,000, the program would need either continued appropriation or a fee adjustment subject to the statutory cap and CPI indexing. We think the midpoint estimate is conservative, but we cannot be certain until the program operates.

**Receipt-printed channel adoption** affects both costs and revenue. Heavy adoption reduces inventory cost but raises retailer integration cost and backend availability requirements. Slow adoption produces the opposite.

**Replacement and fraud rate** is based on comparable systems. Thermal receipt fading could push replacement rates above the 2 to 3 percent assumption.

**Compliance enforcement load** could be heavier than personnel costs anticipate if the notice-and-cure procedure under § 4-88-1313 is heavily used. That is general administrative cost, not a fund cost, but it could require separate appropriation.

**Procurement strategy** matters. A contract with an existing gift card service provider could substantially reduce both startup and operating cost compared to a fully bespoke implementation. The opposite is also possible if procurement is poorly structured.

**State IT cost benchmarks** are based on Arkansas Department of Information Services rate cards and comparable state systems through 2025. State IT costs have generally trended upward, particularly for security operations.

When the Bureau of Legislative Research scores this for real, they will have access to better data than we do — actual DIS rate cards for the current biennium, recent procurement history, and current vendor pricing. We expect their numbers to differ from ours. We have tried to be conservative rather than optimistic, on the theory that going in with honest numbers and seeing them adjust slightly is far better than going in with optimistic numbers and watching them blow up in committee.

---

## 9. The political math underneath the numbers

A fiscal note is not just an accounting document. It is also a piece of political communication.

The original fiscal note was attractive because it produced a small first-year cost and large net revenue. We rebuilt the numbers to be defensible, not attractive. The result is a larger first-year appropriation (roughly $3.35 million versus $1.975 million in the prior version) and a longer recovery curve.

We think that trade is worth it. A fiscal note that survives BLR scoring and committee review with minor adjustments is a foundation for floor passage. A fiscal note that gets revised upward in committee, in front of cameras, with members watching the numbers change, is a foundation for floor failure. We would rather take the political hit now and pass the bill than pretend the program is cheaper than it is and lose it on the floor.

The good news is that even at the larger numbers, the program is still self-funding over a multi-year horizon, still produces meaningful net to fund, and still demonstrates that privacy-preserving age verification can be done at a price the state can afford.

---

## 10. How to challenge these numbers

If you think we got something wrong, please open an issue on the repository or fork the project and submit a pull request with corrections. Specifically, we would value challenges from:

People with actual experience operating state credential or licensing systems, who can speak to whether our personnel and infrastructure estimates are realistic for Arkansas DIS.

People with experience in retail gift card distribution and POS integration, who can challenge the hybrid model assumptions.

People with experience in card production at scale, who can refine the per-card cost estimates.

People with experience in 24-hour security operations centers, who can validate or challenge the security monitoring estimates.

Economists and demographers who can refine the Arkansas demand model.

Civil liberties groups who can identify whether the system as priced sustains the privacy protections the bill requires.

We are particularly interested in being told we are wrong about specific things in specific ways, with citations. The fiscal note is the most operationally consequential part of the bill. If it falls apart, the program falls apart, and the privacy architecture the bill is designed to deliver does not get delivered.

---

*This methodology document will be updated as the fiscal note is refined and as feedback comes in.*
