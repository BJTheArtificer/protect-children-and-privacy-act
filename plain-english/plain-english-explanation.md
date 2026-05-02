# Plain-English Explanation of the Arkansas Protects Our Children and Our Privacy Online Act

This document explains the bill in everyday language, section by section. It is written for people who want to understand what the bill actually does without wading through the legalese. It is not a legal analysis and should not be cited as one.

---

## The basic idea

This bill tries to solve two problems at the same time.

First, Arkansas wants to keep minors from accessing material that is legally considered harmful to minors online.

Second, Arkansas does not want age verification to become a system where adults must repeatedly hand over IDs, birth dates, names, biometric data, or trackable identity tokens every time they visit a website, install software, use an app, or access lawful adult content.

The bill's solution is to require only a simple yes-or-no answer: **Is this user 18 or older?**

That answer is called a *boolean age response*. It can only be `true` or `false`, or `1` or `0`. It cannot include a name, birth date, ID number, exact age, browsing history, device fingerprint, or reusable identity marker.

The bill creates a state-certified system to deliver that yes-or-no answer in a way that protects children while protecting adult privacy.

---

## Section 1 — Title

The bill's official short name is the **Arkansas Protects Our Children and Our Privacy Online Act**. That's all this section does.

---

## Section 2 — Why the bill exists

This section is the legislative findings — the formal explanation of why Arkansas thinks this law is necessary.

The legislature says Arkansas has two interests:

1. Protecting minors from harmful online material.
2. Protecting adults from being tracked, profiled, or forced into repeated identity checks.

The legislature says many age-verification systems are too invasive because they require repeated submission of government IDs, exact birth dates, exact ages, biometric information, or reusable identity tokens.

The bill says that if age assurance is going to happen at the operating system, device, or app store level, the only information that should leave that system is a simple binary answer about whether the user is 18 or older.

The state also says explicitly that it does not want child-protection laws used as an excuse for broader commercial surveillance.

In short: protect children, but do not build an adult tracking system to do it.

---

## Section 3 — Definitions

This section defines the technical terms used throughout the bill. The most important ones are explained below.

**Adult** is anyone 18 or older. **Minor** is anyone under 18.

**Material harmful to minors** means sexual or pornographic material that, taken as a whole, lacks serious literary, artistic, political, or scientific value for a reasonable seventeen-year-old. The standard tracks longstanding US Supreme Court doctrine going back to *Ginsberg v. New York* (1968).

**Covered implementation** is the central concept of the bill. It means an age-assurance system built into or controlled through an operating system, device, app store, or certified successor local system. Examples include phone operating systems, laptop setup processes, app store gates, device profiles, or similar local systems used to determine whether a user is an adult.

**Age query** is the question asked of a covered implementation: "Is this user 18 or older?" The bill specifies it must be expressed only as `is_18_plus`.

**Boolean age response** is the answer. It can only be `true` or `false`, or `1` or `0`. Nothing else.

**Age-assurance data** means almost any information connected to proving or checking age — birth date, exact age, government ID image or number, device fingerprint, persistent identifier, account identifier, biometric data, location data, browsing data, or records of adult-content access. The bill treats this data as highly sensitive.

**One-time adult setup credential** is a single-use credential an adult receives after proving they are 18 or older. It can be used once during device setup, OS installation, ownership transfer, or repair, and then becomes invalid.

**Adult access permit** is a renewable permit for adults who frequently install, reinstall, test, repair, or administer operating systems — IT workers, students, educators, security researchers, system administrators, software developers, repair technicians, virtualization engineers, and homelab hobbyists. Ordinary adults do not need this permit; only people with repeated technical use cases do.

**Local user context** means a specific user account, profile, session, or login on a device or service. The bill is careful to avoid treating an entire device as adult forever just because one adult once activated a setup credential. Each user account or profile gets its own status.

