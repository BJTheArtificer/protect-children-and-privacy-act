# Revised Fiscal Note

**Privacy-Preserving Operating System Adult Access Credential Program**
**Arkansas Cost and Revenue Estimate — Revised**
**Prepared in support of the Arkansas Protects Our Children and Our Privacy Online Act (as amended)**

---

## 1. Purpose and revisions from prior note

This revised fiscal note replaces the prior note dated earlier in the legislative process. The prior note was prepared on the basis of preliminary planning assumptions, including an assumed annual credential demand of 3,000,000 events and an annual operating cost range of $190,000–$420,000. On further review, those assumptions overstated demand and understated infrastructure and personnel cost.

The principal revisions in this note are:

1. **Demand re-estimated** at approximately **750,000 credential events per year** (range 550,000–1,000,000), based on Arkansas household composition, device-replacement cycles, household formation rates, and the population of adults aging into the system annually.

2. **Initial inventory re-scaled** to approximately **1,500,000 cards** (covering the upper end of expected annual demand with full contingency reserve), with a hybrid distribution model that combines pre-manufactured cards and receipt-printed credentials.

3. **Annual operating cost re-estimated** at approximately **$750,000** (range $650,000–$1,090,000), reflecting the redundancy, resiliency, security, and incident-response standards required by § 4-88-1311(f).

4. **Startup and integration cost re-estimated** at approximately **$2,000,000** (range $1,500,000–$3,500,000), reflecting the actual scope of state-certified interface design, multi-region infrastructure, retailer onboarding, and security review.

5. **Distribution architecture analysis added** (Section 6), comparing pre-manufactured card distribution, receipt-printed POS distribution, and the hybrid model recommended for adoption.

6. **Fee structure unchanged.** The $6.00 retail price (with $1.00 retailer share and $5.00 state share) remains workable, and the program remains capable of self-funding under the revised assumptions.

---

## 2. Demand estimate

The credential is required for an operating system installation event as defined in § 4-88-1303. Not every device purchase triggers a credential event; many device replacements migrate an existing user account forward without resetting the adult-enabled state. The triggering events are primarily:

| Event category | Estimated annual Arkansas events |
|---|---|
| First-time device setup in a new or newly-formed household | 25,000–35,000 |
| Adults aging into the system (eighteenth birthday, first independent device) | 35,000–40,000 |
| Device replacement that triggers a fresh OS install or new local user context | 400,000–700,000 |
| Used device transfer, gift, inheritance, or family handoff | 50,000–100,000 |
| Reinstall, recovery, or repair requiring renewed adult setup | 50,000–150,000 |
| **Total estimated annual credential events** | **560,000–1,025,000** |

Note: Permit holders consume a long-term adult access credential rather than one-time cards for repeated installs and are excluded from one-time card demand.

For planning purposes, this note adopts a midpoint planning estimate of **750,000 credential events annually**.

---

## 3. Initial card inventory

Under a hybrid distribution architecture (Section 6 below), pre-manufactured cards are still required for retail rack distribution, gift-purchase use, and channels where receipt-printed credentials are not practical. The recommended initial inventory is:

- Estimated annual upper-bound demand: **1,000,000 events**
- Pre-manufactured inventory share (50% of total events under the hybrid model): **500,000 cards/year**
- Initial inventory with 100% contingency on first-year pre-manufactured share: **1,000,000 cards**
- Strategic reserve for outage, recall, and reorder lead time: **500,000 cards**
- **Recommended initial print run: 1,500,000 cards**

This represents a substantial reduction from the prior note's 4,500,000-card initial run while still maintaining a realistic operational reserve.

---

## 4. Card production cost

Estimated total card manufacturing cost for **1,500,000 cards** at varying security-feature levels:

