[VERSION 3 — CHANGES FROM VERSION 2]

This is version 3 of the Arkansas Protects Our Children and Our Privacy Online Act. The following changes were made from version 2:

1. § 4-88-1303(24)(C) — Corrected the LAPS test in the "material harmful to minors" definition from "literary, artistic, political, AND scientific value" to "literary, artistic, political, OR scientific value" to conform to Miller v. California, 413 U.S. 15 (1973).

2. § 4-88-1304(g)(7) and (g)(8) — Added explicit non-extraterritoriality clauses clarifying that Arkansas does not require any covered implementation to apply Arkansas standards to users located in another state, and that the uniform-application safe harbor is permissive only. This addresses dormant Commerce Clause concerns under National Pork Producers Council v. Ross.

3. § 4-88-1307(i)(4)(G) through (J) — Added five-year program review and renewal mechanism for the startup receipt-printed activation share. The startup share sunsets on June 30 of the fifth full state fiscal year following the operative compliance date unless reauthorized by act of the General Assembly. Includes a pre-expiration report requirement and a construction clause preserving the 36-month per-retailer incentive period for retailers already onboarded.

4. § 4-88-1314(g) — Added new procedural protection of scope limitation, including single-subject requirement, separate committee hearing requirement, recorded vote requirement, public statement of effect requirement, fiscal and privacy impact statement requirement, and a companion rules mechanism requesting that each chamber adopt parallel procedural rules and a point of order against non-compliant bills.

5. Section 9 (DO NOT CODIFY) — Expanded from a federal-law savings clause to a federal-law savings AND severability clause, with specific findings that the privacy-protection provisions serve independent and severable purposes from the underlying age-verification duty, so that the privacy architecture survives even if § 4-88-1304(a) or any other age-verification duty is held invalid, unconstitutional, preempted, enjoined, or otherwise unenforceable.

6. § 4-88-1314(d)(1)(A) — Tightened the language prohibiting OST from extending the state-certified interface to minor-side processing. The previous language ("returning a boolean age response indicating that the user is not an adult") could have been read to authorize a separate minor-specific signal. The revised language requires that any false response to a minor be returned "in the same manner as for any other user under § 4-88-1304(b), without distinguishing minors from unauthenticated adults in the response." Identified during full reread of v3.

[END VERSION 3 CHANGELOG]

State of Arkansas
95th General Assembly
Regular Session, 2025

By: ________________________________

For An Act To Be Entitled

AN ACT TO AMEND THE PROTECTION OF MINORS FROM DISTRIBUTION OF
HARMFUL MATERIAL ACT; TO CREATE THE ARKANSAS PROTECTS OUR
CHILDREN AND OUR PRIVACY ONLINE ACT; TO ESTABLISH AN EXCLUSIVE,
PRIVACY-PRESERVING AGE-ASSURANCE COMPLIANCE PATH FOR CERTAIN
OPERATING SYSTEM-LEVEL, DEVICE-LEVEL, APPLICATION-STORE-LEVEL,
AND OTHER LOCALLY SCOPED, STATE-CERTIFIED SUCCESSOR
IMPLEMENTATIONS; TO REQUIRE THAT THE ONLY LAWFUL EXTERNAL
AGE-ASSURANCE RESULT UNDER THAT COMPLIANCE PATH FOR PURPOSES OF
COMPLIANCE WITH ARKANSAS LAW BE A BINARY DETERMINATION OF
WHETHER A USER IS EIGHTEEN (18) YEARS OF AGE OR OLDER; TO
PROHIBIT BROADER TELEMETRY, RETENTION, AND SECONDARY USE OF
AGE-ASSURANCE DATA; TO AUTHORIZE ONE-TIME ADULT SETUP
CREDENTIALS AND ADULT ACCESS PERMITS; TO CREATE THE ARKANSAS
CHILD PROTECTION AND ONLINE PRIVACY FUND; TO ESTABLISH A
PERCENTAGE-BASED PRICING AND RETAILER COMPENSATION STRUCTURE
DESIGNED FOR LONG-TERM DURABILITY, A COST-RECOVERY ANCHOR, A
SUNSET CLAUSE, AND A LIMITED INTERMEDIARY REMEDY SUBJECT TO
STRICT JUDICIAL FINDINGS; TO INCENTIVIZE RETAILER INVESTMENT IN
RECEIPT-PRINTED ACTIVATION INFRASTRUCTURE THROUGH A TIME-LIMITED
STARTUP COMPENSATION TIER; TO REQUIRE MULTIPLE INDEPENDENT
APPROVED ISSUERS SO THAT NO SINGLE ENTITY BECOMES A GATEKEEPER
FOR LAWFUL ADULT COMPUTING; TO LIMIT THE PROGRAM TO ADULT-SIDE
DETERMINATION AND TO PROHIBIT ADMINISTRATIVE EXTENSION OF THE
PROGRAM TO MINOR-SIDE PROFILING, RESTRICTION, OR BEHAVIORAL
CONTROL WITHOUT AFFIRMATIVE LEGISLATIVE AUTHORIZATION; TO
PERMIT DISTRIBUTION OF FUND SURPLUS TO ARKANSAS PUBLIC SCHOOLS
FOR COMPUTER TECHNOLOGY, SCIENCE TECHNOLOGY ENGINEERING AND
MATHEMATICS CURRICULUM, AND CLASSROOM SUPPLIES, COORDINATED
WITH THE DEPARTMENT OF EDUCATION; AND FOR OTHER PURPOSES.

Subtitle

TO PROTECT CHILDREN ONLINE WHILE
PROTECTING THE PRIVACY OF LAWFUL
ADULTS AND CREATING A NARROW,
WORKABLE, PRIVACY-PRESERVING
ARKANSAS AGE-ASSURANCE SYSTEM.

BE IT ENACTED BY THE GENERAL ASSEMBLY OF THE STATE OF ARKANSAS:

SECTION 1. DO NOT CODIFY. Title.

This act shall be known and may be cited as the "Arkansas Protects Our Children and Our Privacy Online Act".

SECTION 2. Arkansas Code § 4-88-1302 is amended to read as follows:

4-88-1302. Legislative findings and intent.

(a) The General Assembly finds that:
(1) The State of Arkansas has a legitimate and compelling interest in protecting minors from access to material harmful to minors;
(2) The State of Arkansas also has a legitimate interest in protecting lawful adult privacy and in preventing age-assurance systems from becoming broad identity-surveillance systems;
(3) Open-ended age-verification models that require repeated submission of identity documents, exact birth dates, exact ages, reusable identity tokens, or persistent cross-service identifiers create avoidable privacy and security risks for lawful adults;
(4) If age assurance is implemented through an operating system-level, device-level, application-store-level, or successor local implementation, the narrowest workable external result is a binary determination of whether the current user is eighteen (18) years of age or older;
(5) For covered implementations under this subchapter, Arkansas should require only a single adulthood signal and should not require age bands, exact-age outputs, date-of-birth outputs, or category-specific age outputs;
(6) Any covered implementation under this subchapter should minimize data collection, prohibit routine issuer callback after issuance or redemption, and avoid central logs of lawful adult access;
(7) Ordinary adult users should be able to obtain a one-time credential at the point of sale of a personal computing device or operating system installation product by presenting facially valid government-issued proof of age, without ongoing surveillance, recurring proofing, or persistent identification;
(8) Technical, professional, educational, security, repair, research, and hobby users who repeatedly install, reinstall, deploy, virtualize, recover, or administer systems should have access to a practical permit process with a long-term credential;
(9) If the state-certified interface is the exclusive ordinary compliance path for a covered implementation, the State of Arkansas should require redundancy, resiliency, failover capacity, and a narrow emergency fallback process so that lawful adult access is not unnecessarily disrupted by outages;
(10) Other states have enacted or proposed operating-system-level or comparable age-assurance laws that may pressure operating system providers, application stores, developers, and other intermediaries to adopt nationwide or multistate age-assurance architectures;
(11) If not constrained by law, those architectures may enable identity linkage, persistent user tracking, and behavioral profiling beyond what is reasonably necessary to determine whether a user is eighteen (18) years of age or older;
(12) The General Assembly rejects the use of child-protection laws as a pretext for broader commercial surveillance, profiling, or identity linkage of lawful users;
(13) The General Assembly further finds that a narrow Arkansas model should protect minors without expanding the power of large technology platforms to monitor, profile, rank, target, or commercially exploit users on the basis of age-assurance signals; and
(14) The components established under this subchapter, including approved issuers, one-time adult setup credentials, adult access permits, outage procedures, and the state-certified interface, are intended to minimize data disclosure, avoid repeated site-by-site proofing, reduce surveillance risk, and provide the narrowest workable means of implementing age assurance for covered implementations under Arkansas law;
(15) Concentration of credential issuance in a single issuer or in a small number of corporately related issuers would create a single point of failure for lawful adult access, would risk the formation of a private gatekeeper for general-purpose computing in this state, and would undermine the privacy and resiliency goals of this subchapter; and
(16) This subchapter regulates the determination of whether a user is an adult for purposes of unlocking unrestricted adult use of a covered implementation, and any extension of state-certified age-assurance infrastructure to monitor, profile, restrict, or behaviorally control minors must be the subject of separate, affirmative legislative authorization rather than administrative expansion of the program established under this subchapter.

(b) It is the intent of the General Assembly to:
(1) Preserve Arkansas's protection of minors from material harmful to minors;
(2) Replace open-ended identity-linked age-assurance methods for covered implementations under this subchapter with a narrow, privacy-preserving Arkansas compliance path that becomes the exclusive lawful external age-assurance output for those covered implementations once the operative compliance date takes effect;
(3) Ensure that one-time proof of adulthood may occur at issuance through an approved issuer without turning every later adult use into a tracked event;
(4) Provide an administrable, self-funding, state-certified implementation path that simplifies compliance for developers and commercial entities while reducing personal data collection;
(5) Require that any outage fallback remain temporary, narrow, and privacy-preserving;
(6) Preserve flexibility to certify only locally scoped, functionally equivalent successor implementations that satisfy the privacy limits established by this subchapter;
(7) Regulate only the age-assurance output used to satisfy Arkansas law for a transaction, session, access request, or local user context associated with a user in this state;
(8) Ensure that credential issuance under this subchapter is supported by multiple independent approved issuers so that no single entity becomes a gatekeeper for lawful adult access to general-purpose computing in this state; and
(9) Limit this subchapter to the determination of adulthood for purposes of unlocking unrestricted adult use of a covered implementation, and to require that any future extension of state-certified age-assurance infrastructure to minor-side functionality be authorized only by separate act of the General Assembly.

SECTION 3. Arkansas Code § 4-88-1303 is amended to read as follows:

4-88-1303. Definitions.

