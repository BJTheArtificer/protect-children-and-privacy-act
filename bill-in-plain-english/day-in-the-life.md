# A Day in the Life of the Privacy-Preserving Adult Access System

This document walks through how the Arkansas Protects Our Children and Our Privacy Online Act actually works in practice — from the perspective of an ordinary Arkansan who buys a computer and uses it. It is plain-language and illustrative. For the formal section-by-section walkthrough, see `plain-english-explanation.md`. For the legal text, see `bill/full-bill-text-v3.md`.

---

## Jimmy buys a computer

This is Jimmy. Jimmy is a 28-year-old man, and he's shopping for a new laptop. He finds the one he wants and brings it to the counter.

When the cashier rings him up, she asks: "Will you be setting this up as an adult device? If so, you'll want to grab one of our Adult Setup Cards — we can activate it with your purchase for $6. You'll need a valid government ID."

Jimmy says yes, hands over his Arkansas driver's license, and the cashier does two things at once: she verifies he's at least 18 (the same way she'd do for an age-restricted purchase like alcohol or tobacco), and she scans the activation barcode on the back of the Adult Setup Card. That scan pings the state's credential backend, which marks the card as activated and starts a short clock for redemption — set by rule, but think of it as several days.

The cashier doesn't keep a copy of Jimmy's ID. She doesn't enter his name, address, or birth date into anything. She just confirmed he was old enough and triggered the activation. The card itself contains no information about Jimmy — it's an anonymous, single-use credential with two parts: a public activation barcode that's now been validated, and a hidden one-time redemption code under a scratch-off coating that Jimmy hasn't seen yet.

Jimmy leaves with his laptop and his Adult Setup Card.

## Jimmy sets up his laptop

That evening, Jimmy boots up the laptop and starts the setup wizard. He sets a username and password, picks his time zone, agrees to the operating system's terms, and then reaches a screen that asks: "Would you like to enable adult access on this device?"

The screen explains that an adult-enabled local user account can access age-restricted content and apps without further verification, and that Jimmy will need an Adult Setup Card to enable it. If he skips this step, his account will be set up as a standard non-adult-enabled account, and he can enable adult access later if he wants.

Jimmy scratches off the silver coating on the back of his card to reveal the redemption code, types it into the setup wizard, and hits Enter.

The laptop sends a redemption request to the state's credential backend. The backend checks four things: is the credential real, was it activated, has it not yet been redeemed, and has the redemption window not expired? All four check out. The backend marks the credential redeemed (it can never be used again), and returns a confirmation to the laptop.

The laptop then stores a small piece of cryptographic state inside its operating system: this local user account is now adult-enabled. That's it. The state backend doesn't store who Jimmy is, where the redemption came from, or what device received it — the redemption call is processed and the routing information is discarded. There's no record connecting Jimmy's identity to this device.

Jimmy throws the now-useless card in the trash and finishes setting up his laptop.

## Jimmy uses his laptop

A week later, Jimmy is browsing the internet on his laptop. He visits an adult content site. The site, like all websites covered by Arkansas law that publish a substantial portion of material harmful to minors, needs to verify that whoever is visiting is an adult.

The site's age check doesn't ask Jimmy for his ID, his birth date, his name, or anything else. It asks his operating system one question: `is_18_plus`?

The operating system checks whether the local user account currently in use is adult-enabled. It is. So it returns: `true`.

The site lets Jimmy through.

That's the entire interaction. The site never learns Jimmy's age, his name, his date of birth, or anything else about him. It just learns that whoever is using this device, in this user account, right now, is an adult. The state's credential backend isn't involved in this query — it happened weeks ago and is completely out of the loop. The Adult Setup Card itself was destroyed weeks ago. There's no central log anywhere of Jimmy visiting that site.

Later that week, Jimmy installs an app from the app store that's rated adult-only. Same boolean query, same answer, same lack of tracking.

## Jimmy's nephew visits

Jimmy's 14-year-old nephew Tyler comes over for the weekend and asks to use the laptop to do homework. Jimmy creates a second user account for Tyler — a standard, non-adult-enabled account — and lets him sign in.

When Tyler is signed in and a website or app asks `is_18_plus`, the operating system answers `false`. Critically, it returns that `false` in exactly the same way it would for any other context where adult status hasn't been confirmed: an adult who hasn't enabled adult access on their account, a guest account, a freshly installed device, anything. The operating system does not know or signal that this particular `false` is being returned because the user is a minor. It can't, by law. The bill explicitly forbids the program from being used to identify, classify, profile, monitor, or restrict minors, and it specifically requires that minor responses be returned identically to any other unauthenticated response.

This is intentional. The system is designed to verify adulthood, not to surveil children. Parental controls — what Tyler can and can't access on the device — are a completely separate matter, handled by the operating system's existing parental-control tools (the same tools that exist today, like the controls Tyler's parents probably already configured on his own devices). Those tools work the same way they did before this bill existed, and they operate entirely outside the credential system.

When Tyler signs out and Jimmy signs back into his own account, the boolean answer flips back to `true`.

## Two years later: Jimmy sells the laptop

Jimmy upgrades to a newer laptop and sells the old one to his coworker Maria.

Before handing it over, Jimmy does a factory reset. The factory reset clears the adult-enabled state along with everything else on the device — the bill requires credential redemption to be scoped to a local user context, so wiping the device wipes the credential. When Maria boots up the laptop for the first time, she goes through the same setup wizard Jimmy did two years earlier — including the same screen asking whether she wants to enable adult access.

Maria, who is 31, picks up an Adult Setup Card on her next trip to the grocery store, brings it home, and redeems it the same way Jimmy did. Now her account is adult-enabled. Her usage is independent of Jimmy's prior usage. The system has no memory that Jimmy ever owned this laptop.

## Six months later: Maria's card gets stolen — well, almost

A few months after Maria sets up the laptop, she goes back to the same store to buy an Adult Setup Card for her tablet. Between her car and her front door, the card slips out of her bag onto the driveway. By the time Maria notices the next morning, the card is gone.

Maria calls the issuer's compromise reporting line — printed on her receipt — and reports the activated-but-unredeemed card as lost. The issuer marks that specific credential identifier on the blacklist, and within a few minutes the card is dead — even if someone finds it and tries to redeem it, the backend will reject it.

Maria takes her receipt back to the store and gets a replacement card without having to re-prove her age. The bill specifically requires this: when a credential is invalidated through no fault of the holder, the holder gets a replacement promptly without repeating the underlying age proofing. Maria leaves with a fresh card and uses it that evening.

## Two years from now: Jimmy starts a homelab

Jimmy gets into homelabbing as a hobby — he's spinning up virtual machines, reinstalling operating systems for testing, and trying out different Linux distributions on spare hardware. He realizes he'd be buying a new $6 Adult Setup Card every couple of weeks, which is impractical.

He applies online for an Adult Access Permit. The application asks for proof he's an adult, a one-paragraph statement of what he's using it for ("homelab and personal infrastructure testing"), agreement that he won't knowingly pass the credential to a minor, agreement to report compromise, and agreement that compromised credentials may be invalidated. He pays a modest annual permit fee — capped in statute at $25 — and gets back a long-term Adult Access Credential. Now he can authorize adult setup repeatedly across his test machines without buying disposable cards.

The permit doesn't track which machines Jimmy sets up or what he does with them. It just lets the boolean answer be `true` on systems he's authorized.

## Meanwhile: a school district in Mountain View

Jimmy doesn't see this part. But the $5 of his $6 card purchase that went to the state didn't disappear into the general fund. It went into the Arkansas Child Protection and Online Privacy Fund — a dedicated account that exists only to administer the credential program.

That fund covers operating costs first: the state-certified backend that processed Jimmy's redemption, customer service, fraud handling, replacement cards like Maria's, and a reasonable operating reserve. Anything left over after operating costs and reserve is surplus.

The Office of State Technology, working with the Arkansas Department of Education, distributes that surplus to public school districts and public charter schools — using the same school funding formulas the Department of Education already uses for other programs, or a comparable per-pupil or per-school distribution mechanism. The money can only be used for three things:

- Computer technology in school computer labs and classrooms
- K-6 STEM curriculum (the bill specifically emphasizes building foundations in computer science and STEM in early grades, where it matters most)
- Basic classroom supplies — paper, pencils, the consumables teachers too often buy out of pocket

A teacher in Mountain View School District, Mrs. Lawson, opens her classroom budget allocation for the year and notices an additional line item: roughly $85 in classroom supplies funded through the Child Protection and Online Privacy Fund. She uses it to stock pencils, notebooks, and a pack of dry-erase markers. Across the district, the elementary STEM lab gets a couple of refurbished Chromebooks from the same source. Across the state, schools collectively receive several hundred thousand dollars from the fund that year.

Mrs. Lawson never knows that Jimmy bought a laptop two years ago and that some fraction of his card price ended up paying for her dry-erase markers. The connection is invisible to both of them. But it's the connection the bill was designed to make.

The amount each school receives varies year to year. Some years there's no surplus to distribute — the program has to cover operating costs first, and if costs are higher than expected or if demand dips, surplus gets thinner. The bill makes school distribution a discretionary use of any surplus that exists, not a permanent revenue stream. The schools never get to depend on it as a budget line, which means the program never gets captured by school-funding politics. When surplus exists, schools benefit. When it doesn't, the program's primary obligation — running the credential system — is protected.

If surplus persists for three consecutive years above what's needed for reserve and reasonable distribution, the bill requires a price review and probable price reduction. The program can't quietly become a revenue source for the state. It either runs at cost-recovery, or prices come down.

## What the system never built

Walk back through the day in the life: Jimmy bought a card, redeemed it, used a website, had a guest, sold a laptop. Maria reported a compromise. Mrs. Lawson got a budget supplement.

What's *not* anywhere in this story:

A database connecting Jimmy to his laptop. A database connecting Jimmy to the website he visited. An API call from the website to a state server confirming Jimmy's identity. A persistent identifier following Jimmy across services. A profile of Jimmy as "an adult" that gets sold to advertisers. A record of Tyler being identified as a minor. A registry of who used Adult Setup Cards. A central log of when adult-rated content was accessed in Arkansas.

None of that exists, because the bill made it illegal to build any of it.

Jimmy is just a 28-year-old who bought a laptop, set it up, and went about his life. The state, behind the scenes, verified once that he was old enough and then forgot about it. That's the entire system.