**Persistent identifier** means any stable identifier that could track a user, device, account, browser, credential, or session across time or services. The bill is strongly aimed at preventing this kind of tracking.

**Consumer virtual computing service** means a remote computing environment marketed and acquired as a turnkey consumer substitute for a personal computing device, like a cloud desktop product sold to ordinary consumers as their main computer. The definition specifically excludes infrastructure-as-a-service, dedicated servers, virtual machines that require the user to install their own operating system, enterprise virtual desktops, developer sandboxes, and cloud storage. The line is between "buy this and use it like a computer" and "rent infrastructure and configure it yourself."

**State-certified interface** is the official Arkansas-approved technical system for asking the age query and receiving the boolean answer.

**Successor local implementation** is a future technical approach that could replace the current operating-system-level model, as long as it preserves the same privacy properties — boolean output, no persistent identifiers leaking to commercial entities, and direct control by the device or service rather than a remote third party.

---

## Section 4 — The actual rule

This is the core of the bill.

**Subsection (a)** says commercial entities must use reasonable age verification before allowing access to a website if a substantial portion of that site contains material harmful to minors. "Substantial portion" means more than one-third (33.33%).

**Subsection (b)** is where the privacy architecture lives. For covered systems, the only lawful age-assurance output for Arkansas compliance is the state-certified `is_18_plus` yes-or-no answer. The covered implementation must return `false` unless a valid credential has been activated for the active local user context. Translation: websites and apps don't get your ID, age, birthday, name, or any reusable adult badge. They get one bit of information — yes or no — and only that.

**Subsection (c)** allows government IDs and other identity verification methods to be used by approved issuers for limited purposes — issuing or renewing credentials, replacing credentials, fraud review, permit administration, or temporary emergency alternatives. But users cannot be forced to submit ID repeatedly to every website if they are using the covered Arkansas system. You show ID once, at the issuer, to get the credential. After that, the issuer is out of the loop.

**Subsection (d)** says that for covered systems, this section overrides any other age-verification method that would require more information. The privacy-preserving binary answer wins.

**Subsection (e)** says businesses must use the state-certified interface after the operative compliance date, with a temporary backup method available if the system goes down.

**Subsection (f)** says that once a business receives a `true` response, it cannot then demand additional age-verification information from the person. The yes-or-no answer is sufficient.

**Subsection (g)** addresses how the bill interacts with multistate technology systems and other jurisdictions:

- The law only regulates the age-assurance output used for Arkansas compliance.
- Companies can still collect or process information needed to comply with another state's law or a lawful contract, as long as that information is not used to satisfy Arkansas's requirements unless Arkansas allows it.
- Companies can choose to apply Arkansas's privacy-preserving requirements to all users, not just Arkansas users. If they do that, they don't have to identify who is in Arkansas, locate users by state, or build special Arkansas routing logic. This is called the *uniform application safe harbor*.
- If a company does want to limit Arkansas's rules to Arkansas users, it can use commercially reasonable methods like device region settings, coarse network-based state inference, or user declarations. It cannot use precise geolocation, persistent location identifiers, or persistent device or account identifiers.
- Information used solely for Arkansas-applicability purposes must be kept only for the session, not tied to a persistent identifier, not sold or shared, and not used for profiling.
- Companies that follow these rules in good faith get the benefit of the doubt.

---

## Section 5 — Who can be sued and what defenses exist

**Subsection (a)(1)** says a commercial entity that knowingly publishes harmful-to-minors material from a website covered by this law is liable if it fails to perform reasonable age verification. This is the core duty.

**Subsection (a)(2)** is the strict liability provision, which has been narrowed in the current draft. Strict liability — meaning liability regardless of intent — applies only to violations of six specific privacy and data-protection rules:

1. The output limitation (sending anything other than a boolean response)
2. The data prohibitions (collecting names, birth dates, biometric data, persistent identifiers, etc.)
3. The secondary-use prohibition (selling, licensing, or repurposing age-assurance data)
4. The segregation requirement (using age-assurance data in advertising or recommendation systems)
5. The issuer callback prohibition (pinging the issuer every time a user does something)
6. The Arkansas-applicability data limits