As used in this subchapter:
(1) "Adult" means an individual who is at least eighteen (18) years of age.
(2) "Adult access permit" means a renewable authorization issued under this subchapter to an eligible adult — including without limitation an information-technology worker, a student, an educator, a security researcher, a system administrator, a software developer, a repair technician, a virtualization or cloud engineer, a homelab enthusiast, or another technical user — whose work, education, research, administration, repair, testing, security, or hobby use reasonably requires repeated operating system installation events. An ordinary adult who does not engage in such repeated installation activity does not need an adult access permit and may rely on a one-time adult setup credential issued in accordance with § 4-88-1307.
(3) "Age-assurance data" means any information collected, generated, transmitted, stored, retained, derived, inferred, or associated with an age-assurance event, age query, credential issuance, credential redemption, or credential use, including without limitation a date of birth, exact age, government-issued identification image, government-issued identification number, device fingerprint, persistent identifier, account identifier, biometric identifier, geolocation data, browsing data, or a record of access to material harmful to minors.
(4) "Age query" means a request asking only whether the current user is eighteen (18) years of age or older, expressed solely as is_18_plus.
(5) "Age-credential issuer" means a person, business, office, retailer, or service approved under this subchapter to verify age or permit status and issue a credential under this subchapter.
(6) "Application-store-level implementation" means a credential, interface, service, or technical process that is created, maintained, exposed, or enforced by or through an application store, software distribution service, or comparable software-delivery authority and that is used to present, mediate, or enforce an age query and boolean age response for acquisition, installation, download, or access to software or digital content on a personal computing device or a consumer virtual computing service.
(7) "Approved issuer" means an age-credential issuer approved by the Office of State Technology under rules adopted under this subchapter.
(8) "Arkansas applicability determination" means a determination, made by or on behalf of a covered implementation, of whether the requirements of this subchapter apply to a particular user, transaction, session, access request, or local user context. An Arkansas applicability determination is not required if a covered implementation applies the requirements of this subchapter uniformly to all of its users in accordance with § 4-88-1304(g)(3).
(9) "Blacklist" means the list maintained under this subchapter of specific credential identifiers that have been invalidated. Inclusion of a credential identifier on the blacklist applies only to that specific credential identifier and does not bar the affected person from receiving a replacement credential under § 4-88-1311(h) or from later applying for a new credential under this subchapter.
(10) "Boolean age response" means only:
(A) True or false; or
(B) One (1) or zero (0);
and includes no other information.
(11)(A) "Commercial entity" means a corporation, limited liability company, partnership, limited partnership, sole proprietorship, or other legally recognized entity.
(B) "Commercial entity" includes a third-party vendor.
(12) "Consumer virtual computing service" means a remote computing environment that meets all of the following:
(A) Is marketed to the general consumer public as a substitute for a personal computing device for ordinary personal, family, or household use;
(B) Provides a persistent general-purpose desktop or operating environment that permits operation of multiple third-party applications;
(C) Is acquired through ordinary consumer retail channels, including without limitation a consumer subscription, app store purchase, or comparable consumer-facing transaction; and
(D) Does not require the user to supply, install, configure, or administer an operating system as a condition of ordinary use.
(13) "Consumer virtual computing service" does not include:
(A) A cloud storage, backup, synchronization, or file-hosting service;
(B) A content-delivery, caching, or hosting service;
(C) Infrastructure-as-a-service, dedicated server hosting, bare-metal hosting, or virtual machine services that require the user to supply, install, configure, or administer an operating system;
(D) Enterprise virtual desktop infrastructure, managed workplace service, developer sandbox, technical sandbox, or other service not primarily offered for personal, family, or household use;
(E) A single-purpose streaming, gaming, or media service that does not provide a general-purpose operating environment;
(F) A telecommunications service, broadband internet access service, or internet service provider; or
(G) A service primarily marketed to business, technical, professional, research, scientific, educational, or governmental users.
(14) Construction of "consumer virtual computing service." — In construing the definition of "consumer virtual computing service," the controlling question is whether the service is marketed and acquired as a turnkey consumer substitute for a personal computing device. A service is not a consumer virtual computing service solely because it is technically capable of being used as a desktop substitute, if it is not marketed and sold for that purpose to ordinary consumers.
(15) "Covered implementation" means an operating-system-level implementation, device-level implementation, application-store-level implementation, or certified successor local implementation that is made available in this state for use in determining whether a user is an adult or in transmitting an age-assurance output to a commercial entity.
(16) "Credential" means a code, token, key, record, digital object, physical object, cryptographic material, or other authorization mechanism issued under this subchapter to:
(A) Authorize adult setup for an operating system installation event; or
(B) Support the generation of a boolean age response.
(17) "Device-level implementation" means a credential, interface, service, or technical process that is created, maintained, exposed, or enforced by or through device firmware, a hardware-backed security component, a manufacturer-controlled device service, or a comparable device-resident layer and that is used to determine whether the current user is an adult for a local user context or to answer an age query under this subchapter.
(18) "Digitized identification card" means a data file available on a mobile device that has connectivity to the internet through a state-approved application that allows the mobile device to download the data file from the Office of Driver Services that contains all of the data elements visible on the face and back of a license or identification card and displays the current status of the license or identification card, including without limitation valid, expired, cancelled, suspended, revoked, active, or inactive.
(19) "Distribute" means to issue, sell, give, provide, deliver, transfer, transmit, circulate, or disseminate by any means.
(20) "Internet" means the international computer network of both federal and nonfederal interoperable packet-switched data networks.
(21) "Issuer callback" means a network contact, message, request, verification event, application programming interface call, lookup, ping, handshake, or other communication to an age-credential issuer made after issuance for the purpose of validating, authorizing, recording, monitoring, or learning about later credential use.
(22)(A) "Local user context" means a device-resident or covered virtual-environment-resident operating-system-managed user account, profile, session, secure workspace, or other user separation selected or activated at sign-in, unlock, launch, or session start.
(B) "Local user context" does not include a general online account that is not tied to a specific personal computing device or a specific consumer virtual computing service environment.
(23) "Long-term adult access credential" means a credential issued to a permit holder that authorizes repeated adult setup for a limited renewable term established by rule.
(24) "Material harmful to minors" means:
(A) Any material that the average person, applying contemporary community standards, would find, taking the material as a whole and with respect to minors, is designed to appeal to, or is designed to pander to, prurient interest;
(B) Any of the following material that exploits, is devoted to, or principally consists of descriptions of actual, simulated, or animated displays or depictions of any of the following, in a manner patently offensive with respect to minors:
(i) The nipple of the female breast, pubic hair, anus, vulva, or genitals;
(ii) Touching, caressing, or fondling of nipples, breasts, buttocks, the anus, or genitals; or
(iii) Sexual intercourse, masturbation, sodomy, bestiality, oral copulation, flagellation, excretory functions, exhibitions of a sexual act, and any other sexual act; and
(C) The material taken as a whole lacks serious literary, artistic, political, or scientific value for a reasonable seventeen-year-old.
(25) "Minor" means an individual under eighteen (18) years of age.
(26) "News-gathering organization" means:
(A) An employee of a newspaper, news publication, or news source, printed or published on an online or mobile platform, of current news and public interest, while operating as an employee of a news-gathering organization, who can provide documentation of employment with the newspaper, news publication, or news source; or
(B) An employee of a radio broadcast station, television broadcast station, cable television operator, or wire service while operating as an employee of a news-gathering organization, who can provide documentation of employment.
(27) "One-time adult setup credential" means a one-time-use credential that may be redeemed only once to authorize adult setup for one (1) operating system installation event and that becomes invalid after use or expiration.
(28) "Operating system" means software that manages device hardware or virtualized hardware, provides core system services, controls execution of programs, or enables user interaction with a general-purpose computing device or virtual machine.
(29) "Operating system installation event" means device setup, first-time ownership, ownership transfer, installation, reinstallation, recovery, or repair requiring renewed adult setup authorization.
(30) "Operating-system-level implementation" means a credential, interface, service, or technical process that is:
(A) Created, maintained, exposed, or enforced by or through an operating system, device profile, account authority, or system-level service;
(B) Used to determine whether the current user is an adult; and
(C) Used during an operating system installation event or to answer an age query from an application, website, application store, digital service, or other relying party.
(31) "Ownership transfer" means a sale, gift, assignment, inheritance, donation, resale, or other transfer by which control or possession of a device passes from one person to another.
(32) "Permit holder" means a person holding a valid adult access permit.
(33) "Persistent identifier" means a stable or recurring identifier that may be used to recognize, single out, correlate, track, or link a user, device, account, browser, credential, or service interaction across multiple transactions, sessions, applications, services, websites, devices, or periods of time.
(34) "Personal computing device" means a general-purpose consumer device primarily intended for ordinary personal use by an end user, including without limitation:
(A) A desktop computer;
(B) A laptop computer;
(C) A tablet;
(D) A mobile cellular device or smartphone;
(E) A handheld computing device;
(F) A gaming console; or
(G) Another comparable consumer general-purpose computing device.
(35) "Publish" means to communicate or make information available to another person or entity on a publicly available website.
(36) "Reasonable age verification" means:
(A) For a covered implementation subject to this subchapter, compliance as provided in § 4-88-1304; and
(B) For a noncovered method of compliance under this subchapter, a method reasonably designed to confirm that a person seeking access to published material that may have a substantial portion of material harmful to minors is at least eighteen (18) years of age, including without limitation a method described in § 4-88-1304(c) or another method expressly authorized by law.
(37) "State-certified interface" means the state-approved technical interface, protocol, or implementation approved by the Office of State Technology for an age query and boolean age response under this subchapter.
(38) "Substantial portion" means more than thirty-three and thirty-three hundredths percent (33.33%) of total material on a website that meets the definition of material harmful to minors as defined by this section.
(39) "Successor local implementation" means a device-resident, operating-system-resident, application-store-resident, or covered virtual-environment-resident implementation that:
(A) Is directly controlled by the device, its operating system, its application store, or the provider of a covered consumer virtual computing service;
(B) Provides only the age query and boolean age response authorized by this subchapter for purposes of compliance with Arkansas law;
(C) Does not disclose to a commercial entity a birth date, government-issued identifier, proofing record, or persistent identifier beyond what is expressly authorized by this subchapter; and
(D) Is designated by rule, after written findings of functional equivalence, as substantially similar to an operating-system-level, device-level, or application-store-level implementation expressly described in this subchapter.
(40)(A) "Transactional data" means a sequence of information that documents an exchange, agreement, or transfer between an individual, commercial entity, or a third party used for the purpose of satisfying a request or event.
(B) "Transactional data" includes without limitation records from mortgage, education, and employment entities.

SECTION 4. Arkansas Code § 4-88-1304 is amended to read as follows:

4-88-1304. Reasonable age verification methods — exclusive privacy-preserving compliance path for covered implementations.

(a) A commercial entity shall use reasonable age verification before allowing access to a website that contains a substantial portion of material that is harmful to minors.

(b)(1) For a covered implementation used or relied upon in this state, the exclusive lawful external age-assurance output under this subchapter for purposes of compliance with Arkansas law is an age query and a boolean age response through the state-certified interface, and the covered implementation shall return a false boolean age response unless a valid credential under this subchapter has been activated for the local user context then active on the covered implementation.
(2) For purposes of compliance with this subchapter, a covered implementation:
(A) Shall not provide to a commercial entity an external age-assurance output other than:
(i) is_18_plus; and
(ii) A boolean age response; and
(B) Shall not internally store, retain, process, or use age-assurance data beyond what is strictly necessary to generate the authorized boolean age response, subject to § 4-88-1308.

(c)(1) A digitized identification card, government-issued identification, or a commercially reasonable age-verification method meeting Identity Assurance Level 2 as described in NIST Special Publication 800-63-3, as it existed on January 1, 2025, or a successor standard adopted by rule that provides substantially equivalent proofing assurance, may be used by an approved issuer only for issuance, renewal, replacement, fraud review, blacklist administration, permit administration, or an authorized temporary alternative compliance method under this subchapter.
(2) A method described in subdivision (c)(1) of this section shall not be required as a recurring external submission by a user to each commercial entity seeking to comply through a covered implementation.

(d) This section supersedes any conflicting age-verification method under this subchapter to the extent that the conflicting method requires or permits disclosure, transmission, receipt, storage, retention, sale, licensing, or use of information beyond a binary determination of whether the current user is eighteen (18) years of age or older for a covered implementation.

