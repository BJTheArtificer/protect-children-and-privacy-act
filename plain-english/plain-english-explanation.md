Below is a plain-English walkthrough of the **Arkansas Protects Our Children and Our Privacy Online Act** (v3), followed by an "everyman" summary for each section. This is a summary of the bill text, not legal advice.

## Overall bill summary

This bill tries to do two things at once:

First, it keeps Arkansas's rule that websites with a substantial amount of material harmful to minors must verify that users are adults before allowing access.

Second, it tries to prevent age verification from becoming a broad identity-tracking system. Instead of every website collecting IDs, birth dates, names, or reusable adult identity tokens, the bill creates a state-certified age-assurance system where, for covered implementations, the outside world receives only one answer: **is this user 18 or older — yes or no?**

The bill also creates one-time adult setup credentials sold at retail, longer-term adult access permits for technical users, strong privacy limits, liability rules, a state fund, administrative procedures, narrow outage fallback rules, anti-monopoly requirements for credential issuers, and a five-year sunset that forces the legislature to actively decide whether to keep the program.

A note on what the bill regulates: the privacy architecture in this bill applies specifically to **covered implementations** — operating systems, devices, app stores, and certain consumer virtual computing services. The basic age-verification duty for adult websites in existing Arkansas law continues to apply, and websites that aren't using a covered implementation can still use other reasonable age-verification methods.

---

# Section-by-section explanation

## Section 1 — Title

**Plain-English explanation:**
This section gives the act its official name: the **"Arkansas Protects Our Children and Our Privacy Online Act."** It is marked "do not codify," meaning this naming section itself does not get added as a permanent section of the Arkansas Code, though most of the substantive parts of the bill *are* codified into existing Arkansas Code subchapter 4-88-13.

**Everyman summary:**
This section just names the bill.

---

## Section 2 — Legislative findings and intent

**Plain-English explanation:**
This section explains why the General Assembly is passing the bill and what goals it is trying to achieve. It says Arkansas has an interest in protecting minors from harmful sexual material online, but also has an interest in protecting adults from being tracked or forced to repeatedly hand over sensitive identity information. It criticizes age-verification systems that collect exact birth dates, government IDs, identity tokens, or persistent identifiers.

The section says the state prefers a narrow model: an adult proves adulthood once through an approved issuer, and later systems only receive a simple adult/not-adult signal. It also says the system should avoid central logs, routine callbacks to issuers, and single private gatekeepers. It emphasizes that the program is only about determining whether someone is an adult, not about profiling or controlling minors.

The section also notes that other states and the federal government are moving toward operating-system-level or device-level age-assurance laws, and that Arkansas wants to shape what that architecture looks like before it is built badly.

**Everyman summary:**
Arkansas is saying: "Operating-system-level age checks are coming whether we like it or not. We want to keep kids away from harmful adult material, but we do not want this to turn into a giant online ID-tracking system. So we're going to define how it works in Arkansas before someone else builds it the wrong way."

---

## Section 3 — Definitions

**Plain-English explanation:**
This section defines the key terms used throughout the bill. It defines who counts as an adult or minor, what "age-assurance data" means, what a "boolean age response" is, what a "covered implementation" is, what counts as a personal computing device, what a one-time adult setup credential is, what an adult access permit is, and what "material harmful to minors" means.

A major feature of this section is that "age-assurance data" is defined very broadly. It includes things like exact age, date of birth, ID images, ID numbers, biometric identifiers, persistent identifiers, device fingerprints, geolocation, browsing data, and records of access to harmful material. That broad definition supports the privacy restrictions later in the bill.

It also defines "material harmful to minors" using a three-part standard borrowed from federal obscenity case law: material appealing to prurient interest for minors, patently offensive sexual depictions or descriptions as to minors, and lacking serious literary, artistic, political, **or** scientific value for a reasonable seventeen-year-old. (V3 corrected this from "and" to "or" to match the federal standard.)

The "substantial portion" definition that triggers the website age-verification duty is more than 33.33% of total material on a website meeting the harmful-to-minors definition.

**Everyman summary:**
This section is the bill's dictionary. It carefully defines the system's parts and makes clear that sensitive identity and browsing information count as protected data that the system isn't allowed to collect or share.

---

## Section 4 — Reasonable age verification methods and exclusive privacy-preserving compliance path

**Plain-English explanation:**
This is one of the central sections of the bill. It keeps the basic rule that a commercial entity must use reasonable age verification before allowing access to a website with a substantial portion of material harmful to minors.