**Subsection (a)(3)** says that violations of *other* operational, retention, audit, security, or procedural rules in the bill require a showing that the violation was knowing or reckless. This avoids punishing companies for minor procedural mistakes while keeping strict liability for the data-misuse provisions that actually matter.

**Subsection (a)(4)** is the security breach affirmative defense. A company has a defense for unauthorized access to or disclosure of age-assurance data if it can prove that, at the time of the incident, it had a reasonable written information security program based on a recognized framework like the NIST Cybersecurity Framework, ISO/IEC 27001, SOC 2 Type II, or CIS Critical Security Controls; reasonable safeguards, encryption, access controls, vulnerability management, and training; independent assessment at reasonable intervals; timely remediation of known issues; required notices; and good-faith cooperation with authorities.

**Subsection (a)(5)** limits the security defense. It does not protect against intentional misuse of data, knowing retention beyond authorized periods, knowing failure to implement required security controls, non-security violations like illegal telemetry or callbacks, or conduct that independently violates the law.

**Subsection (a)(6)** says the defendant has the burden of proving the security defense by a preponderance of the evidence.

**Subsections (b) and (c)** create private rights of action. Individuals can sue for damages if a minor accessed harmful material due to a violation, or if their age-assurance data was unlawfully retained, sold, licensed, disclosed, or misused.

**Subsection (d)** is the safe harbor for compliant businesses. A commercial entity that uses the state-certified interface in the manner prescribed by rule and relies in good faith on the boolean age response is protected from claims that its age check was insufficient.

**Subsection (e)** says businesses are not liable for failing to use the state-certified interface before it is officially ready and required.

**Subsection (f)** is the outage fallback. If the state-certified system is unavailable, materially degraded, or unable to process requests, the Office of State Technology can authorize a temporary alternative compliance method that is limited in duration, no broader than necessary, as privacy-preserving as practicable, free from secondary use, and automatically expired upon restoration. Companies that comply with the authorized alternative are protected during the outage.

**Subsection (g)** preserves exemptions for bona fide news-gathering organizations covering matters of public concern, for ordinary cloud providers (which are only covered if they offer a consumer virtual computing service used as a covered implementation), and for the existing internet service provider protections.

**Subsection (h)** says ISPs, affiliates, and search engines do not violate the bill merely by providing connection or transmission to content they don't control.

**Subsection (i)** addresses knowingly providing adult credentials to minors. A person cannot knowingly and wittingly furnish, transfer, activate, redeem, or procure an adult credential for a minor who is not the person's child, stepchild, foster child, legal ward, or a minor for whom the person stands in loco parentis. This kinship-caregiver language is intentional — it covers the realities of Arkansas families, including grandparents raising grandchildren, kinship care, and blended families.

The subsection includes:

- A *facially valid identification defense*: a person is not liable if they reasonably relied on what looked like a valid government ID, even if the ID later turned out to be fake.
- Protection for retailers, issuers, and employees who acted in reasonable reliance on apparently valid proof.
- An explicit statement that the subsection does not create liability based solely on loss, theft, or unsolicited resale.

**Subsection (j)** clarifies that private remedies are in addition to public enforcement by the Attorney General, not in place of it.

---

## Section 6 — New code sections added

This section adds eight new sections to Arkansas law, numbered 4-88-1306 through 4-88-1313.

### § 4-88-1306 — What is and isn't covered

The bill applies to personal computing devices (desktops, laptops, tablets, phones, gaming consoles, similar general-purpose devices) and to consumer virtual computing services that act as substitutes for those devices.