(e) For a covered implementation, after the operative compliance date established under this act, a commercial entity using or relying upon the covered implementation in this state shall use the state-certified interface except during a temporary alternative compliance period authorized under § 4-88-1305(f). Use of the state-certified interface in compliance with this subchapter satisfies reasonable age verification for that covered implementation.

(f)(1) Compliance through the state-certified interface under this section constitutes compliance with the reasonable age verification duty under this subchapter for the applicable covered implementation.
(2) Except during a temporary alternative compliance period authorized under § 4-88-1305(f), a commercial entity shall not require any additional age-verification information from an individual after receiving a boolean age response of true for the applicable transaction, session, access request, or local user context through the state-certified interface.
(3) A commercial entity shall not condition access through a covered implementation on submission of a date of birth, legal name, government-issued identification image, government-issued identification number, reusable adult token, or other information beyond what is expressly authorized by this subchapter.

(g)(1) Scope of regulation. — This subchapter regulates only the age-assurance output used to satisfy Arkansas law for a transaction, session, access request, or local user context associated with a user in this state.

(2) No conflict with other-jurisdiction or contractual obligations. — Nothing in this subchapter shall be construed to prohibit a person from collecting, maintaining, processing, or transmitting information solely to comply with the law of another jurisdiction or with a lawful contractual obligation, provided that the information is not used to satisfy Arkansas age-assurance requirements except as expressly authorized by this subchapter. A covered implementation that operates a multistate or nationwide age-assurance system does not violate this subchapter solely by collecting information necessary for compliance in another jurisdiction, so long as the Arkansas-facing output is generated in conformity with this subchapter.

(3) Uniform application safe harbor. — A covered implementation that elects to apply the requirements of this subchapter uniformly to all of its users, without performing an Arkansas applicability determination, is in compliance with this subchapter and is not required to:
(A) Identify, locate, or differentiate users by state;
(B) Collect, process, retain, or transmit any signal indicating Arkansas residence, location, or applicability;
(C) Modify a multistate or nationwide age-assurance architecture to introduce Arkansas-specific routing logic; or
(D) Implement an Arkansas-only code path in software, firmware, or service infrastructure.

(4) Optional Arkansas applicability determination. — A covered implementation that elects to perform an Arkansas applicability determination for the purpose of limiting application of this subchapter to users in this state may rely on commercially reasonable methods, including without limitation:
(A) A device-reported region, locale, or language setting;
(B) A coarse network-derived region indicator, including without limitation a country-level or state-level inference derived from a user's apparent network address, that does not include or rely upon a precise geolocation, a persistent location identifier, or a persistent device or account identifier; or
(C) An express user declaration of state.

(5) Limits on data used for an Arkansas applicability determination. — Information collected, generated, or processed solely for an Arkansas applicability determination under subdivision (g)(4) of this section:
(A) Shall be retained only for the duration of the session, transaction, access request, or local user context for which it is used, except that short, reasonable operational caching consistent with ordinary content-delivery, network-routing, or service-availability practices is permitted as established by rule;
(B) Shall not be associated with a persistent identifier;
(C) Shall not be sold, licensed, traded, disclosed, or used for any purpose other than the Arkansas applicability determination itself; and
(D) Shall not be used to construct, augment, or maintain a profile, infer additional location information, or track users over time.

(6) Presumption of validity. — A covered implementation that uses commercially reasonable methods consistent with subdivision (g)(3) or (g)(4) of this section is presumed to satisfy its applicability-determination obligations under this subchapter. Rules adopted under this subchapter may further specify privacy-preserving methods consistent with this subsection but may not authorize methods broader than those permitted under subdivision (g)(4) of this section or limit the safe harbor in subdivision (g)(3) of this section.

(7) No extraterritorial requirement. — Nothing in this subchapter requires a covered implementation to apply the requirements of this subchapter to a user located outside this state, and the uniform application safe harbor under subdivision (g)(3) of this section is permissive only. A covered implementation may, in its sole discretion, elect to apply the requirements of this subchapter:
(A) Only to users in this state, by means of an Arkansas applicability determination under subdivision (g)(4) of this section; or
(B) Uniformly to all of its users, including users located outside this state, by means of the safe harbor under subdivision (g)(3) of this section.
The State of Arkansas does not require, and this subchapter shall not be construed to require, any covered implementation to apply Arkansas standards to users located in another state.

(8) No regulation of out-of-state commerce. — This subchapter regulates only the age-assurance output used to satisfy Arkansas law for a transaction, session, access request, or local user context associated with a user in this state. Any application of this subchapter to a user located outside this state is the result of an independent election by the covered implementation, the law of another jurisdiction, or a contractual obligation between private parties, and is not the result of regulation by the State of Arkansas.

SECTION 5. Arkansas Code § 4-88-1305 is amended to read as follows:

4-88-1305. Liability — safe harbor — limitations.

(a)(1) A commercial entity that knowingly publishes or distributes material that is harmful to minors on the internet from a website that contains a substantial portion of material that is harmful to minors is liable if the commercial entity fails to perform reasonable age verification to verify the age of the individual attempting to access the material.

(2) Strict liability — data misuse and core privacy violations. — A commercial entity, third-party vendor, or approved issuer is strictly liable, regardless of intent or knowledge, for a violation of any of the following:
(A) The output limitations of § 4-88-1304(b) (transmission of any age-assurance output other than a boolean age response);
(B) The data prohibitions of § 4-88-1308(b) (collection, transmission, retention, or use of prohibited age-assurance data);
(C) The secondary-use prohibition of § 4-88-1308(c) (sale, licensing, trading, disclosure, repurposing, profiling, advertising, or other secondary use of age-assurance data);
(D) The segregation requirement of § 4-88-1308(e) (use of age-assurance data in advertising, recommendation, ranking, personalization, pricing, or profiling systems);
(E) The issuer-callback prohibition of § 4-88-1309(a)–(d), other than callbacks falling within the narrow exceptions of § 4-88-1309(e); and
(F) The Arkansas-applicability data limits of § 4-88-1304(g)(5).

(3) Knowing or reckless violations of other operational requirements. — A commercial entity, third-party vendor, or approved issuer is liable for a violation of any other operational, retention, audit, security, or procedural requirement of this subchapter only upon a showing that the violation was committed knowingly or with reckless disregard of the requirement.

(4) Affirmative defense — security breach despite reasonable controls. — It is an affirmative defense to liability under subdivision (a)(2) of this section, as to a violation arising from unauthorized access to, exfiltration of, or disclosure of age-assurance data, that, at the time of the incident, the defendant:
(A) Had implemented and was reasonably maintaining a written information-security program that:
(i) Conformed in substance to a recognized industry framework, including without limitation the National Institute of Standards and Technology Cybersecurity Framework, ISO/IEC 27001, the SOC 2 Type II Trust Services Criteria, the Center for Internet Security Critical Security Controls, or a substantially equivalent standard;
(ii) Included administrative, technical, and physical safeguards reasonably designed to protect the confidentiality, integrity, and availability of age-assurance data;
(iii) Included reasonable access controls, encryption in transit and at rest as appropriate to the data and threat model, vulnerability management, incident response, and personnel-training components; and
(iv) Was independently assessed, audited, or tested at intervals reasonable in light of the size, complexity, and risk profile of the operation;
(B) Had not, at the time of the incident, failed to remediate within a reasonable time a known material vulnerability or a deficiency identified by the most recent independent assessment, audit, or test;
(C) Timely notified the Office of State Technology, the Attorney General, and any affected individuals as required by applicable law and by rule under this subchapter; and
(D) Cooperated in good faith with any incident-response, investigation, or remediation directed by the Office of State Technology, the Attorney General, or another competent authority.

(5) Limits of the affirmative defense. — The affirmative defense provided in subdivision (a)(4) of this section does not apply to:
(A) Liability for sale, licensing, trading, profiling, advertising use, or other intentional or reckless secondary use of age-assurance data;
(B) Liability for knowing retention of age-assurance data beyond the period authorized by this subchapter;
(C) Liability for knowing failure to implement a security control required by rule;
(D) A violation that is not a security incident, including without limitation a violation of the telemetry, callback, segregation, output-limit, or scope provisions of this subchapter; or
(E) Conduct that is itself an independent violation of this subchapter, regardless of whether a security incident also occurred.

(6) Burden of proof. — A defendant asserting the affirmative defense in subdivision (a)(4) of this section bears the burden of proving each element by a preponderance of the evidence.

(b) A commercial entity that violates this subchapter is liable to an individual for damages resulting from a minor accessing the material harmful to minors, including court costs and reasonable attorney's fees as ordered by the court.

(c) A commercial entity, third-party vendor, approved issuer, or other person covered by this subchapter that retains, sells, licenses, discloses, or makes secondary use of prohibited age-assurance data in violation of this subchapter is liable to the individual whose age-assurance data was unlawfully retained, sold, licensed, disclosed, or used for damages resulting from the violation, including court costs and reasonable attorney's fees as ordered by the court.

(d) A commercial entity that uses the state-certified interface in the manner prescribed by rule and relies in good faith on the resulting boolean age response has a safe harbor from liability under this subchapter for the sufficiency of age assurance through that covered implementation.

(e) A commercial entity is not liable under this subchapter for failure to use the state-certified interface before the operative compliance date established under this act.

(f)(1) If the Office of State Technology determines that the state-certified interface is unavailable, materially degraded, or unable to timely process age queries, credential issuance, credential redemption, or credential validation for a covered implementation, the Office of State Technology may authorize by emergency rule or written order a temporary alternative compliance method.
(2) A temporary alternative compliance method authorized under this subsection shall:
(A) Be limited in duration;
(B) Be no broader than reasonably necessary to address the outage or degradation;
(C) Use the least data-invasive practicable method;
(D) Prohibit sale, licensing, disclosure except as required by law, profiling, advertising use, or other secondary use of age-assurance data;
(E) Expire automatically upon restoration of the state-certified interface or on the expiration date stated in the emergency rule or written order, whichever occurs first; and
(F) Be treated as reasonable age verification for the limited duration of the authorization.
(3) A commercial entity, third-party vendor, approved issuer, or other covered person that complies in good faith with a temporary alternative compliance method authorized under this subsection has a safe harbor from liability under this subchapter for the duration of the authorization.

(g) This section does not:
(1) Apply to a bona fide news-gathering organization acting in the ordinary course of news reporting, commentary, documentary presentation, or coverage of a matter of public concern, if any material harmful to minors made available by the organization is incidental to that reporting, commentary, documentary presentation, or coverage and is not offered, promoted, or organized principally for sexual arousal or entertainment;
(2) Apply to a cloud service provider unless the provider offers a consumer virtual computing service that is used or relied upon as a covered implementation under this subchapter; or
(3) Affect the application of subsection (h) of this section.

(h) An internet service provider, or any affiliate or subsidiary of an internet service provider, or a search engine shall not violate this subchapter solely by providing access or connection to or from a website or other information or content on the internet or a facility, system, or network that is not under the internet service provider's control, including without limitation transmission, downloading, intermediate storage, access software, or another service that provides access or connectivity, to the extent the internet service provider is not responsible for the creation of the content or the communication that constitutes material harmful to minors.

(i)(1) A person shall not knowingly and wittingly furnish, transfer, activate, redeem, or procure for use by a minor a one-time adult setup credential, adult access permit, or long-term adult access credential where the minor is not the person's child, stepchild, foster child, legal ward, or a minor for whom the person stands in loco parentis. For purposes of this subdivision, a person acts "knowingly and wittingly" only if the person:
(A) Has actual knowledge that the recipient is a minor and is not the person's child, stepchild, foster child, legal ward, or a minor for whom the person stands in loco parentis; or
(B) Consciously avoids knowledge of the recipient's status as a minor under circumstances making such knowledge highly probable.

