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

**Subhead:** Low-latency trading systems for brokers, hedge funds, exchanges and fintech
companies—from FIX connectivity and market data infrastructure to risk controls, KYC/AML and
web and mobile trading terminals.

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

**01 — Build** *(New platform, from scratch)*
A strategy, a licence, or a client base already exists. The platform doesn't. We take it from
discovery and architecture through broker and market-data selection, order management, risk
controls, web and mobile terminals, and KYC/AML.

**02 — Modernize** *(An existing platform that caps what you can add)*
It runs, capped by a legacy vendor, an unsupported stack, or latency in the hot path. We audit the
current system, replace the execution and market-data layers a slice at a time, and migrate data
without taking trading offline.

**03 — Integrate** *(One component into a stack you already run)*
The platform exists; you need something wired into it. FIX and proprietary gateways, broker and
exchange APIs, market data and news feeds, payment and KYC/AML providers, portfolio and reporting,
scoped as a project or delivered by engineers embedded in your team.

**Footer link:** Not sure which one you're in? Describe the situation and we'll tell you which path
fits → (`#contact`)

> **Update:** cards 01 and 02 both opened with the same "X, Y, or Z [verb]s a consequence" rhythm —
> a list of three examples folded into one clause that ends on a tail (`and no platform yet` /
> `limits what you can ship next`). That construction, and its short-punchy-tail cousin, turned out
> to repeat across most of this page's numbered cards; see the update notes in §5 and §6 for the
> full sweep. Fixed here by giving each card its own shape instead of the shared template: 01 splits
> into two short declaratives, 02 moves its triad after a colon.

> **Update:** a code-review of that fix (run after PR #8 merged) flagged that 02's "Something is
> capping what you can ship next: [triad]" fix was itself a vague-subject-then-reveal construction —
> the same category of problem, just relocated to the front of the sentence instead of the end.
> Rewritten again as a single clause ("It runs, capped by...") that states the cause without a
> placeholder subject or a colon-reveal.

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
are the ones showing an order whose state is uncertain. Showing a cancelled order that actually
filled turns a UI bug into a support escalation.

**5. Market Data Storage**
A multi-source store with historical intraday data for equities, futures, FX, and options. Budget
for entitlements early: per-user reporting, redistribution licensing, and non-display charges add
up before the vendor contract puts a number on them.

**6. Trading Algorithms**
We implement your strategy and can add a no-code builder with parameter checks and safeguards. Those
checks do most of the work. Without a pre-trade guardrail, a market order on an illiquid symbol at
the open can fill well away from the last print.

**7. Strategy Builder**
A visual builder and a code editor for custom indicators and algorithms. One engine runs both the
backtest and the live strategy, because two separate engines drift apart over time.

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
FINRA 4511 set the retention expectations, and CAT requires industry members to keep business clocks
within 50 ms of NIST, with a one-second allowance where a clock is used only for manual order events.
Retrofitting any of this later is a rewrite.

> **Update:** the original line stated the 50 ms threshold as universal. Verified against the CAT
> NMS Plan FAQ: 50 ms of NIST applies to Industry Members' business clocks specifically (with a
> one-second allowance for clocks used solely on Manual Order Events); Participants — exchanges and
> FINRA — are held to 100 microseconds. This page's readers are building as industry members, so the
> 100 µs figure is left out as noise; "industry members" is the qualifier that keeps the sentence
> from being falsely universal.

**11. Paper Trading**
Simulated trades under live market conditions with no money at risk. Naive simulators are optimistic:
they fill at the touch, ignore queue position, and never partial-fill. Traders who practice against
one and then trade for real get results that don't match, and the platform takes the blame for a
gap the simulator created.

**12. Other Features**
Portfolio management, FIX gateways, and scalable matching components. Corporate actions cause more
trouble here than their profile suggests: a split, a spin-off, or a symbol change touches positions,
cost basis, open orders, historical charts, and the tax lot ledger all at once. Most data models
aren't built to update all of those together.

