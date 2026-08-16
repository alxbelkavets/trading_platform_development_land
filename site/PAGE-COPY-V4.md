# Trading Landing — Page Copy (v4)

Every visible string for the new page, in page order, following the structure in
[PAGE-PLAN.md](PAGE-PLAN.md).

**How to read this file.** Plain text is copy, ready to set. Blockquoted notes are for us, not the
visitor. `[NEEDED: …]` marks a real gap that a person has to fill; those are listed together in
[§ Open inputs](#open-inputs) at the end. Nothing in this file invents a figure, a certification, or
a client claim.

Decisions carried in from the plan: the original hero stays; the build/modernize/integrate cards
stay as they are; scarcity is out and risk reversal is in (see [§8](#8--the-first-step)).

---

## Page meta

- **Title tag:** Trading Platform Development | Itexus
- **Meta description:** We build trading and investing platforms for fintechs and investment
  managers: order management, execution middleware, FIX gateways, market data, KYC/AML. Shipping
  since 2013.

---

## 0 / Header

- **Logo:** Itexus
- **Nav:** Services · Where to Start · Case Studies · Hire Developers · About Us
- **Button:** Tell us what you're building

> The button said *Contact Us*, the hero said *Get a proposal*, the mid-page band said *Get a
> proposal*, and the form button said *Send*. One wording now, in all four places. It asks for less
> than a proposal does, and it can't be contradicted by who actually joins the call.
>
> **Update:** shipped as *"Talk to a trading architect"*, then changed again — the first call is
> actually with a BD rep, not an architect. Architects are expensive and booked on real projects;
> putting one on every inbound lead call isn't something we can staff yet, however good it would be.
> A named-role CTA the process can't honour on contact 1 is worse than a generic one kept honestly,
> so the specificity moved down into §8, where the two-step process is spelled out instead of implied
> by the button.

---

## 1 / Hero (`#top`)

**Eyebrow:** Trading platform development

**H1:** We've built trading platforms before. **We can build yours.**

> Bold part in brand green, as before.

**Subhead:** FIX gateways, market-data fan-out, KYC/AML, audit trails. We build trading and
investing products for fintechs and investment managers, and this is the stack we work in.

**Primary button:** Tell us what you're building
**Secondary button:** See the platforms we've built →

**Assurance line:** We reply within 24 hours and sign an NDA before you share the details.

**Proof strip:** 300+ projects · Building since 2013 · 4.9 on Clutch from 40 reviews

**Hero image alt:** Trading app screens: a wallet balance with deposit and withdraw controls, and a
live candlestick price chart

> Unchanged apart from the button. The subhead is carrying more weight than the headline here, and
> the specific words are the reason. Don't smooth them out.

---

## 2 / Facts strip (new)

> Sits directly under the hero. No heading, no lede, no prose. A single band of labelled values.
> The reader has a comparison table open in another window and is filling cells; this is the row.
> Everything here should be copy-pasteable in one drag.

| Label | Value |
|---|---|
| Clutch | 4.9 from 40 reviews |
| Building since | 2013 |
| Projects delivered | 300+ |
| Team | `[NEEDED: headcount, e.g. "120 engineers"]` |
| Working from | `[NEEDED: locations + hours of overlap with US / UK / EU]` |
| Paperwork | NDA and DPA, signed before the first call |
| First reply | Within 24 hours |
| Typical MVP | 3 to 4 months |

**Client logos:** `[NEEDED: 2–3 logos cleared for public use. Coinstar is already public on the
current page. If nothing else clears, run the strip without logos rather than with filler.]`

---

## 3 / Case studies (`#case-studies`)

**Eyebrow:** Case Studies

**H2:** Trading platforms we've built

**Lede:** Four production systems: three anonymised trading platforms, and a crypto wallet ecosystem
for a fintech with $2.2 billion in annual revenue.

> **The placeholder digits come out of the build before anything else ships.** `00.0 ms` and
> `000 k/day` are visible to visitors right now with no disclaimer, and this is the one section
> where a reader looks hardest. A card with no metrics reads as reticent. A card with fake ones
> reads as fake.
>
> The metric slots below stay empty until someone fills them. Anonymised and bounded is fine and
> needs nobody's permission: *European broker · 12 months · 40k accounts · sub-100ms order
> round-trip · FIX 4.4 to two prime brokers.* That sentence contains no client identity and it
> answers the only question this section exists to answer.

### Featured — Coinstar

- **Tag:** Featured
- **Title:** Cryptocurrency e-Wallet Ecosystem for a Global FinTech Enterprise
- **Body:** PCI DSS-compliant application ecosystem for Coinstar, an international fintech company
  with $2.2 billion in annual revenue: web and mobile crypto wallets, embedded kiosk software, and
  a cloud-based API server.
- **Metrics:** `[NEEDED: 3 figures. Useful shapes — transactions per day, time from kickoff to
  first live release, kiosk or endpoint count, uptime under load.]`
- **Tags:** Enterprise · Fintech
- **Image alt:** Coinstar crypto wallet application screens

**Paired quote:** `[NEEDED: verify which project the Risk Management Director quote belongs to
before pairing it with any card. A testimonial sitting next to the wrong case study is worse than
one sitting in the carousel.]`

### Automated Stock Trading Platform

- **Badge:** Under NDA
- **Body:** An automated, real-time trading system that lets administrators configure and run
  trading strategies.
- **Metrics:** `[NEEDED: order latency, peak message rate, strategies running concurrently]`
- **Tags:** Fintech · Trading
- **Image alt:** Automated stock trading platform on a laptop, showing a candlestick chart and
  strategy modules

### Stock Trading Signals Platform

- **Badge:** Under NDA
- **Body:** An investment assistant that runs technical analysis across a universe of stocks and
  delivers signals to subscribers.
- **Metrics:** `[NEEDED: instruments covered, signal delivery time, subscribers]`
- **Tags:** Fintech · Trading
- **Image alt:** Stock trading signals platform on a laptop, showing the signal library and signal
  settings table

### Algorithmic Intraday Stock Trading System

- **Badge:** Under NDA
- **Body:** A SaaS system for automated intraday trading that connects to investors' own brokerage
  accounts.
- **Metrics:** `[NEEDED: broker integrations, accounts connected, uptime during market hours]`
- **Tags:** Fintech · Trading
- **Image alt:** Algorithmic intraday trading dashboard showing recent trades and account statistics

---

## 4 / Where you're starting (`#where-to-start`)

**Eyebrow:** Where You're Starting

**H2:** Build, modernize or integrate

**Lede:** The four platforms above started in three different places. Find the one that matches
yours.

**01 — Build** *(New platform, from scratch)*
You have a strategy, a licence, or a client base, and no platform yet. We take it from discovery and
architecture through broker and market-data selection, order management, risk controls, web and
mobile terminals, and KYC/AML.

**02 — Modernize** *(An existing platform that caps what you can add)*
It runs, but a legacy vendor, an unsupported stack, or latency in the hot path limits what you can
ship next. We audit the current system, replace the execution and market-data layers a slice at a
time, and migrate data without taking trading offline.

**03 — Integrate** *(One component into a stack you already run)*
The platform exists; you need something wired into it. FIX and proprietary gateways, broker and
exchange APIs, market data and news feeds, payment and KYC/AML providers, portfolio and reporting,
scoped as a project or delivered by engineers embedded in your team.

**Footer link:** Not sure which one you're in? Describe the situation and we'll tell you which path
fits → (`#contact`)

> Unchanged. This section already does its job.

---

## 5 / What we build (`#capabilities`)

**Eyebrow:** What We Build

**H2:** Trading Platform Capabilities

**Lede:** The parts a trading platform needs to actually go live, and what tends to go wrong in
each one.

**Screenshots (keep all three, in this order):**

1. Onboarding — *alt: Onboarding screen from a trading app*
2. Order entry, limit price — *alt: Order entry screen with a limit price slider*
3. Trade confirmation — *alt: Order confirmation screen after a trade*

> **Every second line below needs an engineer to sign off before it ships.** They are written from
> published domain knowledge, not from our project history, and a reader who spots a wrong detail
> is exactly the reader we are writing for. Cut anything nobody will vouch for. Don't soften it,
> cut it.
>
> The regulatory and protocol specifics carry dates and versions on purpose. Re-check them against
> primary sources at publication.

### The 12 capabilities

**1. Integration With Brokers**
We help select and integrate brokers on market coverage, API quality, latency, and SLA. The SLA
tells you about uptime and nothing about what your open orders look like after a gateway restart,
so we test reconnection and state recovery before we recommend anyone.

**2. Trading Execution Middleware**
Messaging, market-data fan-out, FIX and proprietary protocols in one low-latency layer. Most of the
work is at the session layer: sequence gaps, resend requests, gap fill, and suppressing the
duplicate execution that arrives with `PossDupFlag=Y` after a recovery. Plenty of counterparties
are still on FIX 4.2, and the version you get is rarely the version you wanted.

**3. Order Management**
Order types, time in force, leverage, stop-loss and take-profit. What makes it hard is the state
machine: a cancel and a fill crossing on the wire, a replace that gets rejected and forks the
`ClOrdID` chain, and a session that drops with an order still unacknowledged.

**4. Investor Interfaces**
Web, mobile, and desktop with fast presets, hotkeys, and watchlists. The screens that matter most
are the ones showing an order whose state is uncertain. Telling a user their order was cancelled
when it actually filled is a support ticket that becomes a complaint.

**5. Market Data Storage**
A multi-source store with historical intraday data for equities, futures, FX, and options. Budget
for entitlements early: per-user reporting to the exchange, redistribution licensing, and
non-display fees are a cost line that surprises product teams, usually in the form of an audit that
arrives with a bill.

**6. Trading Algorithms**
We implement your strategy and can add a no-code builder with parameter checks and safeguards. Those
checks do most of the work. A market order on an illiquid symbol at the open, with no pre-trade
guardrail, fills far from the last print, and the user only finds out once it has.

**7. Strategy Builder**
A visual builder and a code editor for custom indicators and algorithms. One engine runs both the
backtest and the live strategy, because two engines drift and the user discovers it with real money
on the line.

**8. Backtesting**
Test and optimise strategies against historical data before risking anything. A backtest is only
worth the assumptions underneath it: survivorship bias in the instrument universe, look-ahead bias
in the data, and fill assumptions that ignore queue position will all flatter a strategy that loses
money live.

**9. Real-Time Alerts**
Asset alerts that reach the user within seconds of a target price move. The rules need to know what
to do about prints inside a halt or an auction, or the alert fires on a price nobody could have
traded at.

**10. Trade Log**
Trading histories that let users find their mistakes and adjust. Underneath it sits the audit
trail: every state change, every override, every manual approval, stored immutably. SEC 17a-4 and
FINRA 4511 set the retention expectations, and CAT requires clocks within 50 ms of NIST. Retrofitting
any of this later is a rewrite.

**11. Paper Trading**
Simulated trades under live market conditions with no money at risk. Naive simulators are optimistic:
they fill at the touch, ignore queue position, and never partial-fill. Traders who practise against
one and then trade for real get results that don't match, and they tend to blame the platform.

**12. Other Features**
Portfolio management, FIX gateways, and scalable matching components. Corporate actions cause more
trouble here than their profile suggests. A split, a spin-off, or a symbol change has to move
positions, cost basis, open orders, historical charts, and the tax lot ledger together, and it is
where a lot of platforms find out their data model was wrong.

---

## 6 / What usually goes wrong (new)

**Eyebrow:** Engineering notes

**H2:** The parts of this that usually go wrong

**Lede:** Four of the failure modes we design around. None of them are exotic, and each one is far
cheaper to handle in the design than in production.

> The buyer's fourth priority is whether we can name the hard parts before he does. This is the
> section that answers it, and unlike everything in §3 it needs no client permission and no metrics.
> Four items on the page, the rest on a separate engineering page.

**A cancel and a fill cross on the wire**
The cancel goes out, the fill comes back first, and the reject follows. Systems that trust arrival
order show the user a cancelled order that actually executed, and the position and cash stay wrong
until somebody reconciles them.

**Market-data entitlements arrive as a bill**
Per-user reporting to the exchange, redistribution licensing, and non-display fees are all
contractual, and none of them appear in an API doc. Scoping market data as an integration task
misses the commercial negotiation underneath it, which is usually where the cost sits.

**The affirmation cutoff on trade date**
US equities have settled T+1 since May 2024. Miss the affirmation window and the trade fails. What
used to be a back-office nuisance is now an engineering deadline, and the UK, EU and Switzerland
reach the same point in October 2027.

**Average-price rounding breaks reconciliation**
Recompute `AvgPx` client-side from individual fills instead of trusting what the counterparty sent,
and the number drifts by fractions of a cent. Nobody notices until the end-of-day file doesn't
match.

**Link:** The rest of the list, with what we do about each → `[NEEDED: engineering notes page. Scope
it separately. Don't publish a count in this link until the page exists and an engineer has cut it
down to what we can defend.]`

---

## 7 / Security, compliance and ownership (new)

**Eyebrow:** How we handle risk

**H2:** Security, compliance, and who owns what

**Lede:** The questions procurement sends us, answered up front.

> Written as a labelled band, same treatment as §2, not as paragraphs. This is the section a
> Level-3 buyer arriving with an RFP checks first, and its absence is why we start behind vendors
> who published theirs.
>
> **Honesty rule for this whole section: name what we hold and name what we don't.** "We work to
> ISO 27001 practices and are not certified" beats silence, and it beats a badge nobody can verify.
> Every line below is a fact somebody has to supply.

| | |
|---|---|
| **Certifications we hold** | `[NEEDED: the real list, or the honest empty answer]` |
| **Standards we work to** | `[NEEDED: e.g. ISO 27001 practices, OWASP ASVS. Say "work to" where we're uncertified.]` |
| **Regulatory regimes we've shipped under** | `[NEEDED: name them. MiFID II, FINRA, MiCA, FCA — whichever are true. This is the single most valuable line in the section and a competitor already leads with theirs.]` |
| **Compliance work we've delivered** | PCI DSS-compliant ecosystem for Coinstar. KYC/AML onboarding, sanctions screening, and audit trails across the trading platforms above. |
| **Data residency** | `[NEEDED: which regions we can host in]` |
| **Secure development** | `[NEEDED: code review, dependency scanning, pen-test cadence and who runs it]` |
| **Paperwork** | NDA and DPA signed before the first call. |
| **Source code** | `[NEEDED: confirm with legal — who owns the repository during and after the engagement, and what the handover contains]` |
| **If we part ways** | `[NEEDED: confirm with legal — handover scope, documentation, notice period, and whether the client's own team can take it over]` |

---

## 8 / The first step (new)

**Eyebrow:** What happens next

**H2:** A short call first, then a team on your problem

**Lede:** The first conversation is short and it's about your project. What we do after it depends
on what we hear.

**The first call**
Thirty to forty-five minutes. What you're building, where it starts, and the constraints you're
working under: venues, asset classes, regulatory regime, timeline, and the shape of the budget. We
sign the NDA before it. There are no slides.

**Then our engineers take it**
If there's a project here, we put a team on it: a solution architect, a fintech analyst, and a
designer where design matters. You get an architecture and integration outline, and an indicative
range with its assumptions written down. Where it would help you decide, that can extend to an
interactive prototype you can click through, or look-and-feel screens of the real product.

**Why it's shaped this way**
We don't put an architect on the first call. The good ones are on projects, and you get more from a
real team on the second conversation than from a senior title on the first. Most people who contact
us aren't the person who signs either, so what matters is what you can take into the room where the
decision gets made.

**Button:** Tell us what you're building

**Risk-reversal line:** Both are free and carry no obligation. The write-up is yours to use whether
or not you hire us.

**Handoff line, into §9:** When the scope is big enough that guessing at it is the expensive option,
the next step is a short fixed-price Discovery or System Design phase.

> **Update:** this section originally described the first call itself as the architect
> conversation — *"An hour with the person who would design the system, rather than a discovery call
> with an account manager."* That's backwards from how the first call actually works: it's a BD rep,
> not an architect, because architects are booked on real projects and can't be put in front of every
> inbound lead. Rewritten around the real two-step process instead of the aspirational one-step
> version. The second step is arguably the stronger claim anyway — an interactive prototype the buyer
> can click through beats a one-page architecture diagram as something to carry into a board meeting,
> which is the actual job this whole page is designed around (see BUYER-EVALUATION's "internal
> advocate" framing in PAGE-PLAN.md §1).
>
> **This is still the "guarantee, not scarcity" decision, made concrete.**
>
> The research suggested two things. One was manufactured urgency ("2 discovery slots left this
> month"). That's out. It would be invented, and inventing pressure in front of a buyer whose whole
> job is assessing vendor risk costs more than it earns.
>
> The other was a guarantee, and the useful version of that is simply removing what he stands to
> lose. He risks a short call and gets a written outline he can present either way. That's true
> today, costs nothing, and no competitor on the list says it.
>
> A stronger conditional guarantee is available if you want it, and it only applies once Discovery
> is a paid engagement (see §9): *"if the discovery architecture and estimate aren't usable, we
> refund the discovery fee."* That is a real commercial commitment. `[NEEDED: your call. Don't
> publish it unless we would honour it without arguing.]`

---

## 9 / How we work (`#engagement`)

**Eyebrow:** How We Work

**H2:** Engagement models

**Lede:** Three ways to structure the work. Which one fits usually depends on what your board can
approve.

**Discovery / System Design** *(fixed price, before any of the models below)*
A bounded phase that ends in requirements, an architecture, and a plan the build can be priced
against. This is where an interactive prototype or look-and-feel screens get produced when the
project calls for them.

**01 — Time & Material (Efficient Hours)** *(badge: Recommended)*
*Agile with budget control.* Two-week sprints, a demo at the end of each one. You pay for the actual
work performed on your project, and can change direction as you learn.

**02 — Fixed Price**
Requirements, price, and timeline documented and signed before work starts. Suits a scope that's
already well defined and unlikely to move.

**03 — Outstaffing**
*Development team as a service.* Vetted engineers join your team, work under your project
management, and bill at a pre-agreed monthly rate.

**Cost line:** `[NEEDED: a decision, then a number. Something like "integration projects typically
start at $X; full platforms run $Y to $Z depending on venues and asset classes." He has to open a
board conversation with an order of magnitude. If we publish nothing, he anchors on whichever
competitor did.]`

> **Update:** *"Efficient Hours"* is our own coinage for what procurement knows as Time & Material —
> a buyer comparing three vendors' engagement models shouldn't have to stop and decode ours, so the
> recognised term now leads and the coinage survives in parentheses for continuity with contracts and
> the `/how-we-work/` page. The body copy also drops "within an agreed estimate" (a cap the model
> doesn't actually guarantee) in favour of "the actual work performed on your project."
>
> The Discovery / System Design phase is new — it's the one small, bounded, priced thing on the page
> a visitor can say yes to without committing to a full build, and it's where §8's prototype and
> design-screen offer actually gets delivered. It also makes the conditional guarantee parked at the
> end of §8 coherent: a refund only makes sense once Discovery is something we've been paid for.

**Footer link:** See the full breakdown of each model on our Cooperation Models page →
(`/how-we-work/`)

---

## 10 / What clients say (`#testimonials`)

**Eyebrow:** What Clients Say

**H2:** What our clients say about us

> Real carousel with prev/next controls. A static grid was tried and rejected.
>
> Quote 1 moves up to §3 if it can be matched to a case study; the carousel runs the remaining four
> if it does. Every quote we have praises responsiveness and project management, and none says the
> system worked. For a reader whose fear is recommending the vendor whose platform broke, that's
> the wrong evidence. `[NEEDED: one quote about the platform under load or through launch. Worth
> asking for directly at the next reference call.]`

1. "Itexus delivered the app according to the requirements. The team met all development milestones
   and deliverables. They were efficient, friendly, and cooperative. Itexus team was very timely
   with updates, a regular meeting cadence, and ad-hoc questions and answers via Slack. The team was
   very responsive and still is."
   — **Risk Management Director**, Investing Fund

2. "Itexus' work positions the business well for an imminent launch. They excel at managing their
   team, presenting frequent product demos to ensure that the project is aligned with development
   goals. An affordable price structure coupled with remarkable technical skill makes them an
   attractive partner."
   — **Phill Osolinski**, CEO Ryze Rewards

3. "The assigned team was easy to work with and they are especially strong collaborators and
   communicators. They demonstrated flexibility, professionalism, and trust in everything they did,
   and completed the work on time and budget."
   — **Sue Wollan Fan**, CEO Mango Connects

4. "Itexus excelled at both experimental AI and sprint-oriented UI/UX tasks. Itexus did strong
   project management work, too, a necessity in such a complicated project."
   — **Jesse Dubin**, Senior PM Standard&Poors

5. "They're a great group of developers who really understand the reality of business."
   — **Andreea Vanacker**, CEO SPARKX5

**Clutch strip:** 4.9 rating from 40 reviews

**Award marquee (all 12, don't trim):** GoodFirms · YouTeam · Clutch · Expertise · SelectedFirms ·
TopDevelopers · Top Rated Custom Software Development Companies · ITFirms · TrustFirms · Top
Software Developers · Top Rated Mobile App Companies · techreviewer.co

---

## 11 / FAQ (`#faq`)

**Eyebrow:** FAQ

**H2:** Frequently asked questions

**Side copy:** Cost, timeline, ownership, and compliance, answered here rather than on a call.

**Button:** Tell us what you're building

> Two questions come out: *"How do I hire trading platform developers?"* and *"I have an idea, where
> should I start?"* Both are search-engine questions, not buying questions, and they belong in a
> blog post. Three go in, covering what procurement actually asks.

**1. How much does trading platform development cost?**
It depends on the engagement model. Time & Material bills the actual work performed on your project.
Fixed Price sets the whole cost upfront once requirements are documented. Outstaffing bills a
monthly rate per engineer. A fixed-price Discovery or System Design phase is also available before
committing to either. `[NEEDED: add the order-of-magnitude band here too, if §9 publishes one.]`

**2. How long does it take to build a trading platform?**
An MVP typically takes three to four months, and the range widens quickly with the number of venues,
asset classes, and regulatory regimes in scope. Tell us what you're building and we'll give you a
figure for your case rather than an average.

**3. Which brokers have you integrated, and what went wrong?**
Shipped interim answer: *"We keep a running account of what we've integrated and what surprised us.
Tell us which venues you're looking at and we'll walk through the ones closest to your build."*
`[NEEDED: the honest list — shipped, not evaluated, not read about. Then one real gotcha each. The
drafted examples in EXPERTISE-PROOF are IBKR's daily gateway restart and message pacing limits, and
Alpaca's fractional-share order-type restrictions and overnight corporate-action processing.
Confirm both before publishing, and link to the engineering notes page.]`

**4. Who owns the source code?**
Shipped interim answer: *"Ownership and handover terms are set out in the agreement. Ask us to walk
through them before you sign anything."* `[NEEDED: legal. Say it plainly, including what the
handover contains and what happens if we stop working together.]`

**5. Which certifications do you hold, and which regulations have you worked under?**
Shipped interim answer: *"We'll tell you plainly what we hold and what we don't, and name the
regimes relevant to your case."* `[NEEDED: the real answer, including the parts that are "not
certified". See §7.]`

**6. Can you integrate with a third-party service?**
Yes: brokers, payment gateways, KYC providers, news and market data providers, crypto exchanges, and
whatever else your business case needs.

**7. Do you offer support after launch?**
Yes, either as an ongoing arrangement or on demand.

**8. Do you sign an NDA?**
Before the first call. We'll sign yours, or send you ours.

> **Update:** answers 3, 5, and 8 said "on the call" / "the first technical call," which assumed the
> first call is technical. It isn't — see the §0 and §8 update notes. Wording now promises the
> answer, not the answer on call one.

**9. Have you built a trading platform before?**
Yes. Four are described above, three of them under NDA. The engineering notes cover the parts we
can talk about in more detail.

---

## 12 / Contact (`#contact`)

**Eyebrow:** Contact

**H3:** Tell us what you're building

**Lede:** A work email and a couple of sentences is enough to start. We'll ask for the rest when we
reply.

### Process steps

1. **You write.** We reply within 24 hours to sign the NDA and set up the call.
2. **We talk it through:** a short call about what you're building — venues, asset classes,
   regulatory regime, timeline, and budget.
3. **Our team designs it:** a solution architect, a fintech analyst, and a designer where it helps —
   an architecture and integration outline, and an indicative range in writing.
4. **We start.** Contract signed and development underway within one to two weeks. MVP in three to
   four months.

> **Update:** step 2 said *"You talk to an architect."* The first call is a scoping conversation, not
> an architecture conversation — see the §8 update note. The architect and the written outline now
> show up at step 3, once there's a project worth putting a team on.

### Form

> Five fields and two checkboxes go down to two fields and one checkbox. Phone and company come
> out; we can ask on the reply, where the cost of asking is zero. The NDA checkbox comes out too:
> the hero, the contact steps, and the FAQ already promise an NDA before the call for everyone, so
> a checkbox for it didn't gate anything real. The privacy checkbox stays because it has to.

- **Field — Work email** *(required)*
  - Error: We need an email we can reply to.
- **Field — What are you building?** *(required, textarea)*
  - Error: A sentence or two is enough.
- **Checkbox — Privacy Policy** *(required):* I agree to the Privacy Policy
  - Error: Tick this so we're allowed to reply.
- **Submit button:** Tell us what you're building
- **Under the button:** We reply within 24 hours.
- **Success message:** Thanks. We'll reply within 24 hours.

---

## 13 / Footer

- Logo alt: Itexus
- **Copyright:** © 2013–2026 Itexus. Trading platform development.
- **Link:** Privacy Policy

---

## Open inputs

Everything marked `[NEEDED]` above, gathered in one place and ordered by how much it holds up.

| # | Input | Who | Blocks |
|---|---|---|---|
| 1 | Real or anonymised case-study metrics | Delivery leads, legal | §3 — and the credibility of every other section |
| 2 | Certifications held and not held; regulatory regimes shipped under | Management, legal | §7, FAQ 5 |
| 3 | Engineer sign-off on the 12 capability second lines and the four failure modes | Engineering | §5, §6 |
| 4 | Honest broker list: shipped, versus evaluated, versus read about | Engineering | §6, FAQ 3 |
| 5 | Source-code ownership and exit terms | Legal | §7, FAQ 4 |
| 6 | Headcount, locations, timezone overlap; cleared client logos | Ops, marketing | §2 |
| 7 | Whether to publish a cost band, and what it is | Management | §9, FAQ 1 |
| 8 | Whether to offer the paid-discovery refund | Management | §8 |
| 9 | One testimonial about the platform working, not the team working | Account management | §10 |
| 10 | Data residency options and pen-test practice | Engineering, ops | §7 |

**The rule that governs all ten:** no invented numbers, including the plausible ones. A single
fabricated metric, caught on the call, takes down everything real on the page with it.