It does not apply to ordinary single-purpose or infrastructure devices just because they contain software or connect to the internet. The bill specifically excludes routers, modems, gateways, switches, firewall appliances, thermostats, household appliances, lighting controllers, smart speakers, cameras, doorbells, streaming devices used for media playback, fitness wearables, motor vehicle systems, industrial control systems, medical devices, point-of-sale terminals, printers, smart-home hubs, and similar embedded or single-purpose devices.

The bill says this section must be construed narrowly so it doesn't impede the manufacture, sale, repair, or ordinary use of those devices.

### § 4-88-1307 — One-time adult setup credentials

An adult can prove adulthood once for each operating system installation event through an approved issuer. After proving adulthood, the issuer can issue a one-time adult setup credential redeemable only once.

The credential must be:

- One-time use
- Short-lived before redemption
- Invalid after redemption
- Purged after expiration or redemption within a time set by rule

It can be physical or digital — a printed card, scratch-off code, NFC tag, or one-time digital token. It cannot become a reusable adult badge or persistent identity credential. It cannot create a device-wide presumption that every later user is an adult.

Ordinary adults do not need a permit to get one of these credentials. They can get one at a participating retailer by showing valid government-issued proof of age at or about the time they buy a device, OS installation product, or comparable item. The issuer cannot keep more information than necessary and cannot retain a copy of the ID beyond the brief period needed for issuance and fraud review.

This section also includes the **fee cap**:

- Maximum retail price per credential: $6.00
- Retailer share: at least $1.00
- State share: no more than $5.00, remitted to the Arkansas Child Protection and Online Privacy Fund
- Annual CPI adjustment is allowed within strict limits
- Any increase beyond CPI requires affirmative authorization by the General Assembly
- The retailer share cannot be reduced below $1.00 without legislative action

The fee cap is important because it prevents the Office of State Technology from quietly raising prices over time. Any real increase has to go through the legislature.

### § 4-88-1308 — Single age signal and telemetry limits

This is one of the strongest privacy provisions in the bill.

A covered implementation cannot ask, transmit, store, sell, or rely on any age signal other than the age query and boolean response.

The bill explicitly prohibits collecting, transmitting, storing, retaining, selling, licensing, disclosing, or making secondary use of:

- Legal name
- Exact age
- Date of birth
- Government ID image or number
- Biometric identifiers
- Device fingerprints
- Stable account identifiers
- Stable device identifiers
- Reusable adult tokens
- Persistent cross-site credentials
- Browsing history, search history, or content-viewing history associated with material harmful to minors
- Geolocation data, except very limited coarse use for Arkansas-applicability determinations
- Any age-assurance data beyond what is strictly necessary to issue, redeem, replace, revoke, or validate a credential

Age-assurance data must be kept separate from advertising, recommendation, ranking, personalization, pricing, and profiling systems. It cannot be used to target or differentiate users except to permit or deny age-restricted access.

Audit logging is minimized and cannot include content-specific browsing, viewing, reading, or community-access logs of lawful adult activity.

The section includes a **research and journalism carve-out**: bona fide academic, security, or public-interest researchers, news-gathering organizations, and the state itself can collect, analyze, and publish *aggregate non-identifying* information about how the program operates. This protects academic study, journalism, and government transparency without compromising individual privacy.

### § 4-88-1309 — No issuer callback for ordinary use

After a credential is issued and redeemed, the issuer cannot stay involved in ordinary later use. The issuer cannot be contacted every time a person opens a website, installs software, uses an app, enters an adult community, browses lawful adult material, or uses an unrestricted operating system.

The bill is explicit: **no company and no government office shall operate as a central monitor of lawful adult access.**

Limited callbacks are allowed only for narrow operational purposes — credential replacement, revocation, blacklist administration, fraud prevention, outage recovery, permit renewal, or lawful process.

### § 4-88-1310 — Adult access permits

This section creates the long-term permit track for technical users who repeatedly install, reinstall, or administer operating systems. Eligible categories include IT workers, students, educators, security researchers, system administrators, software developers, repair technicians, virtualization or cloud engineers, and homelab hobbyists.