(2) A person who violates subdivision (i)(1) of this section is liable to the parent or legal guardian of the minor for actual damages resulting from the violation, court costs, and reasonable attorney's fees as ordered by the court.

(3) Affirmative defense — facially valid identification. — It is a complete defense to liability under this subsection that the defendant furnished, transferred, activated, redeemed, or procured the credential in reasonable reliance on identification or other proof of adulthood that:
(A) Appeared on its face to be valid government-issued identification or another form of proof of adulthood expressly authorized by rule;
(B) Was not, on its face, expired, altered, defaced, or otherwise apparently irregular at the time of the transaction; and
(C) Was reviewed by the defendant or the defendant's employee or agent in a manner consistent with reasonable retail or issuance practice.

(4) A retailer, issuer, or employee acting in reasonable reliance on facially valid proof of adulthood is not liable under this subsection, even if the proof later proves to be counterfeit, fraudulent, altered, borrowed, or stolen, unless the defendant had actual knowledge or consciously avoided knowledge of the falsity at the time of the transaction.

(5) This subsection does not create liability based solely on loss, theft, unsolicited resale, or another transfer that was not a knowing and witting furnishing, transfer, activation, redemption, or procurement for the minor's use.

(j)(1) The private remedies created by this section are cumulative and are in addition to any public enforcement authority of the Attorney General under this subchapter or under the Deceptive Trade Practices Act, § 4-88-101 et seq.
(2) Nothing in this subchapter shall be construed to limit, displace, or preclude public enforcement by the Attorney General unless expressly stated.

SECTION 6. Arkansas Code Title 4, Chapter 88, Subchapter 13, is amended to add additional sections to read as follows:

4-88-1306. Scope of covered implementations.

(a) Sections 4-88-1306 — 4-88-1314 apply only to a covered implementation used or relied upon for a user in this state.

(b) Sections 4-88-1306 — 4-88-1314 apply only with respect to:
(1) A personal computing device; or
(2) A consumer virtual computing service used as a substitute for a personal computing device.

(c) Sections 4-88-1306 — 4-88-1314 do not apply to a device, system, product, or service that is not primarily offered as a general-purpose personal computing environment for ordinary end-user use, including without limitation a router, modem, gateway, switch, firewall appliance, thermostat, household appliance, lighting controller, smart speaker, camera, doorbell, streaming device primarily used for media playback, wearable device primarily used for fitness, health, or accessory purposes, motor vehicle system, industrial control system, medical device, point-of-sale terminal, printer, smart-home hub, home-automation controller, or a comparable embedded, appliance-like, single-purpose, or infrastructure device.

(d) A device, system, product, or service is not subject to §§ 4-88-1306 — 4-88-1314 solely because it:
(1) Contains software;
(2) Connects to the internet;
(3) Uses an operating system;
(4) Includes a touchscreen, microphone, camera, or application interface; or
(5) Permits limited user configuration.

(e) In construing this section, the controlling question is whether the device or service is primarily offered as a general-purpose personal computing environment for ordinary end-user use.

(f) Sections 4-88-1306 — 4-88-1314 shall be construed narrowly so that they do not impede the manufacture, sale, transfer, repair, configuration, or ordinary use of embedded, household, network, appliance, infrastructure, or single-purpose devices that do not present a substantial minor-user access risk comparable to a personal computing device.

(g) A successor local implementation may be certified under this subchapter only if it satisfies § 4-88-1303(39) and the written findings required by rule under § 4-88-1311.

4-88-1307. One-time adult setup credentials.

(a) An adult may prove adulthood once for each operating system installation event through an approved issuer.

(b) Upon proof of adulthood for an operating system installation event, an approved issuer may issue one (1) one-time adult setup credential redeemable only once to authorize adult setup only for the local user context then active for that operating system installation event.

(c) A one-time adult setup credential shall be:
(1) One-time use;
(2) Short-lived before redemption;
(3) Invalid after redemption; and
(4) Purged after expiration or redemption within the time established by rule.

(d) A one-time adult setup credential may be delivered in physical or digital form, including without limitation a printed activation card, a scratch-off code, an NFC tag, or a one-time digital setup token.

(e) A one-time adult setup credential shall not become a reusable adult badge, named account token, or persistent identity credential.

(f) A one-time adult setup credential shall not create a device-wide presumption that every later user of the device is an adult.

(g) Rules adopted under this subchapter shall require credential formats and redemption procedures to be scoped to a local user context and to expire without creating a persistent cross-context identifier.

(h)(1) An ordinary adult is not required to obtain an adult access permit to obtain a one-time adult setup credential.
(2) An ordinary adult may obtain a one-time adult setup credential at an approved issuer, including without limitation a participating retailer, by presenting facially valid government-issued proof of age at or about the time of purchase of:
(A) A personal computing device;
(B) An operating system installation medium, activation card, or product key; or
(C) Another comparable product or service that requires adult setup under this subchapter.
(3) An approved issuer shall not require, retain, or transmit information about the adult beyond confirmation of facial validity of proof of age and any minimum information necessary for fraud prevention or credential production as established by rule, and shall not retain a copy of the proof of age beyond the time strictly necessary for issuance and any limited fraud-review period established by rule.

(i) Pricing and retailer compensation.

(1) Cost-recovery purpose. — The retail sale price of a one-time adult setup credential issued under this section is intended to support the self-funding administration of the program established under this subchapter and is not to be used as a general revenue source. The retail sale price set by rule under this subsection shall be reasonably calibrated to the actual administrative cost of the program, including without limitation credential production, retailer compensation, state-certified interface operation, fraud prevention, replacement handling, and a reasonable reserve consistent with § 4-88-1312.

(2) Maximum retail sale price.
(A) The Office of State Technology shall establish by rule the maximum retail sale price of a one-time adult setup credential, calibrated to the cost-recovery purpose of subdivision (i)(1) of this section.
(B) The Office of State Technology may adjust the maximum retail sale price annually by an amount not to exceed the percentage change in the Consumer Price Index for All Urban Consumers, U.S. City Average, All Items, as published by the Bureau of Labor Statistics of the United States Department of Labor, for the preceding calendar year.
(C) The Office of State Technology shall reduce the maximum retail sale price as necessary to maintain consistency with the cost-recovery purpose of subdivision (i)(1) of this section, including without limitation when the cumulative balance of the Arkansas Child Protection and Online Privacy Fund exceeds the reasonable reserve and reasonably anticipated permissible distributions contemplated by subdivisions (i)(5) and (i)(6) of this section.
(D) An increase in the maximum retail sale price by an amount greater than the index adjustment authorized under subdivision (i)(2)(B) of this section requires affirmative authorization by act of the General Assembly.
(E) Recommendation as of enactment. — As of enactment of this subchapter, the General Assembly recommends an initial maximum retail sale price of approximately six dollars ($6.00) per credential, comparable in magnitude to ordinary Arkansas administrative or licensing fees, subject to the cost-recovery analysis required under this subsection.

(3) Retailer compensation — three-tier structure. — The Office of State Technology shall establish by rule the retailer compensation share for each of the following categories of issuance, expressed as a percentage of the retail sale price:
(A) Physical card issuance — issuance of a pre-manufactured one-time adult setup credential through retail rack distribution or comparable physical distribution;
(B) Sustained receipt-printed activation — issuance of a credential generated and printed at the point of sale by a participating retailer that has invested in the point-of-sale integration infrastructure necessary for receipt-printed activation, after expiration of the startup incentive period under subdivision (i)(4) of this section; and
(C) Startup receipt-printed activation — issuance described in subdivision (i)(3)(B) of this section, during the startup incentive period under subdivision (i)(4) of this section.

(4) Relative weighting and sunset.
(A) The retailer compensation share for sustained receipt-printed activation shall exceed the share for physical card issuance, reflecting the additional point-of-sale processing, integration maintenance, and inventory burden the retailer assumes by issuing a credential without state-supplied physical card stock.
(B) The retailer compensation share for startup receipt-printed activation shall exceed the share for sustained receipt-printed activation, reflecting a time-limited incentive intended to support retailer recovery of the initial investment required to deploy point-of-sale receipt-activation integration.
(C) The startup receipt-printed activation share shall apply to a particular retailer for a startup incentive period of thirty-six (36) months commencing on the date that retailer's receipt-printed activation integration is certified as operational by the Office of State Technology. Upon expiration of the startup incentive period, the sustained receipt-printed activation share applies to that retailer prospectively.
(D) The startup incentive period shall apply separately to each retailer.
(E) Each retailer compensation share established under subdivision (i)(3) of this section shall be reasonably calibrated to the work, investment, and operational burden the retailer bears for the corresponding category of issuance, consistent with the cost-recovery purpose of subdivision (i)(1) of this section.
(F) Recommendation as of enactment. — As of enactment of this subchapter, the General Assembly recommends initial retailer compensation shares set by rule at approximately one-sixth (16⅔%) of the retail sale price for physical card issuance, one-quarter (25%) of the retail sale price for sustained receipt-printed activation, and one-third (33⅓%) of the retail sale price for startup receipt-printed activation. These recommendations are not binding on the Office of State Technology and are intended only to inform initial rulemaking.
(G) Five-year program review and renewal. — The startup receipt-printed activation share authorized under subdivision (i)(3)(C) of this section shall expire on June 30 of the fifth full state fiscal year following the operative compliance date published under Section 7 of the act of which this section is a part, unless the General Assembly affirmatively reauthorizes the startup receipt-printed activation share by act of the General Assembly before that date.
(H) Effect of expiration. — Upon expiration under subdivision (i)(4)(G) of this section, the sustained receipt-printed activation share under subdivision (i)(3)(B) of this section applies to all receipt-printed activation thereafter, and the startup share shall not apply to any retailer regardless of the date of certification of that retailer's receipt-printed activation integration.
(I) Pre-expiration report. — Not later than eighteen (18) months before expiration of the startup receipt-printed activation share under subdivision (i)(4)(G) of this section, the Office of State Technology shall submit to the General Assembly a report addressing:
(i) The number of retailers that have deployed receipt-printed activation integration;
(ii) The proportion of credentials issued through receipt-printed activation as compared to physical card issuance;
(iii) The fund balance and surplus distribution history during the startup incentive period;
(iv) Whether continuation of the startup share is necessary to support continued retailer onboarding or whether the sustained share is sufficient; and
(v) Recommendations for reauthorization, modification, or expiration.
(J) Construction. — Nothing in subdivisions (i)(4)(G) through (I) of this section affects the duration of the thirty-six-month startup incentive period applicable to a particular retailer under subdivision (i)(4)(C) of this section, except that no retailer shall receive the startup share for any issuance occurring after the expiration date established under subdivision (i)(4)(G) of this section.

(5) Reasonable reserve. — The Office of State Technology, in coordination with the Department of Finance and Administration, shall maintain in the Arkansas Child Protection and Online Privacy Fund a reasonable operating reserve sufficient to ensure continuity of the program, including without limitation reserve to cover anticipated annual operating cost, contingency for outage response and temporary alternative compliance methods under § 4-88-1305(f), replacement and fraud handling, and orderly wind-down obligations under Section 10 of the act of which this section is a part. The Office of State Technology shall determine the reasonable reserve amount by rule and shall periodically review the reserve target.

