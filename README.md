# Arkansas Protects Our Children and Our Privacy Online Act

**A privacy-first alternative to operating system-level age verification.**

---

## Note from the Author

Hey y'all! This is a project I've been mulling over since I first saw California's A.B. 1043. That law is 100% a wolf in sheep's clothing. If you're reading this, then you probably know it is too.

If California's A.B. 1043 becomes the template for how we protect children from adult content across the country, we will essentially be handing over our every digital move to Big Tech and the government. That means journalists investigating corruption could be meticulously tracked by the very people they are investigating. It could even allow tech giants to track law enforcement officers who might be looking into their misdeeds.

And for the everyday libertarian, this means firearm enthusiasts could end up in the database they have worried about for decades. Not because they purchased a weapon, but because the content they consume places them in a group of people "likely" to own a firearm.

This kind of power is extremely dangerous, and it should scare the hell out of everyone in the country. Best case scenario, they use this information to target ads at us. Worst case, we get segregated into groups based on the content we consume, the items we purchase, where we travel, and more, then categorized as potential friends or potential enemies of the regime. The fact that our representatives are even considering this is deeply disturbing to me.

This kind of tracking will make us second-guess, or even fear, anything we say or do online, and maybe even in our own homes. It makes us much less free as Americans. But I guess if you say it's to "save the children," then it's worth slipping further and further into authoritarianism.

So that's all to say: I felt compelled to come up with a different template. And I think I came up with a concept that doesn't try to stand in front of the boulder rolling down the hill that is OS-level age gating. What my concept does instead is stand to the side and push it toward a more tolerable target.

I am not a lawyer. But I have always been a legal enthusiast. I've spent the past month or so forming these ideas, and when I was ready to put it all together, I kind of just vibe-coded this bill. I don't have the legal jargon to properly write it myself, but I was meticulous with my "pseudocode," if you will.

I've gone over what was written again and again for the past week or two. I've pitted different AI models, Claude Opus 4.7, ChatGPT 5.4 Thinking, Qwen 3.5, against each other. I prompted them to be critical, and sometimes even adversarial, toward what I was trying to achieve in order to strengthen the final product. And I'm pretty content with what resulted.

At this point, I think I've done all I can with this project, and I'm asking any of you with law degrees, computer science degrees, privacy expertise, security experience, or just sharp eyes to chime in. Please throw your thoughts and expertise into this work. Fork it, make it yours, fit it to your state, rip it to shreds in the issues section. This template can show California and the rest of the country that we can walk and chew gum at the same time.

If you do fork or clone this repo, please credit me, because the core concepts and the heart of this plan are mine. The work AI did was taking my manifesto/pseudocode and putting it into a pretty wrapper while I vigilantly micromanaged it and called balls and strikes as it did so.

---

## What this repository is

This is the working repository for a piece of Arkansas legislation that tries to do something most age-verification laws fail to do: protect kids online without building a surveillance system for everyone else.

The bill is being published openly because the federal government and many states are about to make decisions that will shape how every computer, phone, and operating system in the country handles identity and age for the next generation. The model in this bill is intended to be better than the alternatives currently on the table, and the author wants it to be copied, improved, forked, and used.

For the substantive context — California A.B. 1043, the federal Parents Decide Act, the App Store Accountability Act, and the state-level age verification laws in Utah, Texas, Louisiana, and elsewhere — see the Note from the Author above and the foundational `manifesto.md` document.

---

## What this bill actually does

In plain terms, the bill says:

**If Arkansas requires age verification at the operating system, device, or app store level, the only thing those systems can output is a yes-or-no answer to one question: is the current user 18 or older?**


That's it. Not the user's name. Not their date of birth. Not their exact age. Not a reusable adult token. Not a persistent identifier. Not a record of what they accessed. Not a callback to an issuer every time they open a website.

Just `is_18_plus = true` or `is_18_plus = false`.

Behind that simple answer, the bill builds a credential system:

- Adults prove they are 18 once, at the point of purchase of a computer, phone, or operating system, by showing a government ID to a participating retailer
- The retailer activates a one-time adult setup credential at checkout, the same way gift cards are activated today
- The customer redeems the credential during device setup
- After redemption, the credential is dead, the retailer is out of the loop, and nobody is logging the adult's later activity
- IT workers, students, security researchers, system administrators, and homelab hobbyists who reinstall systems often can apply for a long-term adult access permit instead of buying repeated one-time credentials

The bill prohibits selling, sharing, profiling, or making secondary use of any data collected through this system. It prohibits feeding that data into advertising, recommendation, or ranking algorithms. It prohibits routine issuer callbacks during ordinary later use. It includes a sunset clause forcing legislative review every five years. It caps fees in statute. It carves out research, journalism, and security disclosure. It builds in due process for anyone whose credential is wrongly invalidated.

---

## Who this bill protects

**Children**, who continue to be protected from material legally defined as harmful to minors, the same way they are under existing Arkansas law.

**Adults**, who can use computers, phones, and the internet without being forced into repeated identity checks, persistent tracking, or having their lawful activity logged.

**Families**, who don't want the devices in their homes turned into identity checkpoints just so their children can be safe online.

**Vulnerable communities** of every kind: people researching reproductive health care, people researching firearms and Second Amendment issues, people researching mental health resources, journalists protecting sources, religious minorities, political activists, immigrants, LGBTQ individuals, abuse survivors. A surveillance rail built today for child protection can be repurposed tomorrow for any kind of profiling. The narrower the system, the safer everyone is.

**Small businesses, developers, and security researchers** who would otherwise face a patchwork of state-by-state age verification requirements with conflicting data demands.

**Taxpayers**, because the program is designed to be self-funding through credential fees rather than ongoing general appropriations.

---

## Why operate this way instead of the California model

California's approach treats privacy as something to be sacrificed for child protection. It says: if you want children to be safe, accept that operating systems must transmit detailed age information across the device and software ecosystem.

We reject that false choice.

The Arkansas model proves you can have both. A binary signal is enough to protect children. Anything beyond that binary signal is not child protection — it's commercial surveillance, regulatory data collection, or future political infrastructure looking for an excuse to exist.

In Arkansas, we can walk and chew gum. We can protect kids and protect privacy at the same time.

---

## A note to other states and to Congress

If you are a legislator, staffer, advocate, or technologist working on age verification in another state or at the federal level, this work is yours to use.

You can:

- copy this bill in whole or in part
- adapt it to your state's legal framework and existing consumer protection statutes
- pull individual provisions like the boolean output rule, the issuer callback prohibition, the data segregation requirement, or the sunset clause and use them in your own legislation
- improve on what's here — there are certainly things this draft got wrong, things it missed, and things that could be better drafted

If you have improvements, please fork this repository, make your changes, and either open a pull request back here or run with it in your own jurisdiction. The goal is not to make Arkansas the only state with a privacy-preserving model. The goal is to make the privacy-preserving model the default everywhere.

If you find a flaw — constitutional, technical, fiscal, drafting, anything — please open an issue. Better to find problems now than after the bill is enacted.

---

## What's in this repository

```
.
├── README.md                              (this file)
├── CHANGELOG.md                           (substantive changes between bill versions)
├── manifesto.md                           (the foundational document — the lead author's plain-English architecture)
├── LICENSE.md
├── CONTRIBUTING.md
├── bill/
│   ├── README.md                          (explains the three versions and which to use)
│   ├── full-bill-text-v3.md               (current draft — the version intended for filing)
│   ├── full-bill-text-v2.md               (prior draft — preserved for reference)
│   └── full-bill-text-v1.md               (original draft — preserved for reference)
├── companion-resolutions/
│   ├── README.md                          (explains the chamber rules companion architecture)
│   └── chamber-rules-companion.md         (parallel House and Senate rules resolutions)
├── plain-english/
│   └── plain-english-explanation.md       (section-by-section everyman summary, v3-aware)
├── fiscal/
│   ├── fiscal-note.md                     (the formal fiscal note)
│   └── fiscal-note-methodology.md         (how the numbers were built)
└── letters/
    ├── README.md                          (overview of sponsor outreach)
    ├── rep-long.md                        (Rep. Wayne Long)
    ├── rep-pilkington.md                  (Rep. Aaron Pilkington)
    ├── rep-duffield.md                    (Rep. Matt Duffield)
    ├── rep-mcalindon.md                   (Rep. Mindy McAlindon)
    ├── rep-eubanks.md                     (Rep. Jon Eubanks)
    ├── rep-gramlich.md                    (Rep. Zack Gramlich)
    └── rep-garner.md                      (Rep. Denise Garner)
```