| Security feature level | Per-card cost | Total inventory cost |
|---|---|---|
| Basic plastic with thermal printing | $0.12 | $180,000 |
| Standard with barcode and tamper-evident concealment | $0.25 | $375,000 |
| Enhanced with NFC and security printing | $0.40 | $600,000 |
| High-security with holographic and microprinting elements | $0.75 | $1,125,000 |

For fiscal planning purposes, this note adopts the **enhanced moderate estimate**:

**1,500,000 cards × $0.40 = $600,000**

This security-feature level is appropriate because the credential, while not a high-value bearer instrument like a lottery ticket, must resist mass counterfeiting that would compromise the integrity of the program. The $0.40/card estimate is consistent with state-issued credential card production through 2025.

---

## 5. Retail pricing and state receipts (unchanged)

Under the proposed pricing structure as codified in § 4-88-1307(i):

* Retail sale price per card: **$6.00**
* Retailer share per card: **$1.00**
* State gross receipt per card: **$5.00**

If the full initial pre-manufactured inventory of **1,500,000 cards** is sold over its useful life:

* Total consumer sales: **$9,000,000**
* Total retailer commissions: **$1,500,000**
* Total state gross receipts: **$7,500,000**

If steady-state annual demand of **750,000 events** is met through the hybrid model (split roughly evenly between pre-manufactured cards and receipt-printed credentials), state gross receipts at steady state would be:

* Annual consumer sales (at midpoint demand): **$4,500,000**
* Annual retailer commissions: **$750,000**
* Annual state gross receipts: **$3,750,000**

---

## 6. Distribution architecture analysis

The original note assumed exclusive distribution of pre-manufactured cards through retail rack placement modeled on gift card distribution. Further review of available distribution architectures supports a **hybrid model** combining two distribution channels.

### 6.A. Pre-manufactured card distribution

This model leverages existing US retail gift card infrastructure operated by national gift card service providers, which provides:

- Established real-time activation messaging from point-of-sale terminals to central authorization
- Per-card unique identifier tracking
- Fraud detection on activation patterns
- Settlement and remittance to retailers
- Replacement, refund, and dispute handling

Cards are physically manufactured in advance, distributed to retailer racks, sold inactive, and activated only upon ID-verified purchase. This model has the following characteristics:

**Advantages:**
- Leverages existing infrastructure already deployed at major retailers
- Strong customer experience: durable physical card retained in wallet
- Supports gifting use cases (e.g., grandparent purchasing setup card with new device for adult grandchild)
- Familiar consumer model
- Faster retailer onboarding because existing rails are reused

**Disadvantages:**
- Inventory carrying cost, including shrinkage, expiration, and storage
- Initial capital outlay for card production
- Logistics burden for distribution and reorder
- Replacement load for damaged or lost physical cards

**Estimated cost:** $0.40/card production plus 5–10% annual inventory carrying cost on outstanding inventory, plus distribution logistics estimated at $80,000–$150,000 annually.

### 6.B. Receipt-printed POS credential distribution

This model generates a fresh high-entropy credential at the point of sale and prints it on the customer's receipt or a dedicated companion receipt slip. The point-of-sale terminal, after the cashier confirms the customer is at least eighteen (18) years of age via government-issued identification, sends an authorization request to the state-certified backend; the backend generates a unique credential, marks it activated, sets an expiration window, and returns the credential to the POS terminal for printing.

**Advantages:**
- No physical card inventory
- No inventory shrinkage, expiration, or storage cost
- Lower per-credential marginal cost (receipt paper is already at every point of sale)
- Tightly bound to the moment of sale, reducing fraud surface for credential theft from inventory
- Natural pairing with device purchases at electronics and computer retailers

**Disadvantages:**
- Thermal-printed receipts fade over time, particularly in heat; durability concerns reduce customer experience quality
- Receipts are easily lost, misplaced, or discarded
- Awkward as a gift item
- Requires custom POS software integration at each retailer chain, which existing gift card rails do not provide out of the box
- Slower retailer onboarding, particularly for smaller chains and independent retailers
- Higher backend availability requirement (real-time credential generation is on the critical path of every sale)