(6) Surplus distribution.
(A) Definition. — For purposes of this subdivision, "surplus" means the balance of the Arkansas Child Protection and Online Privacy Fund in excess of the reasonable reserve maintained under subdivision (i)(5) of this section.
(B) Permissible uses of surplus. — Surplus, when present, may be applied in the following order of priority:
(i) Such additional reserve as the Office of State Technology determines necessary to address anticipated future costs, including without limitation upcoming infrastructure refresh, security upgrades, expanded demand, or anticipated wind-down expenses;
(ii) Distribution to Arkansas public school districts and Arkansas public charter schools, distributed consistent with the school funding formulas administered by the Department of Education or comparable per-pupil or per-school distribution mechanism established by rule in coordination with the Department of Education, for the following purposes:
(a) Acquisition, refresh, repair, or maintenance of computing technology used in school computer labs and classroom instruction;
(b) Support of science, technology, engineering, and mathematics curriculum, including without limitation acquisition of curriculum materials, software, and instructional equipment, with particular attention to building foundational computer science and STEM capacity in kindergarten through grade six (K-6);
(c) Acquisition of basic classroom supplies, including without limitation paper, writing implements, and other consumable instructional materials; and
(d) Other lawful educational purposes consistent with this subdivision as the Office of State Technology may identify by rule in coordination with the Department of Education;
(iii) Such other lawful uses consistent with this subchapter as the General Assembly may by appropriation direct.
(C) Surplus is not a permanent revenue stream. — The use of surplus under this subdivision is contingent on the existence of surplus in any given period. Surplus distribution under subdivision (i)(6)(B) of this section shall not give rise to any expectation, entitlement, or appropriation right on the part of any school district, charter school, or other recipient. The primary obligation of the Office of State Technology remains administering the program established under this subchapter consistent with the cost-recovery purpose of subdivision (i)(1) of this section.
(D) Persistent surplus triggers price review. — If surplus is present in the fund for three (3) consecutive fiscal years in amounts that exceed reasonable reserve and reasonably anticipated permissible distributions, the Office of State Technology shall review the maximum retail sale price established under subdivision (i)(2) of this section and shall reduce the price as necessary to align program revenue with the cost-recovery purpose of subdivision (i)(1) of this section, unless the Office of State Technology makes written findings that the surplus is non-recurring or is needed for specific anticipated future costs.
(E) Annual accountability reporting. — In each annual report required under Section 8(c) of the act of which this section is a part, the Office of State Technology shall report:
(i) The cumulative balance of the Arkansas Child Protection and Online Privacy Fund;
(ii) The reasonable reserve target then in effect;
(iii) Any surplus present and the disposition of any surplus, including the amount and recipient categories of any distribution under subdivision (i)(6)(B)(ii) of this section;
(iv) Any written findings made under subdivision (i)(6)(D) of this section in lieu of a price reduction; and
(v) Any recommended adjustments to the reasonable reserve target, the maximum retail sale price, or the retailer compensation shares.

(7) State remittance. — The portion of the retail sale price not retained by the issuing retailer under subdivision (i)(3) of this section shall be remitted to the Arkansas Child Protection and Online Privacy Fund established under § 4-88-1312, on a schedule and through procedures established by rule.

(8) Construction.
(A) Nothing in this subsection authorizes a retailer to charge a consumer more than the maximum retail sale price established under subdivision (i)(2) of this section, or to impose a separate fee, surcharge, markup, or other additional charge on a consumer beyond the retail sale price.
(B) Nothing in this subsection authorizes the use of credential pricing under this subchapter as a general revenue source for the State of Arkansas.
(C) Nothing in this subsection creates a property right in any retailer compensation share established by rule, and the Office of State Technology may adjust shares prospectively through ordinary rulemaking consistent with this subsection. A material reduction in any retailer compensation share shall be preceded by reasonable advance notice to affected approved issuers consistent with rules adopted under § 4-88-1311.

4-88-1308. Single age signal and telemetry limits.

(a) A covered implementation shall not ask, require, transmit, receive, store, sell, license, disclose, or rely upon any age signal under this subchapter other than:
(1) An age query; and
(2) A boolean age response.

(b) A covered implementation shall not require, transmit, receive, store, retain, sell, license, disclose, or make secondary use of:
(1) A legal name;
(2) An exact age;
(3) A date of birth;
(4) A government-issued identification image;
(5) A government-issued identification number;
(6) A biometric identifier;
(7) A device fingerprint;
(8) A stable account identifier;
(9) A stable device identifier;
(10) A reusable adult token;
(11) A persistent cross-site credential;
(12) Browsing history, search history, or content-viewing history associated with material harmful to minors;
(13) Geolocation data, except that coarse, non-persistent location indicators may be used solely as authorized by § 4-88-1304(g)(4) for an Arkansas applicability determination, and except as strictly necessary for fraud prevention, security, or lawful process as provided by rule; or
(14) Age-assurance data beyond what is strictly necessary to issue, redeem, replace, revoke, or validate a credential under this subchapter.

(c) A person subject to this subchapter shall not sell, license, trade, disclose, repurpose, profile, advertise with, or otherwise make secondary use of age-assurance data collected under this subchapter.

(d) Audit logging under this subchapter shall be minimized by rule and shall not include content-specific browsing, viewing, reading, or community-access logs of lawful adult activity.

(e) Age-assurance data collected or processed under this subchapter shall be segregated from advertising, recommendation, ranking, personalization, pricing, and profiling systems and shall not be used to target, classify, or differentiate lawful users except to permit or deny age-restricted access as expressly authorized by this subchapter.

(f) Retention of any age-assurance data that is lawfully collected under this subchapter shall be limited to the shortest period reasonably necessary for issuance, redemption, replacement, revocation, fraud review, security, auditing, lawful process, or an authorized temporary alternative compliance method, and information collected for an Arkansas applicability determination shall be retained only as permitted under § 4-88-1304(g)(5).

(g) Research and journalism. — Nothing in this section prohibits:
(1) A bona fide academic, security, or public-interest researcher from collecting, analyzing, or publishing aggregate, non-identifying information about the operation of the program established under this subchapter, provided that the researcher does not collect, retain, or publish age-assurance data identifying specific individuals;
(2) A bona fide news-gathering organization from collecting, analyzing, or publishing information about the operation of the program established under this subchapter, subject to the same limitation; or
(3) The Office of State Technology, the Attorney General, or a legislative body from collecting and publishing aggregate program data consistent with this subchapter.

4-88-1309. Issuer callback prohibited for ordinary later use.

(a) After issuance of a credential under this subchapter, and after redemption if redemption is required, an approved issuer shall not remain in the loop for ordinary later use.

(b) An approved issuer shall not be contacted each time a person:
(1) Opens a site;
(2) Installs software;
(3) Uses an app;
(4) Enters an adult community;
(5) Browses lawful adult material; or
(6) Uses an unrestricted operating system.

(c) A credential governed by this subchapter shall be used locally to the maximum extent reasonably practicable and without routine issuer callback.

(d) No company and no government office shall operate as a central monitor of lawful adult access under this subchapter.

(e) This section does not prohibit a narrowly tailored issuer callback strictly necessary for:
(1) Replacement;
(2) Revocation;
(3) Blacklist administration as defined in § 4-88-1303(9);
(4) Fraud prevention;
(5) Outage recovery;
(6) Permit renewal; or
(7) Lawful process.

4-88-1310. Adult access permits.

(a) A person whose work, education, research, administration, repair, testing, security, or hobby use reasonably requires repeated operating system installation events may apply for an adult access permit. The category of persons eligible for an adult access permit includes without limitation an information-technology worker, a student, an educator, a security researcher, a system administrator, a software developer, a repair technician, a virtualization or cloud engineer, a homelab enthusiast, and another technical user who frequently spins up, deploys, virtualizes, recovers, reinstalls, or administers operating system installations as a routine part of work, study, research, or hobby activity.

(b) The permit process shall be low-burden and practical.

(c) An application for an adult access permit shall require only:
(1) Proof that the applicant is an adult;
(2) A statement of intended qualifying use;
(3) A pledge not to knowingly furnish, transfer, activate, or redeem the credential for use by a minor who is not the applicant's child, stepchild, foster child, legal ward, or a minor for whom the applicant stands in loco parentis;
(4) Agreement to report compromise;
(5) Agreement that a compromised credential identifier may be placed on the blacklist as defined in § 4-88-1303(9), with prompt issuance of a replacement credential under § 4-88-1311(h); and
(6) Renewal at the interval established by rule, which shall not be more frequent than annual renewal.

(d) Fee.
(1) The fee for an adult access permit shall be set by rule and shall not exceed twenty-five dollars ($25.00) per renewal term.
(2) The Office of State Technology may adjust the maximum permit fee under subdivision (d)(1) of this section annually, by an amount not to exceed the percentage change in the Consumer Price Index for All Urban Consumers, U.S. City Average, All Items, as published by the Bureau of Labor Statistics of the United States Department of Labor, for the preceding calendar year.
(3) An increase in the maximum permit fee by an amount greater than the index adjustment authorized under subdivision (d)(2) of this section requires affirmative authorization by act of the General Assembly.
(4) The Office of State Technology may, by rule, establish reduced or waived permit fees for students, educators, low-income applicants, or other categories of applicants for whom the standard fee would be a barrier to lawful access.

(e) An adult access permit shall not require a burdensome licensing process, intrusive investigation, or ongoing surveillance.

(f) A permit holder may receive a long-term adult access credential, subject to rules adopted under this subchapter.

(g) An ordinary adult who does not engage in repeated operating system installation events as described in subsection (a) of this section is not required to obtain an adult access permit and may rely on a one-time adult setup credential issued under § 4-88-1307.

4-88-1311. Administration, enforcement, and rulemaking.

(a) The Office of State Technology of the Department of Shared Administrative Services shall administer §§ 4-88-1304 and 4-88-1306 — 4-88-1314 and may promulgate rules necessary to implement those sections.

(b) The Attorney General shall enforce this subchapter and may bring an action under the Deceptive Trade Practices Act, § 4-88-101 et seq., for a violation of §§ 4-88-1304 and 4-88-1306 — 4-88-1314.

(c) The Office of State Technology may coordinate with the Department of Finance and Administration for physical issuance support, permit administration support, retailer participation, inventory planning, remittance procedures, or other ministerial functions authorized by rule.

(d) Rules adopted under this section shall include without limitation:
(1) Standards for approval, suspension, and removal of issuers, including notice and review procedures;
(2) Minimum issuer eligibility requirements, including data-minimization compliance, information-security controls, breach-reporting capability, financial responsibility sufficient to perform issuer duties, and prohibitions on using age-assurance data for data-brokerage, advertising, or unrelated commercial profiling;
(3) Standards for retailer participation;
(4) Standards for one-time adult setup credentials, including the point-of-sale issuance flow under § 4-88-1307(h);
(5) Standards for permit issuance, renewal, revocation, and replacement;
(6) Standards for compromise reporting and blacklist administration as defined in § 4-88-1303(9);
(7) Data-minimization requirements;
(8) Audit logging limits;
(9) Standards prohibiting persistent identity linkage and routine issuer callbacks except as strictly necessary under § 4-88-1309;
(10) Technical interface requirements for the state-certified interface;
(11) Availability, resiliency, outage, fallback, restoration, and notice procedures;
(12) Fraud-prevention procedures;
(13) Security requirements for credential issuance, redemption, replacement, revocation, storage, and transmission;
(14) Incident response, breach response, and notice procedures consistent with applicable law;
(15) Procedures for expedited replacement or restoration of access after compromise, error, outage, or wrongful denial;
(16) Written findings, certification standards, and public designation procedures for any successor local implementation; and
(17) Privacy-preserving methods for an Arkansas applicability determination consistent with § 4-88-1304(g).

(e) A covered person that uses the state-certified interface in the manner prescribed by rule is presumed to be in compliance with §§ 4-88-1304 and 4-88-1306 — 4-88-1314.