For covered implementations, however, it creates an exclusive Arkansas compliance path. The only lawful external age-assurance output is an age query and a boolean response through the state-certified interface. In plain terms, the system may ask only: **"Is the current user 18 or older?"** The answer may only be **true/false** or **1/0**, with no other information attached.

This section also prevents companies from demanding extra identifying information after receiving a "true" adult response. It says companies cannot condition access through a covered implementation on the user submitting a date of birth, legal name, government ID image, government ID number, reusable adult token, or other additional information beyond what the bill allows.

The section also addresses out-of-state issues. Covered implementations have two options: they can apply the Arkansas system only to Arkansas users using limited, privacy-preserving methods (like a coarse network-derived region indicator), or they can voluntarily apply the system uniformly to all of their users without trying to identify who is in Arkansas. The bill explicitly states that Arkansas is *not* requiring companies to apply Arkansas standards to users located outside Arkansas — that choice is up to the company.

**Everyman summary:**
For phones, computers, tablets, app stores, and similar systems, the answer the outside world gets is just "adult" or "not adult." Companies don't get your name, birthday, ID, location history, browsing history, or a reusable adult identity badge. And companies can choose whether to limit Arkansas's rules to Arkansas users or just apply them to everyone — Arkansas isn't telling other states how to live.

---

## Section 5 — Liability, safe harbor, and limitations

**Plain-English explanation:**
This section explains who can be sued or held responsible and under what circumstances.

A commercial entity can be liable if it knowingly publishes or distributes harmful-to-minors material on a covered website and fails to use reasonable age verification. The section then creates **strict liability** for core privacy violations. Strict liability means the company is responsible regardless of whether they meant to do it. The strict-liability list covers sending more than a boolean age response, collecting prohibited age-assurance data, using the data for advertising or profiling, violating issuer-callback limits, or misusing Arkansas applicability data.

For other operational violations — things like recordkeeping or audit-procedure violations — liability generally requires knowing or reckless conduct. The section also gives a limited defense for security breaches if the defendant had reasonable cybersecurity controls in place that conformed to a recognized industry framework (such as NIST, ISO 27001, SOC 2, or CIS Controls), followed those controls, responded properly, notified authorities and affected individuals, and cooperated in remediation. But that defense does not protect intentional misuse, sale, profiling, advertising use, or other non-security violations.

This section also creates safe harbors. A commercial entity that uses the state-certified interface properly and relies in good faith on the boolean result is protected as to the sufficiency of age assurance. It also protects entities before the operative compliance date and during properly authorized temporary fallback periods when the state system is down.

It includes exceptions for bona fide news-gathering organizations, cloud providers that are not covered consumer virtual computing services, ISPs, search engines, and similar intermediaries that merely provide access or connectivity and are not responsible for creating the harmful content.

Finally, it creates liability for knowingly and wittingly giving adult credentials to unrelated minors, while protecting people who reasonably rely on facially valid proof of adulthood. There's a complete affirmative defense for retailers and issuers who check ID in a reasonable way, even if the ID later turns out to be fake — unless they actually knew or deliberately ignored signs that it was fake.

**Everyman summary:**
If companies ignore the age-check rule, they can be liable. If they misuse age-check data — selling it, profiling people with it, using it for ads — they can be liable even if they claim it was an accident. Companies that use the official system correctly and act in good faith get protection. Cashiers and stores that check ID in good faith are protected if the ID turns out to be fake.

---

# Section 6 — New Arkansas Code sections 4-88-1306 through 4-88-1314

Section 6 is the largest part of the bill. It adds several new code sections.

---

## § 4-88-1306 — Scope of covered implementations

**Plain-English explanation:**
This section limits what the new operating-system/device/application-store age-assurance rules apply to. They apply only to covered implementations used for Arkansas users, and only with respect to personal computing devices or consumer virtual computing services used as substitutes for personal computers.

The section excludes many ordinary connected devices and infrastructure products, such as routers, modems, smart speakers, cameras, thermostats, appliances, wearables mainly used for health or fitness, vehicles, medical devices, printers, point-of-sale terminals, smart-home hubs, and similar embedded or single-purpose devices. It says a device is not covered merely because it has software, connects to the internet, uses an operating system, has a touchscreen/camera/microphone, or allows limited configuration.

The controlling question is whether the device or service is primarily offered as a general-purpose personal computing environment for ordinary end-user use.