---

## Status

This is a working legislative draft. It has not been filed yet. It has not been formally scored by the Bureau of Legislative Research. The fiscal note included here represents our best estimate based on publicly available information about state IT systems, gift card distribution rails, and comparable credential programs through 2025. Final figures may shift after formal procurement consultation.

This draft is expected to change as it moves through committee, takes amendments, and absorbs feedback from constituents, technical experts, civil liberties advocates, child safety advocates, retailers, operating system vendors, and other affected parties. The version in this repository will be updated as the bill evolves.

---

## How to engage

**If you are an Arkansas resident:** Contact your state representative and state senator. Tell them you want this bill filed and supported. Use the letters in `/letters` as a template if you want to write to a specific legislator yourself.

**If you are a legislator or staffer in another state:** Take what's useful. Adapt it. File your own version. Reach out if you want to compare notes.

**If you are a technologist, lawyer, or academic with feedback:** Open an issue. Feedback is particularly valuable from people who can punch holes in the technical architecture, identify constitutional problems this draft missed, or improve the drafting.

**If you are a journalist:** The plain-English explanation in `/plain-english` is written for a general audience and is the best starting point.

**If you have a better idea:** Fork this repository and show how. This draft doesn't have all the answers. It's a starting point that is materially better than the alternatives currently being enacted, and it should keep getting better.

---

## Authorship and credits

The Note from the Author at the top of this README provides the personal account of how this work came together. This section provides the structured attribution detail that legal reviewers, journalists, and adapters in other states will want.

### Lead author

This bill originated with the lead author, who is not a lawyer. The foundational architecture of the bill — the document published in this repository as `manifesto.md` — was written first, in plain English, before any legislative drafting began. That manifesto sets out the principles every section of the bill is built to enforce.

**All core concepts, final decisions, cures, and concessions in this bill were made by the lead author.** The bill reflects the lead author's judgment, not the judgment of any AI system.

### The author's process

As described in the Note from the Author, the lead author's process was deliberately structured to use AI as a critic rather than a cheerleader:

- **Multiple fresh AI sessions used as critical sounding boards.** Rather than working in one long conversation where context could bias the analysis, the lead author opened many short sessions with fresh context. This was done to look at each problem from independent perspectives without the conversational momentum that can push an AI toward agreement.

- **Multiple AI models used adversarially against one another.** The lead author pitted Claude Opus 4.7 (Anthropic), ChatGPT 5.4 Thinking (OpenAI), and Qwen 3.5 (Alibaba) against each other on the same questions, prompting each to be critical of the others' analysis. This produced cross-model challenge that no single model would have generated on its own.

- **Deliberately seeking criticism of every idea and decision.** The lead author specifically prompted AI sessions to push back, identify weaknesses, and argue against proposed solutions before any commitment was made.

- **Grounding in current law and recently passed children's safety legislation.** The bill is built on the substantive framework of existing Arkansas law, the Texas H.B. 1181 architecture upheld in *Free Speech Coalition v. Paxton* (2025), the California A.B. 1043 model the bill is meant to provide an alternative to, and other state and federal proposals in this space.

- **Section-by-section review with fine-tooth-comb scrutiny.** Every section and subsection of the legislative draft was examined and approved by the lead author before being included. Nothing was accepted on faith.

### Core concepts originated by the lead author

The ideas that make this bill different from the California, Utah, and Texas family of age-verification laws were developed by the lead author and are documented in the manifesto. Specifically:

- **The boolean `is_18_plus` output as the only lawful external age signal.** The decision to require a single binary answer — yes or no — instead of age bands, exact ages, dates of birth, or persistent identity tokens is the central privacy commitment of the bill.