The permit process must be low-burden. The application can require only:

- Proof that the applicant is an adult
- A statement of intended qualifying use
- A pledge not to knowingly provide the credential to a minor (with the same kinship-caregiver language as Section 5)
- Agreement to report compromise
- Agreement that compromised credentials may be blacklisted, with prompt replacement
- Renewal at intervals set by rule, no more frequent than annually

The fee cap is $25 per renewal term, with CPI indexing only and any larger increase requiring legislative action. The Office of State Technology may establish reduced or waived fees for students, educators, low-income applicants, or other categories where the standard fee would be a barrier.

The permit cannot require a burdensome licensing process, intrusive investigation, or ongoing surveillance.

Ordinary adults do not need this permit; it is only for technical users with repeated installation needs.

### § 4-88-1311 — Administration, enforcement, and rulemaking

This section gives the Office of State Technology authority to administer the technical parts of the program and gives the Attorney General authority to enforce the law through the Deceptive Trade Practices Act.

The rules adopted under this section must address issuer approval and oversight, retailer participation, credential standards, permit administration, blacklist procedures, data minimization, audit limits, persistent identifier prohibitions, technical interface requirements, outage procedures, fraud prevention, security, breach response, replacement procedures, and certification of successor systems.

The Office of State Technology must design the system with redundancy, backup capacity, disaster recovery, security monitoring, and failover testing. The system must be administered so that the temporary alternative compliance method is used only when reasonably necessary, not as a substitute for adequate system capacity.

The section also includes:

- Notice and administrative review for issuer suspension, permit denial or revocation, credential revocation, and blacklist placement.
- Emergency action authority on specific articulable facts, with prompt notice and post-deprivation review.
- Restoration procedures when access is wrongly denied.

The **blacklist** is explicitly limited. It contains only specific invalid credential identifiers — not people. Inclusion on the blacklist does not bar the affected person from getting a replacement credential or applying for a new one. When a credential is invalidated due to compromise, loss, theft, system error, or any circumstance not constituting knowing misuse by the holder, an approved issuer must promptly issue a replacement without making the holder repeat the underlying age proofing process (except for limited reverification when strictly necessary for fraud prevention).

The Office of State Technology must publish technical documentation sufficient for compliance, plus notices of certification, decertification, outage authorization, and restoration. It does not have to publish security-sensitive details that would increase fraud or cybersecurity risk.

The section includes a **coordinated vulnerability disclosure** safe harbor. Security researchers who find and report bugs in the state-certified interface in good faith, following a published policy, are protected from civil and criminal liability — provided they don't exfiltrate more data than necessary, don't exploit the vulnerability for personal gain, don't disclose publicly before the state has had a chance to fix it, and otherwise act in good faith.

### § 4-88-1312 — The fund

This creates the **Arkansas Child Protection and Online Privacy Fund** on the books of the Treasurer of State, the Auditor of State, and the Chief Fiscal Officer.

The fund consists of fees collected under the law (subject to the caps), legislative appropriations, grants, donations, and interest. Money in the fund can only be used for program purposes — administration, issuer oversight, retailer support, credential lifecycle operations, technology systems, hosting, redundancy, security, audits, enforcement, and consumer education.

The program is designed to be self-funding to the maximum extent practicable. The Office of State Technology and the Department of Finance and Administration are directed to implement a narrow, low-burden, fiscally sustainable model.

### § 4-88-1313 — Notice, cure, and remedial procedures

This section creates a notice-and-cure procedure so that alleged violations can be addressed without immediately resorting to litigation.

**Subsection (a)** explains the purpose: a fair, expeditious procedure that gives operators a reasonable chance to fix problems.

**Subsection (b)** defines key terms — a *business day*, a *covered notice* (which must identify the alleged violation specifically, include a sworn good-faith statement, and be signed), and an *operator* (the person with operational control over the website or service).

