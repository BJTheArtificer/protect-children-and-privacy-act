# Arkansas Protects Our Children and Our Privacy Online Act

**A privacy-first alternative to operating system-level age verification.**

This is the working repository for a piece of bipartisan Arkansas legislation that tries to do something most age-verification laws fail to do: protect kids online without building a surveillance system for everyone else.

We are publishing this work openly because we believe other states and the federal government are about to make decisions that will shape how every computer, phone, and operating system in the country handles identity and age for the next generation. We think the model in this bill is better than the alternatives currently on the table, and we want it to be copied, improved, forked, and used.

---

## Why this bill exists

Age verification on the internet is no longer a question of *if* — it is a question of *how*.

California passed Assembly Bill 1043 in October 2025, requiring operating systems and app stores to handle age signals starting in 2027. The federal Parents Decide Act and the App Store Accountability Act would push similar requirements nationwide. Utah, Texas, Louisiana, and a growing list of other states have enacted or are debating their own versions.

The boulder is rolling downhill. Operating-system-level age verification is coming whether anyone likes it or not.

The question is: **what shape will it take?**

The default direction the country is moving is toward systems that:

- collect dates of birth, exact ages, government ID images, or biometric data
- transmit age signals tied to persistent device or account identifiers
- create records of who accessed what content and when
- give app stores, operating system vendors, and the state visibility into lawful adult activity
- treat every device interaction as a potential tracking event

That is not child protection. That is the foundation of identity surveillance, dressed up as child protection.

This bill is the alternative.

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
- improve on what we've done — we are certain there are things we got wrong, things we missed, and things that could be better drafted

If you have improvements, please fork this repository, make your changes, and either open a pull request back here or run with it in your own jurisdiction. The goal is not to make Arkansas the only state with a privacy-preserving model. The goal is to make the privacy-preserving model the default everywhere.

If you find a flaw — constitutional, technical, fiscal, drafting, anything — please open an issue. We would rather find problems now than after the bill is enacted.

---

## What's in this repository

```
.
├── README.md                              (this file)
├── bill/
│   └── full-bill-text.md                  (the complete bill, current draft)
├── plain-english/
│   └── plain-english-explanation.md       (section-by-section, no legalese)
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

We expect this draft to change as it moves through committee, takes amendments, and absorbs feedback from constituents, technical experts, civil liberties advocates, child safety advocates, retailers, operating system vendors, and other affected parties. The version in this repository will be updated as the bill evolves.

---

## How to engage

**If you are an Arkansas resident:** Contact your state representative and state senator. Tell them you want this bill filed and supported. Use the letters in `/letters` as a template if you want to write to a specific legislator yourself.

**If you are a legislator or staffer in another state:** Take what's useful. Adapt it. File your own version. Reach out if you want to compare notes.

**If you are a technologist, lawyer, or academic with feedback:** Open an issue. We particularly want to hear from people who can punch holes in the technical architecture, identify constitutional problems we missed, or improve the drafting.

**If you are a journalist:** The plain-English explanation in `/plain-english` is written for a general audience and is the best starting point.

**If you have a better idea:** Fork this repository and show us. We don't think we have all the answers. We think we have a starting point that is materially better than the alternatives currently being enacted, and we want it to keep getting better.

---

## License

The text of legislation is, by its nature, public. Anything in this repository that is or will become part of an Arkansas bill is in the public domain. Commentary, plain-English explanations, fiscal analysis, and letters in this repository are released under Creative Commons Attribution 4.0 (CC BY 4.0) — copy them, modify them, use them in your own work, just credit the source.

---

*"Child protection should not require treating every adult as a suspect."*