(f)(1) The Office of State Technology shall design, procure, implement, and maintain the state-certified interface and related credential systems with reasonable redundancy, resiliency, failover, backup capacity, and recovery capability sufficient to minimize outages and material degradation.
(2) The redundancy and resiliency required under this subsection shall include without limitation:
(A) Geographic or infrastructure redundancy sufficient to avoid a single point of failure;
(B) Backup processing and storage capability;
(C) Disaster recovery and restoration procedures;
(D) Capacity planning for peak demand;
(E) Security monitoring and incident response procedures;
(F) Testing of failover and recovery capability at intervals established by rule; and
(G) Logging and audit procedures sufficient to verify availability and restoration performance, but not lawful adult browsing, viewing, reading, or community-access activity.
(3) The Office of State Technology shall administer the system so that a temporary alternative compliance method under § 4-88-1305(f) is used only when reasonably necessary and not as a substitute for adequate system capacity, maintenance, or redundancy.
(4) Rules adopted under this section shall establish minimum availability, resiliency, recovery, and restoration standards for the state-certified interface and related systems.

(g)(1) Rules adopted under this section shall provide notice and an opportunity for administrative review for:
(A) Issuer suspension or removal;
(B) Permit denial or revocation;
(C) Long-term credential revocation; and
(D) Placement of a credential identifier on the blacklist or another action that materially affects lawful adult access.
(2) The Office of State Technology may take immediate temporary emergency action upon specific and articulable facts showing fraud, compromise, misuse, or a security threat.
(3) If emergency action is taken under subdivision (g)(2) of this section, the affected person shall receive prompt written notice of the grounds for the action and an opportunity for expedited post-deprivation review.
(4) Rules shall include prompt restoration, replacement, or correction procedures when lawful adult access is wrongly denied, blocked, or affected by inclusion of a credential identifier on the blacklist through error, mistaken identity, compromise, or system failure.

(h)(1) The blacklist maintained under this subchapter consists only of specific credential identifiers that have been invalidated and does not bar the affected person from receiving a replacement credential or from later applying for a new credential.
(2) When a long-term adult access credential held by a permit holder is invalidated and the credential identifier is placed on the blacklist due to compromise, loss, theft, suspected fraud not committed by the holder, system error, or another circumstance not constituting knowing misuse by the holder, an approved issuer shall promptly issue a replacement long-term adult access credential to the holder without requiring the holder to repeat the underlying age-proofing process, except to the extent that limited reverification is strictly necessary for fraud prevention as established by rule.
(3) When a one-time adult setup credential is invalidated and its identifier is placed on the blacklist before redemption due to compromise, loss, theft, suspected fraud not committed by the original purchaser, system error, or another circumstance not constituting knowing misuse by the purchaser, an approved issuer shall promptly issue a replacement one-time adult setup credential to the purchaser upon reasonable proof of original purchase, without requiring the purchaser to repeat the underlying age-proofing process, except to the extent that limited reverification is strictly necessary for fraud prevention as established by rule.
(4) Rules adopted under this section shall:
(A) Establish standards for placement of a credential identifier on the blacklist, including specific and articulable grounds;
(B) Establish a maximum duration for blacklist placement of a particular credential identifier in the absence of renewed grounds;
(C) Establish a procedure by which an affected person may petition for removal of a credential identifier from the blacklist or for correction of an erroneous placement; and
(D) Ensure that placement of a credential identifier on the blacklist is not used as a means of identifying, tracking, profiling, or restricting the affected person beyond invalidation of that specific credential identifier.

(i) The Office of State Technology shall publish nonconfidential technical documentation sufficient to enable compliance with the state-certified interface and shall publish notice of certification, decertification, outage authorization, and restoration under this subchapter, except that the Office of State Technology is not required to publicly disclose security-sensitive details that would materially increase fraud or cybersecurity risk.

(j) Coordinated vulnerability disclosure. — The Office of State Technology shall establish and publish a coordinated vulnerability disclosure policy for the state-certified interface and related systems. A person who, in good faith, identifies and reports a security vulnerability in accordance with the published policy shall not be subject to civil or criminal liability under state law for the act of identifying or reporting the vulnerability, provided that the person:
(1) Did not exfiltrate data beyond what was reasonably necessary to demonstrate the vulnerability;
(2) Did not exploit the vulnerability for personal gain or to cause harm;
(3) Did not publicly disclose the vulnerability before the Office of State Technology had a reasonable opportunity to remediate it, consistent with the published policy; and
(4) Otherwise acted in good faith and in accordance with the published policy.

(k) Multiple independent approved issuers required.
(1) Purpose. — The General Assembly finds that concentration of credential issuance in a single approved issuer or a small number of corporately related approved issuers would create a single point of failure for lawful adult access, would risk the formation of a private gatekeeper for general-purpose computing in this state, and would undermine the privacy and resiliency goals of this subchapter. The Office of State Technology shall administer this subchapter so that credential issuance is supported by multiple independent approved issuers.
(2) Minimum number of approved issuers. — Beginning on the operative compliance date and at all times thereafter, the Office of State Technology shall maintain a roster of not fewer than three (3) approved issuers in active operation in this state, drawn from at least two (2) of the following categories:
(A) Brick-and-mortar retail issuers, including without limitation participating consumer electronics retailers, general-merchandise retailers, and gift-card-rail retailers;
(B) Online or mail-order issuers operating under rules adopted under this subchapter;
(C) Government office issuers, including without limitation a state revenue office, a county clerk, or another government office authorized by rule; and
(D) Any other category of issuer authorized by rule.
(3) Limit on common control. — No single corporate parent, controlled subsidiary group, or other commonly controlled enterprise shall control more than one (1) approved issuer slot for purposes of subdivision (k)(2) of this section. For purposes of this subdivision, "common control" includes ownership of more than fifty percent (50%) of the voting equity of an approved issuer, the right to appoint a majority of the directors or managers of an approved issuer, or any other arrangement that confers substantial control over the operation of an approved issuer.
(4) Geographic distribution. — The Office of State Technology shall, by rule, establish standards designed to ensure that approved issuers are distributed across this state in a manner that provides reasonable physical access to credential issuance for residents of urban, suburban, and rural areas. The Office of State Technology shall periodically review issuer distribution and may approve additional issuers, subject to the eligibility requirements of this subchapter, to address coverage gaps.
(5) Anti-gatekeeper requirements. — Rules adopted under this section shall include without limitation:
(A) Standards for issuer eligibility designed to permit qualified entrants and to avoid unnecessary barriers to entry;
(B) Prohibitions on exclusive-dealing arrangements, exclusive-territory arrangements, or other contractual arrangements that would prevent the approval or operation of additional issuers;
(C) Standards prohibiting an approved issuer from conditioning issuance of a credential on the purchase of unrelated goods or services from that issuer or an affiliated entity, except for the purchase of a personal computing device, operating system installation product, or comparable product or service for which adult setup is required under this subchapter;
(D) Standards prohibiting an approved issuer from charging the consumer more than the maximum retail sale price authorized under § 4-88-1307(i); and
(E) Procedures for the Office of State Technology to monitor issuer market concentration, identify anticompetitive conduct, and refer matters to the Attorney General for action under the Deceptive Trade Practices Act, § 4-88-101 et seq., or other applicable law.
(6) Inability to maintain minimum. — If, despite good-faith effort, the Office of State Technology is temporarily unable to maintain the minimum number of approved issuers required under subdivision (k)(2) of this section, the Office of State Technology shall:
(A) Promptly publish notice of the deficiency, the steps being taken to address it, and the expected timeline for restoration;
(B) Take all reasonable measures to approve additional eligible issuers as expeditiously as practicable; and
(C) Authorize, if necessary, a temporary alternative compliance method under § 4-88-1305(f) to ensure that lawful adult access is not unduly disrupted during the deficiency.
(7) Continuing application. — The requirements of this subsection are continuing requirements and apply at all times during which the program established under this subchapter is in operation.

4-88-1312. Arkansas Child Protection and Online Privacy Fund.

(a) The Arkansas Child Protection and Online Privacy Fund is created on the books of the Treasurer of State, the Auditor of State, and the Chief Fiscal Officer of the State.

(b) The fund shall consist of:
(1) Fees collected under this subchapter;
(2) Credential issuance, replacement, activation, or permit fees established by rule, subject to the fee caps in §§ 4-88-1307(i) and 4-88-1310(d);
(3) Monies appropriated by the General Assembly;
(4) Grants, donations, and other lawful funds; and
(5) Interest earned on fund balances.

(c) Monies in the fund shall be used only for:
(1) Administration of this subchapter;
(2) Issuer approval and oversight;
(3) Retailer and issuer participation support;
(4) Credential production, activation, redemption, replacement, revocation, and blacklist administration;
(5) Information technology systems, hosting, redundancy, maintenance, fraud prevention, security, and audit functions;
(6) Enforcement;
(7) Consumer education;
(8) Surplus distribution authorized under § 4-88-1307(i)(6), only to the extent surplus is present after maintenance of the reasonable reserve under § 4-88-1307(i)(5); and
(9) Other lawful implementation costs under this subchapter.

(d) The program created under this subchapter shall be administered as a self-funding program to the maximum extent practicable.

(e) In adopting rules and administering the program, the Office of State Technology and the Department of Finance and Administration shall strive to implement a narrow, low-burden, and fiscally sustainable model, including without limitation:
(1) Use of one-time adult setup credentials suitable for retail or equivalent distribution;
(2) Incentives sufficient to support voluntary retailer or issuer participation;
(3) State remittance structures sufficient to support ongoing administration, redundancy, fraud prevention, and replacement handling;
(4) Inventory and production planning reasonably tied to expected demand and contingency needs;
(5) Modest staffing levels or contracted support reasonably suited to a narrow program scope;
(6) Moderate startup and integration planning;
(7) Narrow technical implementation that avoids unnecessary feature expansion or overengineering; and
(8) Financial and technical practices designed to maintain long-term self-sufficiency to the maximum extent practicable.

4-88-1313. Notice, cure, and remedial procedures.

(a) Purpose. — This section establishes a notice-and-cure procedure for addressing alleged violations of this subchapter. The purpose of this section is to provide a fair, expeditious, and procedurally regular method for addressing alleged violations without requiring litigation in every instance and to ensure that an operator of a website or other publishing service has a reasonable opportunity to come into compliance before any remedial measure is sought.

(b) Definitions. — As used in this section:
(1) "Business day" means a day other than Saturday, Sunday, or a state legal holiday.
(2) "Covered notice" means a written notice that:
(A) Identifies the website, page, or other publishing location alleged to be in violation, with specificity sufficient to permit location of the material;
(B) Identifies the specific provision of this subchapter alleged to have been violated;
(C) Includes a statement, made under penalty of perjury, that the complainant has a good-faith belief that the use of the website, page, or service is in violation of this subchapter and that the information in the notice is accurate;
(D) Includes the name and contact information of the complainant or the complainant's authorized representative; and
(E) Is signed physically or electronically by the complainant or authorized representative.
(3) "Operator" means a person with operational control over the website, page, or other publishing location alleged to be in violation, including without limitation a commercial entity or third-party vendor.

(c) Submission of a covered notice.
(1) Any person may submit a covered notice to the Office of the Attorney General alleging a violation of this subchapter.
(2) The Office of the Attorney General shall:
(A) Maintain a publicly accessible mechanism for submission of covered notices, including without limitation an online form;
(B) Conduct a preliminary review of each covered notice for facial sufficiency and apparent good-faith basis; and
(C) Forward each facially sufficient covered notice to the operator of the alleged violation as promptly as practicable, but in no event later than two (2) business days after receipt.
(3) A covered notice that is facially insufficient or that appears, on preliminary review, to lack a good-faith basis may be dismissed by the Office of the Attorney General with written notice to the complainant.