**Estimated cost:** $200,000–$500,000 one-time POS software integration per major retailer chain partner, plus a higher availability requirement on the state backend (driving operating cost upward by an estimated $50,000–$100,000 annually).

### 6.C. Hybrid model (recommended)

The hybrid model deploys both channels:

- Pre-manufactured cards distributed through general retail (grocery, drug store, big-box gift card racks) for general consumer access, replacement purchases, and gift use
- Receipt-printed credentials generated at point of sale at participating electronics, computer, and device retailers, bundled with device purchases

This captures the strengths of both models. The pre-manufactured channel uses established gift card rails and reaches the broadest retail footprint with the lowest integration cost per retailer. The receipt-printed channel reduces inventory pressure for the most common use case (credential purchased at the same time as a device) and is attractive to electronics retailers who do not currently stock gift cards but who have a natural customer flow for the product.

The hybrid model also provides redundancy: if either channel experiences disruption, the other remains available, supporting the continuity goals of § 4-88-1311(f).

### 6.D. Note on existing rails

Whether the gift card rails operated by major service providers can be directly leveraged, or whether a dedicated state contract is required, is a procurement question that should be resolved by the Department of Finance and Administration in coordination with the Office of State Technology before final implementation. A contract with an existing gift card service provider would substantially reduce backend implementation cost. A bespoke implementation would offer greater control over data minimization but at higher implementation cost. Both options should be evaluated in the procurement phase.

---

## 7. Annual operating cost (revised)

The prior note's annual operating range of **$190,000–$420,000** materially understated the cost of the redundancy, resiliency, and security obligations imposed by § 4-88-1311(f). Realistic annual operating cost under the amended bill includes:

| Cost category | Annual estimate |
|---|---|
| Multi-region cloud infrastructure (active-active failover, encrypted storage, WAF, DDoS protection, GovCloud or comparable government-grade hosting) | $80,000–$150,000 |
| Security monitoring (SIEM, 24-hour SOC coverage by contract or in-house) | $120,000–$200,000 |
| Annual independent security assessment and penetration testing | $40,000–$80,000 |
| Compliance, audit, and breach-readiness (SOC 2 Type II, state records retention, incident response) | $30,000–$60,000 |
| Personnel (technical operations lead, partial-FTE security analyst, fraud reviewer, customer service supervisor, vendor management) | $300,000–$450,000 |
| Customer service and replacement processing (estimated 15,000–22,500 replacement transactions annually at 2–3% rate against 750,000 events) | $80,000–$150,000 |
| Coordinated vulnerability disclosure program, bug bounty pool, and program administration | $20,000–$50,000 |
| Contingency for outage response, surge support, and unplanned remediation | $40,000–$80,000 |
| **Estimated annual operating range** | **$710,000–$1,220,000** |

For fiscal planning purposes, this note adopts a moderate planning assumption of:

**Annual operating cost: $750,000**

If the receipt-printed channel is heavily adopted, real-time backend availability requirements increase and annual operating cost may rise toward the high end of the range.

---

## 8. Startup and integration cost (revised)

The prior note's startup estimate of **$250,000–$1,000,000** materially understated the actual scope of work. Realistic startup cost includes:

| Cost category | Estimated startup cost |
|---|---|
| State-certified interface design, technical specification, and standards development | $200,000–$400,000 |
| Backend implementation (credential lifecycle, activation API, redemption API, blacklist, fraud controls) | $400,000–$800,000 |
| Multi-region infrastructure provisioning, security architecture, and disaster recovery setup | $200,000–$400,000 |
| Retailer onboarding, including POS integration with major chains and gift card rail integration | $300,000–$700,000 |
| Initial card production (1.5M cards at $0.40) | $600,000 |
| Security review, penetration testing, and independent assessment of initial system | $100,000–$200,000 |
| Public education and consumer information campaign | $100,000–$300,000 |
| Procurement, vendor management, and contracting overhead | $80,000–$150,000 |
| Rule-making, public comment, and administrative setup | $50,000–$100,000 |
| Contingency reserve | $200,000–$400,000 |
| **Estimated startup range** | **$2,230,000–$4,050,000** |