**Subsection (c)** says any person can submit a covered notice to the Attorney General, who maintains a public submission system, screens notices for sufficiency and good faith, and forwards sufficient notices to the operator within two business days. Notices that are facially insufficient or appear to lack a good-faith basis can be dismissed.

**Subsection (d)** gives the operator five business days to bring the site into compliance, remove or restrict access to the violating material, or submit a counter-notice. An operator that cures within the period is generally not liable for the pre-cure conduct, with three exceptions: knowing or willful violations, cases where a minor actually accessed harmful material because of the violation, or operators who have already cured a substantially similar violation in the past twelve months.

**Subsection (e)** lets operators submit a counter-notice asserting that the original notice is wrong, that the site isn't subject to the law, that the operator is in compliance, or that another good-faith basis exists for declining to cure. Counter-notices must be sworn. The Attorney General must review counter-notices and provide a copy to the original complainant before seeking remedial relief.

**Subsection (f)** is the remedial relief structure. It is split into:

- **Direct remedies**: court orders directing the operator to comply, restraining further violation, or imposing civil penalties under the Deceptive Trade Practices Act.

- **Limited intermediary remedy**: a court can order ISPs, CDNs, search engines, or other intermediaries to block or restrict access only when *all* of the following are true:
  - The operator has been served and failed to cure
  - The operator is beyond the court's jurisdiction or has failed to appear
  - More than two-thirds of the site's material constitutes material harmful to minors
  - The operator has failed to comply with reasonable age verification
  - The court enters specific written findings supported by clear and convincing evidence
  - Notice and an opportunity to be heard have been provided (with narrow exceptions for genuinely exigent circumstances, in which case ex parte orders expire after 14 days unless extended)
  - The order is narrow, limited in duration, and subject to expedited modification or dissolution
  - The order is automatically stayed pending appeal unless the court finds specific harm
  - There is expedited appellate review on the record
  - The court retains continuing jurisdiction

- **Federal-law savings**: a court cannot enter an order that would be inconsistent with Section 230 or other federal law.

- **Intermediary good-faith protection**: intermediaries that comply in good faith are not liable.

- **Construction**: the remedy cannot be used to restrict access to non-violating material, and intermediary remedies are last-resort.

The high two-thirds threshold and clear-and-convincing standard are deliberate. The bill takes the position that compelled intermediary action is constitutionally fragile and should be available only against operators who are clearly out of reach, running clearly violating sites, after clearly failing to cure.

**Subsection (g)** is the extended cure path for systemic technical violations. Operators facing violations that arise from genuine systemic technical defects requiring re-engineering, vendor coordination, or hardware replacement can apply for up to 30 days (extendable once for another 30 days under extraordinary circumstances) to complete remediation, provided they implement reasonable interim mitigation. The Office of State Technology must act on complete applications within three business days. The extended cure does not protect against knowing or willful violations, violations that resulted in actual minor access, or violations involving intentional misuse of age-assurance data. The Office must publish nonconfidential summaries of granted extensions to maintain transparency.

**Subsection (h)** addresses bad-faith notices. People who knowingly submit false, misleading, or bad-faith covered notices are liable to operators for damages, costs, lost revenue, court costs, and attorney's fees. The Attorney General can establish procedures to track and refuse notices from people with patterns of bad-faith submissions.

**Subsection (i)** confirms this section is in addition to other remedies, doesn't relieve operators of liability for knowing violations, allows good-faith cure to be considered as a mitigating factor, doesn't require ISPs or search engines to monitor content, and doesn't impose obligations inconsistent with Section 230.

---

## Section 7 — Phased implementation

The Office of State Technology has to build the system before businesses are required to use it.

OST publishes the certified interface, any certified successor implementations, and an operative compliance date. Businesses are not required to use the interface before that date. After the date, covered businesses must use it (subject to the outage fallback in Section 5(f)).