(d) Cure period.
(1) Upon delivery of a forwarded covered notice to the operator, the operator shall have five (5) business days to:
(A) Bring the website, page, or service into compliance with this subchapter;
(B) Remove or restrict access to the allegedly violating material in a manner sufficient to remedy the alleged violation; or
(C) Submit a written counter-notice as provided in subsection (e) of this section.
(2) An operator that, within the cure period, brings the website, page, or service into compliance or removes or restricts access to the allegedly violating material is not subject to remedial action under this section based on the alleged violation identified in the covered notice, and shall not be liable under this subchapter for the conduct alleged in the covered notice as to the period before the cure was effected, unless:
(A) The operator engaged in a knowing or willful violation;
(B) A minor in fact accessed material harmful to minors as a result of the violation; or
(C) The operator has previously cured a substantially similar violation under this section within the preceding twelve (12) months.

(e) Counter-notice.
(1) An operator may submit to the Office of the Attorney General, within the cure period, a written counter-notice asserting that:
(A) The covered notice is materially inaccurate or incomplete;
(B) The website, page, or service is not subject to this subchapter;
(C) The operator is in compliance with this subchapter; or
(D) Another good-faith basis exists for declining to cure.
(2) A counter-notice shall be made under penalty of perjury and shall include sufficient supporting information to permit reasonable evaluation by the Office of the Attorney General.
(3) Upon receipt of a timely counter-notice, the Office of the Attorney General shall:
(A) Provide a copy to the original complainant; and
(B) Conduct further review and shall not seek remedial action under subsection (f) of this section without first providing the operator a reasonable opportunity to be heard.

(f) Remedial relief.
(1) Direct remedies. — If, after the expiration of the cure period and any further review under subsection (e) of this section, the Attorney General has reasonable cause to believe that the operator remains in violation of this subchapter, the Attorney General may apply to a court of competent jurisdiction for an order:
(A) Directing the operator to come into compliance with this subchapter;
(B) Restraining further violation of this subchapter; or
(C) Imposing civil penalties as authorized by the Deceptive Trade Practices Act, § 4-88-101 et seq.

(2) Limited intermediary remedy. — A court shall not order an internet service provider, content delivery network, search engine, or other intermediary to block, restrict, deindex, or otherwise restrain access from this state to a website, page, or other publishing location except upon all of the following:
(A) The operator of the website, page, or other publishing location:
(i) Has been served with a covered notice and has failed to cure within the period authorized by this section;
(ii) Is beyond the personal jurisdiction of the court for purposes of direct enforcement, or has failed to appear after reasonable service;
(iii) Operates a website, page, or service for which more than two-thirds (2/3) of the total material constitutes material harmful to minors as defined by this subchapter; and
(iv) Has failed to comply with the reasonable age verification duty under this subchapter;
(B) The court enters specific written findings, supported by clear and convincing evidence, as to each of the elements in subdivision (f)(2)(A) of this section;
(C) Notice and an opportunity to be heard have been provided to the operator and to any intermediary against whom relief is sought, except where the court finds, on specific and articulable facts, that exigent circumstances of imminent and substantial harm to minors require ex parte relief, in which case any ex parte order shall expire automatically not later than fourteen (14) days after entry unless extended after notice and hearing;
(D) The order is limited to the specific website, page, or publishing location identified in the application and is no broader than reasonably necessary;
(E) The order is limited in duration and is subject to expedited modification or dissolution upon a showing that the operator has come into compliance, that the factual predicate has changed, or that the order is no longer necessary;
(F) The order is automatically stayed pending appeal upon timely notice of appeal by the operator or any affected intermediary, unless the court enters specific written findings that the stay would result in imminent and substantial harm to minors;
(G) The order provides for expedited appellate review on the record; and
(H) The court retains continuing jurisdiction to modify or dissolve the order on motion of the operator, an affected intermediary, or any person whose lawful access to non-violating material is impaired by the order.

(3) Federal-law savings. — A court shall not enter an order under subdivision (f)(2) of this section if entry of the order would be inconsistent with 47 U.S.C. § 230 or other applicable federal law.

(4) Intermediary good-faith compliance. — An intermediary that complies in good faith with a court order under this subsection is not liable under this subchapter or under state law for compliance with the order.

(5) Construction. — An order under this subsection shall not be used to restrict access to material that is not material harmful to minors or to material the publication of which does not itself violate this subchapter. The remedies under subdivision (f)(2) of this section are last-resort remedies and shall not be sought where direct enforcement against the operator is reasonably available.

(g) Extended cure for systemic technical violations.
(1) Availability. — A person otherwise eligible for cure under subsection (d) of this section may apply to the Office of State Technology for an extended cure period of up to thirty (30) days from the date of acquisition of actual knowledge if:
(A) The violation arises from a systemic technical defect in hardware, firmware, software, or system architecture;
(B) Full remediation cannot reasonably be completed within the five-business-day cure window because remediation requires re-engineering, vendor coordination, software release cycles, hardware replacement, or comparable structural changes; and
(C) The applicant has implemented or is implementing reasonable interim mitigation under subdivision (g)(3) of this section.

(2) Application requirements. — An application for an extended cure period shall be submitted to the Office of State Technology no later than three (3) business days after acquisition of actual knowledge of the violation and shall include:
(A) A description of the violation with reasonable specificity;
(B) A technical explanation of why remediation cannot reasonably be completed within the five-business-day cure window;
(C) A proposed remediation plan with milestones and a target completion date not later than thirty (30) days after acquisition of actual knowledge;
(D) A description of the interim mitigation measures the applicant has implemented or will implement under subdivision (g)(3) of this section; and
(E) A point of contact responsible for the remediation.

(3) Mandatory interim mitigation. — During the extended cure period, the applicant shall implement reasonable measures to limit ongoing exposure of age-assurance data and ongoing risk to lawful adult privacy, including without limitation, as applicable to the violation:
(A) Suspension of the affected feature, function, or data flow;
(B) Routing of affected operations through a temporary alternative that is in compliance with this subchapter;
(C) Manual review or human-in-the-loop processing of affected transactions;
(D) Quarantine, segregation, or accelerated purging of affected age-assurance data;
(E) Suspension of any logging, telemetry, or transmission implicated in the violation; or
(F) Other reasonable measures established by rule.

(4) Decision. — The Office of State Technology shall act on a complete application within three (3) business days of receipt and may:
(A) Grant the application as submitted;
(B) Grant the application with modifications to the proposed remediation plan or interim mitigation; or
(C) Deny the application, with written reasons.
If the Office of State Technology does not act on a complete application within three (3) business days, the application is deemed provisionally granted on the terms proposed by the applicant, subject to later modification by the Office of State Technology upon written findings.

(5) Effect of grant. — During an extended cure period granted under this subsection, the applicant is not liable under § 4-88-1305(a)(2) for the violation, provided that the applicant is in substantial compliance with the remediation plan and the interim mitigation requirements. Liability under § 4-88-1305(a)(1), § 4-88-1305(c), and subdivisions (d)(2)(A), (d)(2)(B), and (d)(2)(C) of this section is not affected.

(6) Limits. — An extended cure period:
(A) Shall not exceed thirty (30) days from the date of acquisition of actual knowledge, except that the Office of State Technology may grant a single additional extension of up to thirty (30) days upon a showing of extraordinary circumstances and continued substantial compliance with the remediation plan and interim mitigation;
(B) Is not available for a person who has received an extended cure period for a substantially similar violation within the preceding twelve (12) months;
(C) Is not available for a knowing or willful violation, a violation that resulted in a minor in fact accessing material harmful to minors, or a violation involving sale, licensing, trading, profiling, advertising use, intentional secondary use, knowing unlawful retention, routine issuer callback, unlawful output expansion, or other intentional or reckless misuse of age-assurance data; and
(D) May be revoked by the Office of State Technology upon written findings that the applicant has materially failed to comply with the remediation plan or interim mitigation requirements, in which case liability under § 4-88-1305(a)(2) attaches as of the date of revocation.

(7) Public notice. — The Office of State Technology shall publish a nonconfidential summary of each granted extended cure period, including the nature of the violation category and the duration of the extension, but shall not publish information that would compromise security or identify specific affected individuals. This publication requirement is intended to maintain transparency regarding use of the extended cure mechanism.

(8) Appeal. — A denial or revocation under this subsection is subject to administrative review under rules adopted by the Office of State Technology consistent with § 4-88-1311(g).

(h) Bad-faith notices.
(1) A complainant who knowingly submits a materially false, misleading, or bad-faith covered notice is liable to the operator for damages resulting from the false notice, including without limitation costs of compliance, lost revenue resulting from improper restriction of access, court costs, and reasonable attorney's fees as ordered by the court.
(2) The Office of the Attorney General may, by rule, establish a procedure for tracking, identifying, and refusing to forward covered notices from a person who has demonstrated a pattern of bad-faith submissions.

(i) Limitations and other rights.
(1) This section is in addition to, and does not limit, any other enforcement authority of the Attorney General, any private right of action created by this subchapter, or any other remedy available under law.
(2) Compliance with this section does not relieve an operator of liability for a knowing or willful violation of this subchapter or for damages resulting from a minor's actual access to material harmful to minors.
(3) An operator's good-faith cure under this section may be considered by a court as a mitigating factor in any subsequent enforcement action.
(4) Nothing in this section shall be construed to require an internet service provider, search engine, or other intermediary to monitor user content, search results, or third-party communications, or to evaluate compliance of third parties with this subchapter, except in compliance with a specific court order under this section.
(5) Nothing in this section shall be construed to impose liability or compliance obligations inconsistent with 47 U.S.C. § 230 or other applicable federal law.

4-88-1314. Scope limited to adult-side determination — no default minor-side functionality.

(a) Purpose. — The General Assembly finds that the privacy and child-protection goals of this subchapter are best served by strictly limiting the program established under this subchapter to its core function: determining whether a user is an adult for purposes of unlocking unrestricted adult use of a covered implementation. Any extension of state-certified age-assurance infrastructure to monitor, profile, restrict, or behaviorally control minors raises distinct constitutional, family-autonomy, and child-welfare considerations that must be the subject of separate, affirmative legislative authorization rather than administrative expansion of this program.

(b) Scope limitation.
(1) The program established under this subchapter, the state-certified interface, and any credential issued under this subchapter shall be used solely to determine whether a user is an adult for purposes of unlocking unrestricted adult use of a covered implementation and to generate the boolean age response authorized by § 4-88-1304(b).
(2) Neither the Office of State Technology, an approved issuer, a commercial entity using the state-certified interface, nor any other person shall use the program established under this subchapter, the state-certified interface, or any credential issued under this subchapter to:
(A) Identify, classify, profile, monitor, track, or rank a user known or believed to be a minor;
(B) Apply content restrictions, filtering, application restrictions, behavioral controls, screen-time controls, location-tracking, communication-monitoring, or other minor-directed functionality through the state-certified interface or related infrastructure;
(C) Maintain a registry, list, or database of minor users derived from age-assurance data or from boolean age responses indicating that a user is not an adult; or
(D) Transmit, sell, license, disclose, or make secondary use of any signal indicating that a particular user is not an adult, except as strictly necessary to permit or deny age-restricted access in accordance with this subchapter.

(c) Permissive parental controls preserved.
(1) Nothing in this section prohibits a parent, legal guardian, or other person standing in loco parentis from configuring, on a device or service the parent or guardian controls, parental controls, content filtering, application restrictions, screen-time limits, location-sharing, or other minor-directed safety features that operate independently of the program established under this subchapter.
(2) Nothing in this section prohibits an operating system, device, application store, or other service from offering parental control features, family-account features, or comparable minor-protection tools that operate independently of the state-certified interface and that do not rely on age-assurance data collected or generated under this subchapter.
(3) Nothing in this section prohibits an operating system, device, application store, or other service from honoring a request from a parent or legal guardian to enable, configure, or modify parental control features, provided that the request is parent-initiated and the resulting features operate independently of the state-certified interface and the credential system established under this subchapter.