For fiscal planning purposes, this note adopts a moderate planning assumption of:

**Startup and integration cost: $2,000,000**

This is roughly four times the prior note's moderate startup estimate.

---

## 9. First-year cost estimate (revised)

Using the revised moderate planning assumptions:

| Line item | Amount |
|---|---|
| Card printing (1.5M × $0.40) | $600,000 |
| Annual operations (year one) | $750,000 |
| Startup and integration | $2,000,000 |
| **Estimated first-year total cost** | **$3,350,000** |

### Lean scenario

| Line item | Amount |
|---|---|
| Card printing (1.5M × $0.25) | $375,000 |
| Annual operations | $650,000 |
| Startup and integration | $1,500,000 |
| **First-year total** | **$2,525,000** |

### Higher-feature scenario

| Line item | Amount |
|---|---|
| Card printing (1.5M × $0.75) | $1,125,000 |
| Annual operations | $1,090,000 |
| Startup and integration | $3,500,000 |
| **First-year total** | **$5,715,000** |

The likely first-year appropriation request is therefore in the range of **$2.5M–$5.7M**, with a moderate planning estimate of **$3.35M**.

---

## 10. Net state revenue and break-even analysis (revised)

### State per-card retained amount (moderate scenario):

- Sale price: **$6.00**
- Retailer share: **$1.00**
- State gross: **$5.00**
- Per-card production cost (pre-manufactured channel): **$0.40**
- Per-credential marginal cost (receipt-printed channel): approximately **$0.05** (paper, processing, settlement)
- Blended per-credential retained amount before operating overhead (assuming 50/50 hybrid mix): approximately **$4.78 per credential**

### Break-even thresholds:

| Cost target | Credentials required to recover (at $4.78 retained) |
|---|---|
| Annual operations of $750,000 | ~157,000 credentials/year |
| First-year operations + reserve of $1,000,000 | ~210,000 credentials/year |
| Full first-year cost of $3,350,000 (recovered over multi-year horizon) | ~700,000 credentials cumulative |

Against estimated annual demand of 750,000 credential events, the program reaches operational break-even at approximately 21% of annual demand and full first-year cost recovery within roughly one year of full deployment. The program remains feasibly self-funding under the revised assumptions, though with a longer recovery curve than the prior note suggested.

---

## 11. Multi-year fiscal projection (moderate scenario)

| Year | State gross receipts | Operating cost | Startup amortization | Net to fund |
|---|---|---|---|---|
| Year 1 (partial deployment) | $1,500,000 | $750,000 | $2,000,000 | **($1,250,000)** |
| Year 2 | $3,750,000 | $750,000 | — | **$3,000,000** |
| Year 3 | $3,750,000 | $775,000 | — | **$2,975,000** |
| Year 4 | $3,750,000 | $800,000 | — | **$2,950,000** |
| Year 5 | $3,750,000 | $825,000 | — | **$2,925,000** |
| **Five-year cumulative** | **$16,500,000** | **$3,900,000** | **$2,000,000** | **$10,600,000** |

Under the revised moderate assumptions, the program runs a first-year deficit (covered by initial appropriation under Section 8 of the act) and reaches positive cumulative net status by year 2. Five-year cumulative net to fund, after operating cost and startup amortization, is approximately **$10.6 million**.

This margin provides a meaningful reserve to:
- Absorb demand below the midpoint estimate
- Fund permit-program operations and waivers under § 4-88-1310(d)(4)
- Support outage response and temporary alternative compliance methods under § 4-88-1305(f)
- Build a sunset-period wind-down reserve consistent with Section 10 of the act