- **Purchasing an adult credential at retail with state or federal ID, modeled on age-restricted retail products.** The structural decision to treat the credential like an alcohol or tobacco purchase — show ID once at the point of sale, walk out with a one-time activation, no ongoing identity registration — is what makes the system work without a centralized identity registry.

- **One-time credentials that expire upon use or after a period of inactivity.** The decision that credentials must be short-lived, single-use, and self-destructing rather than reusable adult tokens is what prevents the credential from becoming a tracking instrument.

- **The professional and hobbyist permit carve-out with long-lived credentials.** The recognition that IT workers, students, security researchers, system administrators, software developers, repair technicians, virtualization engineers, and homelab hobbyists need a separate track — and that forcing them to repeatedly buy one-time credentials is both impractical and unfair — is what makes the bill workable for the technical community rather than hostile to it.

- **Surplus revenue allocated to a contingency reserve and to Arkansas public schools rather than to the general fund.** The decision to direct any program surplus to a reasonable operating reserve first, and then to school computer technology, K-6 STEM curriculum, and basic classroom supplies, rather than letting the program become a general revenue source, is what keeps the bill honest about its purpose. Money raised to protect children should be reinvested in children's futures, not absorbed into the budget for unrelated spending.

These are the ideas that distinguish this bill from every other age-verification law on the table. They are the lead author's. If you fork this work, those concepts are the foundation you are building on, and credit belongs to the lead author.

### AI assistance with drafting

The lead author is not a lawyer and does not know the formal legalese in which legislation is drafted. To translate the manifesto into actual statutory language, the lead author worked with multiple AI systems in the manner described above. Across the three models used (Claude Opus 4.7, ChatGPT 5.4 Thinking, and Qwen 3.5), AI assistance contributed to:

- Translation of the manifesto's concepts into formal legislative language consistent with the Arkansas Code structure
- Drafting suggestions for structural protections including the five-year sunset clause, the percentage-based pricing structure, the narrowing of strict liability to core data-misuse provisions, the kinship-caregiver language reflecting Arkansas's significant population of grandparents and other relatives raising children, the research and journalism carve-out, the coordinated vulnerability disclosure safe harbor, the eighteen-month implementation runway, the procedural protections on compelled-intermediary remedies, and the procedural protection of scope limitation in § 4-88-1314(g)
- Constitutional and federal-law analysis touching on Section 230, First Amendment doctrine after *Free Speech Coalition v. Paxton* (2025), and the dormant Commerce Clause after *National Pork Producers v. Ross* (2023)
- The Miller v. California correction in § 4-88-1303(24)(C) and the loophole closure in § 4-88-1314(d)(1)(A)
- Reconstruction of the fiscal note demand model, infrastructure cost estimates, and break-even analysis
- The hybrid distribution architecture analysis (pre-manufactured cards plus receipt-printed POS credentials)
- Drafting of the public-facing materials in this repository — the plain-English explanation, the methodology document, the chamber rules companion, the sponsor outreach letters, and the structured portions of this README

Every proposed addition, amendment, and structural change was reviewed and either accepted, modified, or rejected by the lead author. The formatting and phrasing throughout the legislative text and supporting materials reflect AI drafting assistance; the substantive content reflects the lead author's choices.

### Disclosure norm for adapters

If you adapt this work, please credit the lead author for the core architecture and disclose your own use of AI tools if any are involved in your drafting. AI assistance in legislative drafting is a current and growing reality. The norm of transparency is part of what makes cross-jurisdictional collaboration on legislation trustworthy, and that norm is easier to establish if people who use these tools well are open about it.

### Acknowledgments to come

As this bill moves through the legislative process and as contributors engage with this repository, additional acknowledgments will be added for substantive contributions. If you contribute, you will be credited for what you contributed.

---

## License

The text of legislation is, by its nature, public. Anything in this repository that is or will become part of an Arkansas bill is in the public domain. Commentary, plain-English explanations, fiscal analysis, and letters in this repository are released under Creative Commons Attribution 4.0 (CC BY 4.0) — copy them, modify them, use them in your own work, just credit the source.

---

*"Child protection should not require treating every adult as a suspect."*