(d) Affirmative legislative authorization required for minor-side extension.
(1) Notwithstanding any other provision of law, the Office of State Technology shall not adopt rules, certify implementations, approve issuers, or otherwise administer the program established under this subchapter in a manner that:
(A) Extends the state-certified interface to handle, transmit, store, or process information about a user known or believed to be a minor for any purpose other than returning a false boolean age response in the same manner as for any other user under § 4-88-1304(b), without distinguishing minors from unauthenticated adults in the response;
(B) Requires, authorizes, or facilitates the construction of a minor-side identification system, profiling system, restriction system, or behavioral monitoring system; or
(C) Permits a successor local implementation to be certified under this subchapter if that implementation includes minor-side identification, profiling, restriction, or behavioral monitoring functionality.
(2) Any extension of state-certified age-assurance infrastructure to functionality described in subdivision (d)(1) of this section requires affirmative authorization by act of the General Assembly.

(e) Construction.
(1) This section shall be construed broadly in favor of limiting the program established under this subchapter to adult-side determination and against extension of the program to minor-side functionality.
(2) This section does not limit the protection of minors from material harmful to minors under § 4-88-1304(a) or other provisions of this subchapter, the Arkansas Code, or applicable federal law.
(3) This section does not authorize, require, or limit any minor-directed functionality offered by an operating system, device, application store, or other service that operates independently of the state-certified interface and the credential system established under this subchapter.

(f) Reporting. — In each annual report required under Section 8(c) of the act of which this section is a part, and in each pre-sunset report required under Section 10(b) of that act, the Office of State Technology shall affirmatively certify that the program established under this subchapter has been operated in compliance with this section, or shall identify any departure from this section and the basis on which the departure was made.

(g) Procedural protection of scope limitation.
(1) Findings. — The General Assembly finds that:
(A) The scope limitation established by this section is essential to the privacy, child-welfare, and family-autonomy purposes of this subchapter;
(B) Expansion of the program established under this subchapter to minor-side identification, profiling, restriction, or behavioral control would constitute a fundamental change in the program that warrants full deliberative consideration by the General Assembly, separate from other legislative business; and
(C) Procedural protections that raise the deliberative cost of modifying the scope limitation are appropriate to ensure that any such modification reflects considered judgment of the General Assembly rather than incidental legislative action.
(2) Single-subject requirement. — A bill that would amend, repeal, weaken, or otherwise modify the scope limitation established by this section, or that would extend the program established under this subchapter to minor-side identification, profiling, restriction, or behavioral control, shall be filed as a standalone bill addressing that subject and shall not be included as a provision within an omnibus bill, an appropriations bill, a budget reconciliation measure, a revenue bill, or any other bill addressing additional subjects.
(3) Committee hearing required. — A bill described in subdivision (g)(2) of this section shall receive a separate committee hearing in each chamber, with public notice of not less than fourteen (14) days, before the bill may be reported out of committee.
(4) Recorded vote required. — A vote on final passage of a bill described in subdivision (g)(2) of this section shall be a recorded roll-call vote in each chamber.
(5) Public statement of effect required. — A bill described in subdivision (g)(2) of this section shall include a plainly worded statement, prominently displayed in the bill, identifying the bill as one that modifies or extends the scope limitation established by this section and summarizing the effect of the modification or extension.
(6) Fiscal and privacy impact statement. — A bill described in subdivision (g)(2) of this section shall be accompanied by a written impact statement, prepared by the Office of State Technology in consultation with the Attorney General, addressing:
(A) The anticipated effect of the bill on the privacy of lawful adult users of covered implementations;
(B) The anticipated effect of the bill on minors and on family-autonomy interests;
(C) The anticipated fiscal effect on the Arkansas Child Protection and Online Privacy Fund and on program administration; and
(D) Any anticipated conflict with applicable federal law, including without limitation 47 U.S.C. § 230 and the First Amendment to the United States Constitution.
(7) Companion rules mechanism. — The General Assembly requests that the House of Representatives and the Senate each adopt, as part of the rules of the chamber, procedural rules implementing the requirements of subdivisions (g)(2) through (g)(6) of this section, including without limitation a point of order that may be raised on the floor of the chamber against a bill that does not comply with those subdivisions. The procedural requirements of this subsection apply regardless of whether the chambers adopt the requested rules.
(8) Construction. — This subsection establishes procedural expectations for the orderly consideration of changes to the scope limitation established by this section. Nothing in this subsection purports to limit the constitutional authority of a future General Assembly to enact legislation by the procedures established by the Arkansas Constitution. The procedural requirements of this subsection are intended to ensure that any modification of the scope limitation receives full deliberative consideration consistent with the importance of the subject matter.
(9) Severability. — If any provision of this subsection is held invalid or unenforceable as a limitation on future legislative action, the remaining provisions of this section, including the substantive scope limitation in subsections (a) through (f), shall remain in full force and effect.

SECTION 7. DO NOT CODIFY. Phased implementation.

(a) During the first phase of implementation, the Office of State Technology shall develop the technical system, approve issuers, adopt rules, and certify when the state-certified interface is available for use.

(b) The Office of State Technology shall publish the certified interface, any certified successor local implementation, and an operative compliance date.

(c) A commercial entity is not required to use the state-certified interface before the operative compliance date.

(d) After the operative compliance date, a commercial entity using or relying upon a covered implementation in this state shall use the state-certified interface and shall be entitled to the safe harbor provided under this act, except during a temporary alternative compliance period authorized under § 4-88-1305(f). Compliance through the state-certified interface supersedes any other reasonable age verification duty under this subchapter for that covered implementation.

(e) The Office of State Technology may provide by rule for pilot participation, staged onboarding, or category-based implementation if necessary for orderly deployment.

(f) The operative compliance date published under subsection (b) of this section shall be not less than eighteen (18) months after publication of the certified interface and the final rules required to implement this subchapter.

SECTION 8. DO NOT CODIFY. Initial implementation funding.

(a) The General Assembly recognizes that establishment of the program created under this act will require initial appropriations for:
(1) Procurement, design, build, and integration of the state-certified interface and credential lifecycle systems, with reasonable redundancy and resiliency consistent with § 4-88-1311(f);
(2) Retailer onboarding, including point-of-sale integration with major retail chains and regional retailers, training, and ongoing technical support;
(3) Initial card production and inventory;
(4) Security review, penetration testing, and independent assessment;
(5) Staffing, contracted technical operations, and 24-hour incident-response capacity;
(6) Public education and consumer information; and
(7) Other lawful startup costs.

(b) The General Assembly may appropriate monies for the purposes described in subsection (a) of this section before fee revenues are sufficient to support the program. Initial appropriations are intended to facilitate startup and do not alter the requirement that the program be administered as a self-funding program to the maximum extent practicable under § 4-88-1312.

(c) Within thirty (30) days after the operative compliance date, and annually thereafter, the Office of State Technology shall report to the Legislative Council and to the chairs of the House and Senate Committees on State Agencies and Governmental Affairs on:
(1) Total program revenues and expenditures;
(2) Self-funding status;
(3) Any anticipated need for supplemental appropriations; and
(4) Any rule changes recommended to maintain self-funding status consistent with the fee caps in §§ 4-88-1307(i) and 4-88-1310(d).

SECTION 9. DO NOT CODIFY. Federal law savings and severability.

(a) Nothing in this act is intended to impose liability or compliance obligations inconsistent with 47 U.S.C. § 230 or other applicable federal law.

(b) If a provision of this act is preempted in whole or in part by federal law as applied to a particular person or circumstance, the provision shall be construed to apply only to the extent not preempted, and the remaining provisions of this act and their application to other persons or circumstances shall not be affected.

(c) This act shall be construed to avoid conflict with applicable federal law to the maximum extent consistent with its purposes.

(d) Severability — general. — If any provision of this act, or the application of any provision to any person or circumstance, is held invalid, unconstitutional, preempted, or otherwise unenforceable, the invalidity shall not affect other provisions or applications of this act that can be given effect without the invalid provision or application, and to this end the provisions of this act are severable.

(e) Severability — privacy architecture preserved. — The General Assembly specifically finds that the privacy-protection provisions of this act, including without limitation §§ 4-88-1304(b), 4-88-1304(g), 4-88-1306 through 4-88-1314, and the corresponding liability, scope-limitation, anti-gatekeeper, anti-extension, and fund-administration provisions, serve independent and severable purposes from the underlying age-verification duty in § 4-88-1304(a). If § 4-88-1304(a) or any other provision establishing or modifying an age-verification duty is held invalid, unconstitutional, preempted, enjoined, or otherwise unenforceable, in whole or in part, the privacy-protection, scope-limitation, anti-gatekeeper, anti-extension, fund-administration, and remedial provisions identified in this subsection shall remain in full force and effect and shall continue to apply to any covered implementation that elects, or is otherwise required by federal law, the law of another jurisdiction, or independent business judgment, to perform age assurance with respect to users in this state.

(f) Severability of remedies. — If a particular remedy authorized by this act, including without limitation the limited intermediary remedy under § 4-88-1313(f)(2), is held invalid, unconstitutional, preempted, or otherwise unenforceable, the invalidity shall not affect the validity of any other remedy authorized by this act.

(g) The General Assembly would have enacted each provision of this act independently of every other provision and would have enacted the privacy-protection, scope-limitation, anti-gatekeeper, anti-extension, fund-administration, and remedial provisions of this act regardless of whether any age-verification duty under this subchapter were held invalid, unconstitutional, preempted, or otherwise unenforceable.

SECTION 10. DO NOT CODIFY. Sunset and reauthorization.

(a) Sections 4-88-1304, 4-88-1306 through 4-88-1314, and any rules adopted under those sections shall expire on June 30 of the fifth full state fiscal year following the operative compliance date published by the Office of State Technology under Section 7 of this act, unless reauthorized by act of the General Assembly before that date.

(b) Not later than eighteen (18) months before the sunset date, the Office of State Technology, in consultation with the Attorney General and the Department of Finance and Administration, shall submit to the General Assembly a report addressing:
(1) The number of credentials issued, redeemed, replaced, and revoked;
(2) The number and disposition of covered notices submitted under § 4-88-1313;
(3) Aggregate, non-identifying data on system availability, outage incidents, and use of temporary alternative compliance methods;
(4) Aggregate, non-identifying data on security incidents, breaches, and remedial measures;
(5) Program revenues, costs, and self-funding status;
(6) Any documented instances of unauthorized retention, sale, licensing, profiling, or secondary use of age-assurance data;
(7) Any developments in federal law, including Section 230 jurisprudence and First Amendment jurisprudence, that materially affect the operation of this subchapter;
(8) The extent to which the certified successor local implementation provisions of this subchapter have been used and whether the boolean output requirement has been preserved in practice; and
(9) Recommendations for reauthorization, modification, or repeal.

(c) Upon expiration under subsection (a) of this section, all credentials issued under this subchapter remain valid for the duration stated on their face but shall not be renewed, and the Office of State Technology shall wind down the program in an orderly manner, including by purging age-assurance data in accordance with rules adopted under this subchapter.

(d) The protections of § 4-88-1308 governing data minimization, telemetry limits, secondary-use prohibitions, and segregation from advertising and profiling systems shall continue to apply to age-assurance data collected before the sunset date for as long as the data is retained.