---

## 12. Sensitivity analysis

The fiscal outcome is most sensitive to the following variables:

**Demand realization.** If actual annual demand falls below 400,000 events, the program may approach steady-state break-even but accumulate insufficient reserve to absorb cyclical variation. If demand falls below 250,000 events, the program would require continued legislative appropriation or a fee adjustment (subject to the cap and CPI indexing in § 4-88-1307(i)).

**Receipt-printed channel adoption.** If the receipt-printed channel achieves rapid adoption among major electronics and device retailers, inventory cost falls, retailer integration cost rises, and net per-credential margin improves modestly.

**Replacement and fraud rate.** The 2–3% replacement rate assumption is based on comparable credential systems. If the actual rate exceeds 5% — for example, due to thermal receipt fading driving higher replacement of receipt-printed credentials — annual customer service and replacement cost may rise by $100,000–$200,000.

**Compliance enforcement load.** Sustained heavy use of the notice-and-cure procedure under § 4-88-1313, particularly the extended-cure mechanism under subsection (g), could increase Office of State Technology administrative cost beyond the personnel estimate. This is not a fund cost but a general administrative cost that may require separate appropriation.

---

## 13. Fiscal effect

The fiscal effect of the revised program is likely to be **net favorable over a five-year horizon** if:

- Demand realizes within the 550,000–1,000,000 annual range
- Card production and POS integration costs are controlled
- Startup and infrastructure scope remains disciplined
- The hybrid distribution model achieves meaningful adoption in both channels
- Replacement and fraud rates remain within historical norms for comparable credential systems

The primary cost pressures are:

- Multi-region infrastructure and 24-hour security operations under § 4-88-1311(f)
- POS software integration with retailer chains
- Customer service and replacement load
- Sustained compliance enforcement under § 4-88-1313

The primary strengths of the model are:

- Self-funding capability over a multi-year horizon
- Predictable per-credential revenue
- Statutory fee cap providing legislative control over revenue ceiling
- Hybrid distribution providing operational redundancy
- Sunset clause forcing periodic legislative review of cost-effectiveness

---

## 14. Preliminary conclusion

Using a revised initial print run of **1,500,000 cards** under a hybrid distribution model, based on **750,000 estimated annual credential events**, the proposed adult access credential program appears **fiscally feasible over a five-year horizon**, though with substantially larger first-year appropriation requirements than the prior note suggested.

Under the moderate planning scenario, the program would require approximately:

- **$3,350,000 in first-year total cost** (covered by combination of fee revenue and initial appropriation under Section 8 of the act)
- **$750,000 in recurring annual operating cost**
- **$10,600,000 in cumulative five-year net to fund**, providing a reserve sufficient for cyclical variation, permit-program operations, outage response, and sunset wind-down

At the proposed $6 retail price, with $1 paid to the retailer and $5 remitted to the state under § 4-88-1307(i), the program is capable of covering inventory production, technical operations, staffing, retailer incentives, and startup integration over a multi-year horizon while remaining self-funding at steady state.

---

## 15. Caveats and procurement recommendations

This fiscal note relies on planning assumptions derived from comparable state credential programs, gift card industry infrastructure, and US retail electronics markets through 2025. Final cost estimates should be validated by:

1. Formal procurement consultation with major gift card service providers regarding rail availability and integration cost
2. Bid-quality quotes from card production vendors for the security-feature specification ultimately selected
3. Department of Information Services rate-card validation of personnel and infrastructure cost assumptions
4. Survey of major Arkansas retail chains regarding POS integration appetite and timeline
5. Independent demand modeling with US Census household and device data specific to Arkansas

The Office of State Technology and Department of Finance and Administration should jointly conduct this validation before final appropriation request.

The annual reporting requirement under Section 8(c) of the act will provide feedback for refinement of these assumptions over the program's first operational years and inform any reauthorization decision under Section 10.