**Everyman summary:**
This is aimed at computers, phones, tablets, gaming consoles, app stores, operating systems, and similar general-purpose computing systems — not your thermostat, doorbell camera, smart speaker, fitness tracker, or refrigerator.

---

## § 4-88-1307 — One-time adult setup credentials

**Plain-English explanation:**
This section creates the one-time adult setup credential. An adult can prove adulthood once for a specific operating system installation event, such as setting up a new device, reinstalling an operating system, transferring ownership, repairing, or recovering a device.

The credential is one-time use, short-lived before use, invalid after redemption, and must be purged after expiration or use. It may be physical or digital, such as a printed activation card, scratch-off code, NFC tag, or digital setup token. An ordinary adult can buy one at a participating retailer (alongside the device or operating system they're activating) by showing a valid government ID. The retailer is not allowed to keep a copy of the ID or record information beyond what's needed to issue the credential.

The credential cannot become a reusable adult badge, named account token, or persistent identity credential. It also cannot create a device-wide assumption that every future user of the device is an adult — each user profile gets its own determination.

This section also sets up pricing and retailer compensation. The bill recommends, but does not mandate, an initial maximum retail price of about **$6.00** per one-time credential. The Office of State Technology sets the actual maximum by rule based on cost recovery. Retailers may receive different compensation shares depending on how they issue the credential:

- **Physical card issuance** (pre-printed cards on a rack) — recommended at about 16⅔% of the price.
- **Sustained receipt-printed activation** (printed at checkout by a retailer that has built point-of-sale integration) — recommended at about 25%.
- **Startup receipt-printed activation** (a higher rate to reward retailers who invest early in building the integration) — recommended at about 33⅓%, applies to each retailer for 36 months from when their system is certified.

The startup tier has a **five-year program-wide review and sunset**: it expires on June 30 of the fifth full fiscal year after the operative compliance date unless the General Assembly votes to renew it. Retailers already in their 36-month window get to finish out their term, but no new retailer onboards at the startup rate after the sunset.

The section also creates rules for maintaining a reasonable reserve and using any surplus. Surplus may support school technology, STEM curriculum (with attention to K-6 computer science capacity), classroom supplies, and other lawful educational purposes coordinated with the Department of Education. The bill is explicit that the program is not supposed to become a general revenue source for the state, and if surplus persists for three years, the Office of State Technology must consider lowering the credential price.

**Everyman summary:**
An adult can buy a one-time activation code for about $6 at a store like Walmart or Best Buy when they're buying a new device or reinstalling an operating system. The store keeps a small share to compensate for the work; the rest goes to running the program. The codes are temporary, privacy-preserving, and not reusable as an online ID. If the program ever runs a surplus, that money helps Arkansas schools — but the program isn't supposed to become a money-maker for the state.

---

## § 4-88-1308 — Single age signal and telemetry limits

**Plain-English explanation:**
This section is the core privacy wall. It says covered implementations cannot ask for, transmit, receive, store, sell, license, disclose, or rely on any age signal other than the age query and boolean age response.

It specifically bans use or retention of legal names, exact ages, dates of birth, government ID images, government ID numbers, biometric identifiers, device fingerprints, stable account identifiers, stable device identifiers, reusable adult tokens, persistent cross-site credentials, browsing history, search history, viewing history of harmful material, and most geolocation data.

It also bans secondary use of age-assurance data. That means no selling, licensing, trading, repurposing, profiling, advertising, or unrelated disclosure. Age-assurance data must be **segregated** from advertising, recommendation, ranking, personalization, pricing, and profiling systems — meaning the data has to live in a separate place from the company's marketing and ad-targeting infrastructure.

The section allows limited aggregate, non-identifying research, journalism, government reporting, and legislative oversight — so academics and reporters can study how the system is working without anyone tracking individual users.

**Everyman summary:**
The system can only answer "18 or older?" It cannot become a tracking tool, an ad-targeting tool, a browsing-history database, or a hidden identity database. Companies can't quietly route this data into their advertising systems.

---

## § 4-88-1309 — Issuer callback prohibited for ordinary later use

**Plain-English explanation:**
This section prevents approved issuers from staying "in the loop" after a credential is issued and redeemed. The issuer cannot be contacted every time an adult opens a site, installs software, uses an app, enters an adult community, browses lawful adult material, or uses an unrestricted operating system.

The system must work locally as much as reasonably possible, without routine issuer callbacks. The bill expressly says **no company and no government office may operate as a central monitor of lawful adult access.**

There are narrow exceptions for replacement, revocation, blacklist administration, fraud prevention, outage recovery, permit renewal, and lawful process (like a valid court order).

**Everyman summary:**
Once you prove you're an adult, the place that issued your credential should not get pinged every time you do something online. There's no central log of what adults are doing.

---

## § 4-88-1310 — Adult access permits

**Plain-English explanation:**
This section creates an adult access permit for people who repeatedly install, reinstall, test, repair, virtualize, deploy, or administer operating systems. Eligible users include IT workers, students, educators, security researchers, system administrators, software developers, repair technicians, virtualization or cloud engineers, homelab users, and similar technical users.

The permit process must be low-burden. Applicants need to prove they are adults, state their qualifying use, promise not to knowingly give the credential to unrelated minors, agree to report compromise, agree that compromised credentials may be blacklisted, and renew at intervals set by rule. Renewal cannot be more frequent than annually.

The permit fee is capped at **$25.00 per renewal term**, subject to limited inflation adjustments unless the General Assembly authorizes a larger increase. The Office of State Technology may reduce or waive fees for students, educators, low-income applicants, or others for whom the fee would be a barrier.

A permit holder can receive a **long-term adult access credential** so they don't have to keep buying one-time codes every time they reinstall a system.

**Everyman summary:**
IT workers, students, repair people, developers, and homelab hobbyists who constantly reinstall systems can pay up to $25/year for a longer-term credential instead of buying one-time codes over and over. Students and low-income applicants can get reduced or waived fees.

---

## § 4-88-1311 — Administration, enforcement, and rulemaking

**Plain-English explanation:**
This section assigns responsibilities. The Office of State Technology administers the technical parts of the program and writes rules. The Attorney General enforces the law and may bring actions under the Arkansas Deceptive Trade Practices Act.

The rules must cover approved issuers, retailer participation, credential standards, permit issuance, renewal, revocation, replacement, blacklist procedures, data minimization, audit logging limits, issuer-callback restrictions, technical interface requirements, availability, resiliency, outages, fallback procedures, fraud prevention, security requirements, breach response, and successor local implementations.

The section requires the state-certified interface to have redundancy, resiliency, backup capacity, disaster recovery, peak-demand capacity, security monitoring, failover testing, and audit procedures that do *not* log lawful adult browsing activity. The state has to actually build a reliable system, not skimp on it and rely on the outage-fallback exception.

It also requires due-process protections for issuer suspension, permit denial or revocation, long-term credential revocation, and blacklist placement. Emergency action is allowed for fraud, compromise, misuse, or security threats, but affected people must receive prompt notice and expedited review. There's also a coordinated vulnerability disclosure policy that protects security researchers who report problems in good faith.

**The blacklist works at the credential level, not the person level.** When a credential is invalidated (because it was lost, stolen, or compromised), only that specific credential is blacklisted. The person can get a replacement credential without redoing the whole age-proofing process, and is not banned from getting future credentials.

This section also requires **multiple independent approved issuers**. The Office of State Technology must maintain at least three active approved issuers from at least two different categories — such as retail issuers, online or mail-order issuers, government offices, or other approved categories. **No single corporate parent can control more than one approved issuer slot.** The goal is to make sure no one company becomes the gatekeeper for adult access in Arkansas. The rules also prohibit exclusive-dealing arrangements and require geographic distribution so that urban, suburban, and rural Arkansans all have reasonable physical access to credential issuance.

**Everyman summary:**
This section tells the state how to run the system, how to keep it reliable, how to prevent any one company from monopolizing it, how to protect people from wrongful denial, and how to enforce the rules. If your credential gets stolen, you can get a replacement without going through the whole process again. And there always have to be at least three independent companies competing to issue credentials.

---

## § 4-88-1312 — Arkansas Child Protection and Online Privacy Fund

**Plain-English explanation:**
This section creates the **Arkansas Child Protection and Online Privacy Fund** on the state's books. Money from credential sales, permit fees, appropriations, grants, gifts, interest, and other lawful sources goes into the fund.

The fund can be used only for administering the program, including building and maintaining the state-certified interface, credential systems, issuer support, retailer compensation, security, audits, public education, enforcement support, replacement processes, outage response, and authorized surplus distributions to schools.

The fund is meant to support the program, not become general state revenue. The bill repeatedly emphasizes a "self-funding to the maximum extent practicable" standard.

**Everyman summary:**
This creates the dedicated bank account for the program. Money from the system pays for the system. Extra money may support schools under the bill's rules — but the program isn't a piggy bank for the state.

---

## § 4-88-1313 — Notice, cure, and remedial procedures

**Plain-English explanation:**
This section creates a structured process for notices, violations, cures, and remedies. Any person can submit a sworn complaint (a "covered notice") to the Attorney General about an alleged violation. The notice has to be specific and made under penalty of perjury — it can't be a fishing expedition.

The Attorney General forwards facially sufficient notices to the operator within two business days. The operator then has **five business days** to either fix the problem, remove the offending material, or file a counter-notice explaining why no fix is needed. An operator that cures within the window is generally not liable for the alleged conduct, with exceptions for knowing violations, cases where a minor actually accessed harmful material, or repeat violations within the past 12 months.

For systemic technical violations that genuinely can't be fixed in five business days (because they require re-engineering, vendor coordination, or hardware replacement), there's an **extended cure** procedure of up to 30 days, with a possible 30-day extension for extraordinary circumstances. To get the extended cure, the operator has to apply quickly, propose a remediation plan, and implement interim mitigation (like suspending the affected feature). This isn't available for knowing violations or for cases where a minor actually accessed harmful material.

The section also contains a **limited intermediary remedy**. In serious circumstances, after strict judicial findings supported by clear and convincing evidence, a court may order intermediaries (like ISPs or search engines) to block, restrict, or deindex access to a noncompliant website. This remedy is heavily constrained: the operator must be beyond the court's reach, the website must be more than two-thirds harmful-to-minors material, the order must be narrowly tailored, the affected parties get notice and a chance to be heard, the order is automatically stayed pending appeal, and the order cannot conflict with Section 230 or other federal law.

The section makes clear that ISPs, search engines, and other intermediaries are not required to monitor user content or evaluate third-party compliance — only to follow specific court orders.

There's also a penalty for **bad-faith notices**: someone who knowingly submits a false or misleading notice can be liable to the operator for damages, costs, and attorney's fees.

**Everyman summary:**
There's a complaint process. Someone files a sworn complaint, the AG forwards it, and the website has five business days to fix it or push back. Most violations get fixed at this stage without a lawsuit. For really hard technical problems, there's a longer cure period. For really serious violators who are out of state and ignoring the law, courts can — under tight conditions — order ISPs or search engines to block them. The bill goes out of its way not to turn ISPs and search engines into internet police, and people who file fake complaints can be sued.

---

## § 4-88-1314 — Scope limited to adult-side determination; no default minor-side functionality

**Plain-English explanation:**
This section says the program may only be used to determine whether a user is an adult for purposes of unlocking adult use. It may *not* be converted into a system for identifying, classifying, profiling, monitoring, tracking, ranking, restricting, or behaviorally controlling minors.

It bars the Office of State Technology, approved issuers, commercial entities, and others from using the state-certified interface or credentials to create a minor registry, minor profile, minor monitoring system, or minor restriction system. **A "false" response (meaning the user isn't a verified adult) must look the same whether the user is a minor or just an adult who hasn't logged in or activated their credential** — there is no separate "this user is a minor" signal.

The section preserves independent parental controls. Parents, guardians, operating systems, devices, app stores, and services may still offer parental controls, family accounts, content filters, screen-time limits, location-sharing, or other safety features, as long as those features operate independently from this state-certified age-assurance program. A parent can still set up their kid's tablet with restrictions; the bill just says the *state-certified system* isn't the tool that's doing it.

Any expansion of the state-certified system into minor-side monitoring, profiling, restriction, or behavioral control would require a separate act of the General Assembly.

The section also adds **procedural protections** that make it harder for a future legislature to quietly change this scope limit:
- Any bill changing the scope limitation must be a standalone bill, not buried in an omnibus or appropriations bill.
- It must get its own committee hearing in each chamber, with at least 14 days of public notice.
- It must have a recorded roll-call vote on final passage.
- It must include a plainly worded statement on its face identifying it as a bill that changes the scope limitation.
- It must be accompanied by a written impact statement from the Office of State Technology and the Attorney General addressing privacy effects, effects on minors and family autonomy, fiscal effects, and conflicts with federal law.

The section also requests that the House and Senate adopt parallel chamber rules with a point-of-order mechanism enforcing these requirements, and acknowledges that no legislature can fully bind a future legislature — but the procedural cost of evading these rules is real.

**Everyman summary:**
The system is only supposed to prove adulthood. It is not allowed to become a government-backed child-tracking or child-control system. Parents can still use parental controls — that's separate. And if a future legislature ever wants to change this rule, they have to do it as a standalone bill with its own hearing, its own roll-call vote, and a public report on how it would affect kids and families. No quietly slipping it into a budget bill at 2 a.m.

---

# Section 7 — Phased implementation

**Plain-English explanation:**
This section explains how the program starts. The Office of State Technology must first build the technical system, approve issuers, adopt rules, and certify when the state-certified interface is ready.

The Office must publish the certified interface, any certified successor implementation, and the operative compliance date. Businesses do not have to use the state-certified interface before that date. After that date, covered commercial entities must use it unless there is an authorized temporary alternative compliance period.

The operative compliance date must be at least **18 months** after the certified interface and final rules are published. The Office may use pilot participation, staged onboarding, or category-based implementation to roll things out in an orderly way.

**Everyman summary:**
The law does not switch on immediately. The state has to build the system, publish the rules, and give at least 18 months before covered businesses must use it. Realistically, that means roughly two to three years from passage before anything changes for end users.

---

# Section 8 — Initial implementation funding

**Plain-English explanation:**
This section recognizes that the program will need startup money before fees can fully support it. Startup costs may include system design, procurement, integration, retailer onboarding, point-of-sale integration, training, card production, security testing, staffing, technical operations, 24-hour incident response, and public education.

The General Assembly may appropriate money for those startup costs. But the long-term goal remains that the program should be self-funding as much as practicable.

The Office of State Technology must report within 30 days after the operative compliance date and annually after that on revenues, expenses, self-funding status, need for supplemental appropriations, and recommended rule changes.

**Everyman summary:**
The state may need seed money to build the system, but the program is supposed to pay for itself over time, and the legislature gets annual reports to make sure that's actually happening.

---

# Section 9 — Federal law savings and severability

**Plain-English explanation:**
This section tries to protect the bill if parts of it are challenged or struck down. It says the act should not impose liability or obligations inconsistent with Section 230 or other federal law. If a provision is preempted or invalid in one situation, the rest of the act should still apply where possible.

The section also specifically says **the privacy architecture is independent and severable from the underlying age-verification duty.** That means if a court invalidates the core requirement that covered websites perform age verification, the bill's privacy protections, scope limits, anti-gatekeeper rules, fund rules, and remedies are intended to survive for any covered implementation that still chooses or is required elsewhere (by federal law, another state's law, or its own business judgment) to perform age assurance.

It also says if one remedy is invalidated, other remedies should remain valid, and the General Assembly explicitly states it would have enacted the privacy-protection provisions even if the age-verification duty were struck down.

**Everyman summary:**
If a court strikes down the age-verification requirement, the privacy protections still apply. So if Apple or Google ends up doing age verification anyway because California or the federal government requires it, Arkansas's rules about *how* they're allowed to do it — no tracking, no profiling, no selling the data — still bind them when they handle Arkansas users.

---

# Section 10 — Sunset and reauthorization

**Plain-English explanation:**
This section creates a sunset. The key program sections and related rules expire on **June 30 of the fifth full state fiscal year after the operative compliance date**, unless the General Assembly reauthorizes them. Combined with the 18-month build-out period in Section 7, this means the program comes up for review roughly six and a half years after the bill is passed.

At least 18 months before the sunset date, the Office of State Technology, with the Attorney General and Department of Finance and Administration, must report to the General Assembly. The report must cover credential numbers, notices, outages, security incidents, revenues, costs, self-funding status, documented data misuse, relevant federal-law developments, use of successor implementations, whether the boolean-output requirement has been preserved, and recommendations for reauthorization, modification, or repeal.

If the program expires, existing credentials remain valid for their stated duration but are not renewed, and the Office must wind down the program and purge age-assurance data. The privacy protections for data already collected continue as long as that data is retained.

**Everyman summary:**
The system automatically comes up for review after about five years of operation. Lawmakers must take an active vote to keep it. If they don't act, it ends — but the privacy rules still protect any data that was already collected, so nobody can grab the data on the way out the door.

---

## One-sentence "everyman" version of the whole bill

Arkansas would require age checks for certain adult-material access, but instead of letting every website collect IDs and personal data, it would create a narrow state-certified system that only says "yes, this user is 18+" or "no" — while strictly limiting tracking, callbacks, profiling, monopolies, and mission creep, with a built-in five-year review and procedural protections to keep it from quietly expanding.