> **Update:** six of the twelve second lines (4, 5, 6, 7, 11, 12) shared the same closing move — a
> setup clause followed by a short tail revealing that someone finds out, gets surprised, or gets
> blamed once it's too late (`the user only finds out once it has` / `Nobody notices until...` /
> `is a support ticket that becomes a complaint`). That's the same device as the §4 path-card fix,
> just running underneath most of this grid. Rewritten to state the mechanism and stop, rather than
> stage a reveal. Cards 1, 2, 3, 8, 9, 10 were checked against the same test and left alone — their
> closing lines are specific technical claims (a named protocol quirk, a named bias, a named
> statute), not a generic "and then everyone finds out" beat, so they don't read as templated.

> **Update:** a code-review of that fix (run after PR #8 merged) found the replacements had their
> own problems. Card 4's "Show a cancelled order..." read as an instruction to the reader on a fast
> skim rather than a description of system behavior — rewritten as a gerund-subject sentence
> ("Showing... turns...") to remove the imperative reading. Card 5 had drifted into near-duplicating
> §6's "Market-data entitlements arrive as a bill" card almost word for word ("...are all
> contractual... don't show up in an API doc" vs. "...are all contractual... don't appear in an API
> doc") — reworded around a different idea (underestimating cost, not doc-coverage) to stop
> duplicating that card. Card 6 had the same reader-imperative problem as card 4 ("skip the
> pre-trade guardrail, and...") — rewritten as a conditional ("Without a pre-trade guardrail...").
> Card 11 had both problems at once: the imperative "Practice against one, then trade for real,
> and..." *and* a "[claim], not [noun]" tail duplicating the affirmation-cutoff card's "not a
> back-office SLA" further down in §6 — rewritten as a single declarative sentence with a different
> closing shape. Card 12's "Most data models aren't built for that" left "that" without a clear
> referent — changed to "built to update all of those together" so the pronoun points at the five
> named items, not the whole prior clause.

> **Update:** a second-round code review found this fix's own problems. Card 5's rewrite reworded
> only the tail of its sentence — the shared subject clause ("per-user reporting to the exchange,
> redistribution licensing, and non-display fees are...") was still verbatim identical to §6's
> "Market-data entitlements arrive as a bill" card, so the duplication it was meant to fix wasn't
> actually gone. Shortened to "exchange and redistribution fees," which drops the exact fee-type
> enumeration from this card (it stays precise, unchanged, in the §6 engineering note) so the two
> cards no longer share a repeated clause.

> **Update:** a third-round review caught that the previous fix went too far — dropping to "exchange
> and redistribution fees" lost a real, distinct cost category (non-display fees) rather than just
> the duplicated phrasing, and recast "per-user reporting to the exchange" as generic "exchange
> fees," understating what a prospect should actually budget for. Restored all three fee categories
> with different wording and a different sentence tail than §6's card ("add up before the vendor
> contract puts a number on them" vs. "are all contractual, and none of them appear in an API doc"),
> so the two cards stay factually consistent without sharing a repeated clause.

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
until the next reconciliation run catches them.

> **Update:** this card's original rewrite ("...stay wrong until somebody reconciles them" → "...go
> wrong at the same moment") shipped without an Update note, unlike every other edit in that pass —
> caught by a post-merge code review. The rewrite had also quietly dropped real information: "go
> wrong at the same moment" only restates that the error and the race condition are simultaneous
> (nearly tautological), losing the original's point that the wrong state *persists* until someone
> runs a reconciliation. Restored that, worded differently from the pre-PR original ("the next
> reconciliation run catches it" instead of "somebody reconciles them") so it isn't a plain revert.

> **Update:** "catches it" didn't agree with the plural "the position and cash" — a second-round
> code review caught the mismatch. Changed to "catches them."

**Market-data entitlements arrive as a bill**
Per-user reporting to the exchange, redistribution licensing, and non-display fees are all
contractual, and none of them appear in an API doc. Scoping market data as an integration task
misses the commercial negotiation underneath it, which is usually where the cost sits.

**The affirmation cutoff on trade date**
US equities have settled T+1 since May 2024, and SEC rules expect allocations, confirmations, and
affirmations completed as soon as technologically practicable on trade date. Missing that window
alone doesn't fail a trade, but missing same-day affirmation compresses exception resolution and
increases settlement-failure risk. It's a build requirement now, not a back-office SLA. The UK, EU
and Switzerland reach the same point in October 2027.

> **Update:** "miss the window and the trade fails" overstated a policies-and-procedures standard as
> a hard deadline. The SEC rule requires broker-dealers to have policies reasonably designed to
> complete affirmations as soon as technologically practicable on trade date — missing it raises
> settlement risk, it doesn't deterministically fail every trade. `[NEEDED: confirm the rule number
> (believed to be Rule 15c6-2) against a fetchable primary source before naming it explicitly on the
> page — sec.gov returned 403 to automated fetches this session.]`
>
> **Update:** "unaffirmed trades are the ones that fail to settle" still read as a direct,
> near-universal causal claim — the same overstatement the update above already flagged for the
> sentence before it, just restated. Replaced with the hedged version: affirmation failure
> compresses the exception-resolution window and raises settlement-failure risk, not guarantees it.
> "What used to be a back-office nuisance is now an engineering deadline" is cut too — a nostalgia/
> contrast construction ("used to be X, now Y") that reads templated regardless of whether the claim
> underneath it is accurate. Replaced with a direct statement of the same point.

> **Update:** that rewrite deleted "Missing that window" and left "That alone doesn't fail a trade"
> with a dangling antecedent — "That" read as pointing at the SEC expectation just stated, not at
> missing it, which is nonsensical (an expectation can't fail a trade). Caught independently by two
> passes of a post-merge code review. Restored "Missing that window alone doesn't fail a trade" so
> the pronoun has something to point at.

> **Update:** restoring that antecedent left two consecutive sentences both starting with "Missing"
> — an accidental stutter, caught in a second review round. Joined with "but" into one sentence
> instead of two, keeping the exact wording of both clauses.

**Average-price rounding breaks reconciliation**
Recomputing `AvgPx` client-side from individual fills, instead of using the value the counterparty
sent, introduces rounding drift measured in fractions of a cent. Across a full day of fills, that's
enough to break end-of-day reconciliation.

> **Update:** rewritten — the original was a two-sentence "quietly-wrong-until-someone-notices" beat
> (`the number drifts... Nobody notices until the end-of-day file doesn't match`), the same reveal
> device flagged across §4, §5, and the other three cards in this section. States the mechanism and
> the consequence directly instead.

> **Update:** that rewrite introduced "a few hundredths of a cent per fill" — a specific figure with
> no source, caught by a post-merge code review against this file's own rule (see "The rule that
> governs all nine" near the Open Inputs table): "no invented numbers, including the plausible
> ones." Reverted to "measured in fractions of a cent," which is vague but not fabricated — the
> same honesty level as the pre-PR wording, kept alongside the non-reveal sentence structure.

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
| **Standards we work to** | `[NEEDED: e.g. ISO 27001 practices, OWASP ASVS. Say "work to" where we're uncertified.]` |
| **Regulatory regimes we've shipped under** | `[NEEDED: name them. MiFID II, FINRA, MiCA, FCA — whichever are true. This is the single most valuable line in the section and a competitor already leads with theirs.]` |
| **Compliance work we've delivered** | PCI DSS-compliant ecosystem for Coinstar. KYC/AML onboarding, sanctions screening, and audit trails across the trading platforms above. |
| **Data residency** | `[NEEDED: which regions we can host in]` |
| **Secure development** | `[NEEDED: code review, dependency scanning, pen-test cadence and who runs it]` |
| **Paperwork** | NDA and DPA signed before the first call. |
| **Source code and exit** | You own the IP and the source code. Ownership transfers on payment, or from day one when the engagement starts with a deposit. |

> **Update:** the **Certifications we hold** row is cut — it invited a question the page would
> rather not open while unanswered, and nothing forced it to ship before the section did. If a real
> certifications list becomes available, it can come back as its own row. **Source code** is answered
> and no longer split from **If we part ways** — owning the IP and code from day one (or on payment)
> largely *is* the exit answer; a separate notice-period/handover-scope line is a future addition, not
> a blocker.

---

## 8 / The first step (new)

**Eyebrow:** What happens next

**H2:** A short call first, then a team on your problem

**Lede:** The first conversation is short and it's about your project. If there's a fit, we return
with an architecture outline, integration assumptions, and an indicative range.

> **Update:** the previous lede described the process without naming what comes back. This version
> names the three things the visitor actually receives, which is a preview of the offer block that
> follows it rather than a description of a process.

**The first call**
Thirty to forty-five minutes. What you're building, where it starts, and the constraints you're
working under: venues, asset classes, regulatory regime, timeline, and the shape of the budget. We
sign the NDA before it. There are no slides.

**Then our engineers take it**
We put a team on it: a solution architect, a fintech analyst, and a
designer where design matters. Over one to two weeks of workshops they work through feasibility, the
integrations you'd need, a high-level architecture and stack, and a workload and cost estimate. You
get that back in writing with its assumptions stated, and where it would help you decide, an
interactive prototype you can click through or look-and-feel screens of the real product.

**Why it's shaped this way**
The first call is about your project. Once there's a fit, the people who'd actually
build it — architect, analyst, designer — do the deeper work together, so what comes back reflects
real project experience. And since the person we're speaking with often isn't the one who signs off,
what matters most is giving you something solid to bring into that next conversation.

**Button:** Tell us what you're building

**Risk-reversal line:** Both are free and carry no obligation. The write-up is yours to use whether
or not you hire us.

**Handoff line, into §9:** When guessing at scope is the expensive option, the next step is a
fixed-price Discovery or System Design phase.

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

> **Update:** "Then our engineers take it" and the handoff line now match
> `stage.itexus.com/how-we-work/`, which describes this exact step as a free initial consultation:
> one to two weeks of workshops (feasibility, integration analysis, high-level architecture and
> stack, workload/cost estimate) ending in written project documentation and a proposal, and states
> the Discovery/System Design phase is for when the client "has only a high-level idea or the project
> is complex." Both details are folded in without changing the two-step framing above.

> **Update:** that sync introduced a 13-word clause ("the idea is still high level, or the project
> is complex enough that") duplicated verbatim in both the handoff line above and the §9 Discovery
> card — caught by a post-merge code review. Trimmed from the handoff line, which now just states
> the trigger ("guessing at scope is the expensive option") and lets the Discovery card below it
> carry the full reasoning.

---

## 9 / How we work (`#engagement`)

**Eyebrow:** How We Work

**H2:** Engagement models

**Discovery / System Design** *(fixed price, before any of the models below)*
We recommend this when the idea is still high level, or the project is complex enough that the
scope has to be worked out before it can be priced. It ends in requirements at the user-story level,
a worked-through architecture, and a scope broken into a phased plan. Where the project calls for
it, that also produces a clickable prototype and screen-by-screen UI design.

**01 — Time & Material (Efficient Hours)** *(badge: Recommended)*
*Agile with budget control.* Delivered in two-week sprints with a demo at the end of each one, so you
can change direction as you learn. A project manager holds scope, risk, and budget, and reports cost
and progress every week. You pay for the actual work performed on your project.

**02 — Fixed Price**
Requirements, price, and timeline are documented and signed before work starts, and you pay in
stages against milestones. It suits a scope that's already well defined and unlikely to move: expect
a longer analysis phase up front, a risk buffer built into the price, and any change to go through a
contract addendum.

**03 — Outstaffing**
*Development team as a service.* We put forward candidates who match your requirements; you
interview them and decide who joins. They work on your tasks under your own management, on a
development environment we set up to fit your infrastructure. Billed at a pre-agreed monthly rate
per engineer, and you can scale up or down as the workload moves.

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

> **Update:** all three model descriptions and the Discovery card now match
> `stage.itexus.com/how-we-work/` — Time & Material gets the weekly-reporting PM the source page
> makes central to the model; Fixed Price gets milestone payments plus the source's own stated
> tradeoffs (longer analysis phase, risk buffer in the price, changes go through an addendum);
> Outstaffing is corrected from "vetted engineers join your team" to what the source actually
> describes — Itexus sends CVs, the client interviews and decides who joins.
>
> **The billing sentence in model 01 was deliberately left as "the actual work performed on your
> project."** The source page states a stronger claim — "only efficient hours within the agreed
> estimates are billed, inefficient work is not billed" — but that's the same cap the previous update
> above removed on the grounds that it isn't one we actually guarantee. Re-litigated this round;
> the call stands.
>
> The lede also changed from the earlier "no invented figures" framing (about our own copy process)
> to one built from the source page's actual pitch — matching the model to requirements firmness and
> desired involvement.

> **Update:** the /how-we-work/ sync above introduced two instances of the same rhythmic pattern
> flagged and fixed across §4, §5, and §6 — the Discovery card stacked two three-item lists back to
> back (requirements/architecture/sprints, then mockups/prototype/design), and Fixed Price used the
> "X, Y, and Z, so [consequence]" shape. Fixed the same way: the Discovery card drops the redundant
> "UI mockups" item (a clickable prototype already implies mockups were made) so the second list
> isn't a full triad; Fixed Price is restructured conclusion-first with its three specifics after a
> colon instead of building to a "so" tail.

> **Update:** a post-merge code review found two more issues. First, the Discovery card's "a scope
> split into sprints" only describes how Time & Material delivers — Fixed Price bills by milestone,
> Outstaffing has no sprint structure at all — but Discovery sits above all three models and
> shouldn't promise a delivery shape only one of them uses. Changed to "a scope broken into a phased
> plan," which holds for any of the three. Second, Outstaffing's "You interview candidates we put
> forward" (from the earlier /how-we-work/ sync) dropped any sense that Itexus screens candidates
> before forwarding them — it now reads as "we forward CVs, you do all the filtering." Restored with
> "candidates who match your requirements," which mirrors the source page's own wording ("Itexus
> sends CVs of the candidates fitting the requirements") without re-adding the word "vetted" this
> repo's PR #8 deliberately removed as overclaiming.

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
Fixed Price sets the whole cost upfront once requirements are documented, with a risk buffer built
into the price. Outstaffing bills a pre-agreed monthly rate per engineer. A fixed-price Discovery or
System Design phase is also available before committing to either. `[NEEDED: add the
order-of-magnitude band here too, if §9 publishes one.]`

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
You own the IP and the source code. Ownership transfers on payment, or from day one when the
engagement starts with a deposit. See §7.

**5. Can you integrate with a third-party service?**
Yes: brokers, payment gateways, KYC providers, news and market data providers, crypto exchanges, and
whatever else your business case needs.

**6. Do you offer support after launch?**
Yes, either as an ongoing arrangement or on demand. We handle second- and third-line support:
monitoring production servers and logs, installing updates, fixing what can be fixed without
touching code, and releasing patches for what can't. First-line user support is usually run by the
client.

**7. Do you sign an NDA?**
Before the first call. We'll sign yours, or send you ours.

> **Update:** answers 3 and 7 said "on the call" / "the first technical call," which assumed the
> first call is technical. It isn't — see the §0 and §8 update notes. Wording now promises the
> answer, not the answer on call one.
>
> **Update:** the certifications question (formerly #5, *"Which certifications do you hold, and
> which regulations have you worked under?"*) is cut along with its §7 row — see the §7 update note.
> Question #4's answer is now the real one rather than a "shipped interim" placeholder, since §7's
> source-code row is answered. It also carried the FAQ's only link into §7, now re-homed here.
>
> **Update:** answers 1 and 6 now match `stage.itexus.com/how-we-work/` — the cost answer picks up
> Fixed Price's stated risk buffer, and the support answer replaces the vague "ongoing or on demand"
> with the source page's actual three-level model (Itexus runs 2nd/3rd-line; clients typically run
> 1st-line call-center support themselves).

> **Update:** replacing "ongoing or on demand" also silently narrowed the promise — the new answer
> only describes a standing 2nd/3rd-line arrangement, with no mention that ad-hoc, non-contractual
> support is available. Caught by a post-merge code review. Restored the opening "either as an
> ongoing arrangement or on demand" line ahead of the 2nd/3rd-line detail, so the answer keeps both
> the old promise and the new specificity instead of trading one for the other.

**8. Have you built a trading platform before?**
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
3. **Our team designs it:** one to two weeks of workshops with a solution architect, a fintech
   analyst, and a designer where it helps. You get an architecture and integration outline, and an
   indicative range in writing.
4. **We start.** Once you've approved the budget, scope, and architecture, and the contract is
   signed, development starts. MVP in three to four months.

> **Update:** step 2 said *"You talk to an architect."* The first call is a scoping conversation, not
> an architecture conversation — see the §8 update note. The architect and the written outline now
> show up at step 3, once there's a project worth putting a team on.
>
> **Update:** step 3 now carries the one-to-two-week workshop figure from
> `stage.itexus.com/how-we-work/`'s free-consultation description (see the §8 update note). Step 4
> previously read "Contract signed and development underway within one to two weeks," which had
> quietly repointed that same 1–2 week figure at time-to-contract — a claim the source page doesn't
> make. It only says the project starts once budget, scope, and architecture are approved and the
> contract is signed, so step 4 now says that instead.
>
> **Update:** two issues from that pass, caught by a post-merge code review. Step 3's rewrite here
> and the HTML had drifted apart — the shipped page dropped the em dash/comma construction below in
> favor of two shorter sentences, but this doc kept the old phrasing, so the two files disagreed
> with no record of why. Synced to match the shipped page. Step 4 was also missing a comma before
> "and the contract," letting "architecture and the contract" briefly misread as one list item
> before "is signed" forces a re-parse — added.

> **Update:** step 3's new sentence had the same missing-comma problem step 4 was just fixed for —
> "an architecture and integration outline and an indicative range" briefly misreads as a run-on
> list. Caught in a second review round. Added the comma.

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
| 2 | Regulatory regimes shipped under | Management, legal | §7 |
| 3 | Engineer sign-off on the 12 capability second lines and the four failure modes | Engineering | §5, §6 |
| 4 | Honest broker list: shipped, versus evaluated, versus read about | Engineering | §6, FAQ 3 |
| 5 | Headcount, locations, timezone overlap; cleared client logos | Ops, marketing | §2 |
| 6 | Whether to publish a cost band, and what it is | Management | §9, FAQ 1 |
| 7 | Whether to offer the paid-discovery refund | Management | §8 |
| 8 | One testimonial about the platform working, not the team working | Account management | §10 |
| 9 | Data residency options and pen-test practice | Engineering, ops | §7 |

**The rule that governs all nine:** no invented numbers, including the plausible ones. A single
fabricated metric, caught on the call, takes down everything real on the page with it.

> **Update:** two rows resolved and came out — certifications held/not held (the §7 row and FAQ 5
> both cut; see their update notes) and source-code ownership (§7 and FAQ 4 both now carry the real
> answer). Row 2 narrowed from "certifications and regimes" to regimes only.