The operative compliance date must be at least **eighteen months** after publication of the certified interface and final rules. This is a deliberate runway for major technology companies to build to the standard. A shorter runway risks hasty implementations that compromise the privacy architecture.

OST may allow pilots, staged onboarding, or category-based implementation if needed for orderly deployment.

---

## Section 8 — Initial implementation funding

This section authorizes the General Assembly to appropriate startup money for procurement, infrastructure, retailer onboarding, card production, security review, staffing, public education, and other startup costs before fee revenue is sufficient to support the program.

The startup appropriation is intended to facilitate launch. Long-term, the program is supposed to be self-funding through credential fees within the statutory caps.

The section adds an annual reporting requirement: within thirty days of the operative compliance date and every year thereafter, the Office of State Technology must report to the Legislative Council and to the chairs of the State Agencies and Governmental Affairs committees in both chambers on program revenues, expenditures, self-funding status, supplemental appropriation needs, and recommended rule changes.

---

## Section 9 — Federal law savings

The bill is not intended to impose obligations inconsistent with Section 230 or other federal law. If a provision is preempted as applied to a particular person or situation, the provision applies only to the extent not preempted, and the rest of the bill survives. The bill is to be construed to avoid conflict with federal law to the maximum extent consistent with its purposes.

---

## Section 10 — Sunset and reauthorization

The substantive sections of the bill expire on June 30 of the fifth full state fiscal year following the operative compliance date, unless reauthorized by the General Assembly.

Eighteen months before the sunset date, the Office of State Technology must submit a report to the General Assembly addressing:

- How many credentials have been issued, redeemed, replaced, and revoked
- How many notices have been submitted under the notice-and-cure procedure and how they were resolved
- Aggregate non-identifying data on system availability, outages, and use of temporary alternative compliance methods
- Aggregate non-identifying data on security incidents and remediation
- Program revenues, costs, and self-funding status
- Any documented instances of unauthorized retention, sale, licensing, profiling, or secondary use of age-assurance data
- Any developments in federal law (including Section 230 and First Amendment jurisprudence) that materially affect the operation of the law
- The extent to which successor implementations have been used and whether the boolean output requirement has been preserved in practice
- Recommendations for reauthorization, modification, or repeal

If the program sunsets, existing credentials remain valid for their stated duration but are not renewed, and the Office of State Technology winds down the program in an orderly manner, including purging age-assurance data.

The privacy obligations in § 4-88-1308 — data minimization, telemetry limits, secondary-use prohibitions, and segregation from advertising — continue to apply to any data still being held after sunset.

The sunset clause is in the bill because a regulatory program of this scope, building infrastructure that didn't previously exist, deserves a real legislative reexamination on a regular cycle. If the program is working, reauthorization is straightforward. If it isn't, the legislature has a built-in opportunity to fix it or end it.

---

## A short summary of the whole bill

For ordinary adults, the system works like this:

You prove you are an adult once, at a participating retailer, by showing a government ID at the point of sale.

You receive a one-time adult setup credential — a card or code that's been activated for your specific purchase.

You take it home and redeem it once during device or operating system setup.

After that, the credential is dead. The retailer is out of the loop. The state is not tracking what you do online. Your operating system simply knows that an adult-enabled local user context exists on your device.

When a website or app asks whether you're an adult, the operating system answers only one question: yes or no. It does not send your name, age, date of birth, browsing history, or any reusable identity token.

For people who reinstall systems often as part of work, school, research, or a serious hobby, there is a long-term permit track at modest cost.

For everyone, there are real privacy guarantees with real legal teeth, real due process when something goes wrong, and a sunset clause that forces the legislature to revisit the program on a regular schedule.

That's the deal. Protect children. Protect adults. Don't build a surveillance machine.

---

## One-sentence summary

This bill protects Arkansas children online while making sure that the systems built to protect them do not also become the foundation for a permanent identity-tracking apparatus pointed at every lawful adult.
