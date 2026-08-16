# Trading Landing — New Page Plan (v4)

Outline stage. Sections, what each one contains, and what job it does. Copy is directional here,
not final — the next pass writes the actual strings.

Built from: [GPT_Conversion verdict.md](../GPT_Conversion%20verdict.md) (CRO audit of the live page),
[CONVERSION-RESEARCH.md](CONVERSION-RESEARCH.md) (offer mechanics), [BUYER-EVALUATION.md](BUYER-EVALUATION.md)
(who reads it and how), [EXPERTISE-PROOF.md](EXPERTISE-PROOF.md) (how to prove domain competence),
[PAGE-COPY.md](PAGE-COPY.md) (redesign brief + locked brand system), [PAGE-COPY-REVIEW.md](PAGE-COPY-REVIEW.md)
(v3 copy as shipped), [DESIGN-SYSTEM.md](DESIGN-SYSTEM.md) (measured tokens).

---

## 1. What the four research docs agree on

Four documents written from different angles converge on the same five things. That convergence is
the strongest signal we have about what to change.

| # | Finding | Said by |
|---|---|---|
| 1 | **Proof is placeholder or absent.** Case studies describe features; the stats on v3 are literally `00.0 ms`. The buyer's #1 question is "have you built *this* before" and the page answers with a feature list. | all four |
| 2 | **The CTA misreads the buying stage.** "Get a proposal" implies the visitor has a spec — only ~20% do. What he wants is a bounded technical conversation with a named architect, and a document afterwards. | BUYER-EVAL §5, CONVERSION §5, GPT §5 |
| 3 | **No compliance / security / IP posture anywhere.** For brokers and exchanges this is a hard qualification gate, not a nice-to-have. Its absence is noticed. | BUYER-EVAL #3/#8, CONVERSION §3, GPT §1 |
| 4 | **The page never names a risk.** Naming the hard parts before the buyer does is the single clearest operator-vs-vendor signal, it needs no client permission, and no competitor does it. | EXPERTISE-PROOF §0, BUYER-EVAL #4 |
| 5 | **The page reads as a catalogue, not a journey.** Overlapping capability sections, generic SEO FAQs, 145 links, ~14,000px on mobile. Target is 35–45% shorter with earlier specificity. | GPT §3, CONVERSION §6 |

The one-line version, from BUYER-EVALUATION: the visitor is **not a customer, he's an internal
advocate assembling a defensible recommendation.** Every section below is judged on whether it gives
him something he can lift into a slide.

## 2. Where the docs conflict — decide before writing copy

**A. Which hero.** Three different H1s are in play:

- PAGE-COPY.md declares the hero **locked and out of scope**: *"Trading platforms built by people who have shipped them before."*
- v3 actually shipped: *"Build a Trading Platform Around Your Execution Logic"* (the GPT verdict's suggestion).
- BUYER-EVALUATION §3 rates the *locked* version as the page's best-performing moment — it passes the 5-second "specialist or generalist?" test.

Recommendation: **go back to the locked "shipped them before" hero.** It answers the buyer's actual
first question; the v3 line describes an outcome the buyer hasn't asked for yet. Needs your call
before section 1 copy is written.

> **Update:** shipped as the locked hero, then replaced again after review — "Trading platforms
> built by people who have shipped them before" read too much like AI-templated copy. The current
> hero in page-v4.html and PAGE-COPY-V4.md is *"We've built trading platforms before. We can build
> yours."*

**B. Buyer Variant B is under-served.** BUYER-EVALUATION §1 identifies two distinct visitors — build-
from-scratch, and *bolt an investing module onto an existing fintech app*. Variant B buys capacity +
a missing domain skill, and the integration surface is his whole risk. The page's Integrate card is
one of three, buried at position 3. If Variant B is a real share of inbound, it deserves equal
weight, and the plan below assumes it does.

**C. Guarantee and scarcity.** CONVERSION-RESEARCH pushes hard for both. Scarcity is fabricated
unless it's true and maintained; I'd **skip it** and take the guarantee only in a form we'd honour.
Your call — noted in section 9 below.

---

## 3. Proposed section order

| # | Section | Status | Job it does |
|---|---|---|---|
| 0 | Header / sticky CTA | ✍️ | One CTA verbatim, everywhere |
| 1 | Hero | ✍️ | Pass the 5-second specialist test |
| 2 | Facts strip | 🆕 | Fill his spreadsheet columns |
| 3 | Case studies | ⛔ blocked | Answer "have you built this before" |
| 4 | Where you're starting | ✅ keep | Fork the buyer by situation |
| 5 | Capabilities | ✍️ | Vocabulary check + name the hard part |
| 6 | What usually goes wrong | 🆕 | Operator, not vendor — the differentiator |
| 7 | Security, compliance, IP | 🆕 | Clear the qualification gate |
| 8 | The first step (offer) | 🆕 | Give him something small he can say yes to |
| 9 | How we work | ✅ keep | Map to his procurement process |
| 10 | Testimonials + awards | ✍️ | Third-party validation |
| 11 | FAQ | ✂️ cut + add | Objection dump |
| 12 | Contact | ✍️ | Convert, at low friction |
| 13 | Footer | ✅ keep | — |

Legend: ✅ keep as-is · ✍️ rewrite · 🆕 new · ✂️ cut down · ⛔ blocked on missing data

---

## 4. Section detail

### 0 — Header / persistent CTA
**Goal:** keep one conversion path visible without changing what it says mid-page.
**Contains:** logo, nav (Services · Where to Start · Case Studies · Hire Developers · About Us),
one button.
**Change:** the button, the hero CTA, the mid-page CTA and the form button currently say four
different things (*Contact Us · Get a proposal · Get a proposal · Send*). Pick **one named
deliverable** and repeat it verbatim in all four places. Working candidate: **"Talk to a trading
architect"** — the docs agree this is the strongest existing line on the page and it's currently
mid-page, in the weakest position.

### 1 — Hero
**Goal:** in five seconds, prove this is a trading specialist rather than a general agency with a
trading landing page. That is the only question being asked here.
**Contains:** eyebrow · H1 (decision A above) · subhead carrying real vocabulary (FIX gateways,
market-data fan-out, KYC/AML, audit trails) · primary CTA · secondary "See the platforms we've
built" · assurance line (24h reply, NDA first) · hero image (existing trading app screens).
**Note:** the vocabulary in the subhead is doing more work than the H1. Don't sand it down.

### 2 — Facts strip *(new, directly under the hero)*
**Goal:** the highest-leverage new element on the page. He reads by **field extraction** — he has a
comparison table open and is filling cells. Anything not liftable into a cell doesn't survive the
visit. Currently he has to email us to learn basic vendor-profile facts, which is friction at
exactly the stage where he's comparing rather than engaging.
**Contains:** one horizontal band of labelled facts, no prose —
4.9 on Clutch (40 reviews) · shipping since 2013 · 300+ projects · team size · HQ + delivery
locations + timezone overlap · NDA/DPA ready · MVP target 3–4 months · reply within 24h.
Plus 2–3 recognisable client logos if we have permission.
**Why here:** GPT verdict measured the current proof at ~12,000px down on mobile. Most qualified
visitors never see it.
**Needs from you:** headcount, locations, and which logos are cleared.

### 3 — Case studies
**Goal:** answer priority #1. This is the deepest read on the page (60–90 seconds) — he is hunting
for *one* project close enough to his own that he can cite it upward.
**Contains:** flagship (Coinstar, PCI DSS, $2.2B fintech) + three NDA cards, each carrying
**outcome metrics, not feature descriptions**: order round-trip latency, peak throughput, venue/broker
integration count, time to first live release, concurrent accounts, uptime, regulatory regime shipped
under, manual ops eliminated.
**Also:** pair one testimonial *directly with the case study it validates* instead of leaving all
five in a separate carousel.
**⛔ This is the blocker.** v3 ships visible placeholders (`00.0 ms`, `000 k/day`). A visitor sees
fake-looking numbers with no disclaimer. Nothing else on this page matters until these are real.
Anonymised and bounded is fine and needs no client sign-off:
*"European broker · 12 months · 40k accounts · sub-100ms order round-trip · FIX 4.4 to two prime brokers."*
**Needs from you:** real figures, even ranged. Until they exist, ship the cards with no stats rather
than with placeholders.

### 4 — Where you're starting (build / modernize / integrate)
**Goal:** route the buyer to his own situation before the capability list, which raises "they've
solved my specific problem before" without adding length. CONVERSION-RESEARCH rates this as already
correct and Hormozi-aligned.
**Contains:** three cards as currently written — no changes needed to the copy.
**One change:** if decision B goes the way I've recommended, **Integrate** gets weighted equal to
Build (Variant B is buying capacity + a domain skill, and the integration surface into his live
product is the entire risk). Consider promoting this section above the case studies so each buyer
lands on the case study that matches him — worth testing, not asserting.

### 5 — Capabilities
**Goal:** priority #2, the vocabulary check — and it's the page's current strongest asset. He skims
this for **absence**: two or three terms specific to his own project (options? FIX 4.4? margin?
multi-currency settlement?). A missing term signals louder than eleven present ones.
**Contains:** the 12 cards + 3 product screenshots, both kept in full (a previous version dropped the
screenshots and was called out).
**Change:** give each card a **second line naming the hard part**, per EXPERTISE-PROOF §J. This is
the cheapest credibility gain on the page. Example:

> *Order Management* — order types, time in force, leverage, stop-loss and take-profit — with the
> state machine that holds up when a cancel and a fill cross on the wire, when a replace is
> rejected, and when the session drops with an unacknowledged order outstanding.

Priority cards for this treatment: Order Management, Integration With Brokers, Trading Execution
Middleware, Market Data Storage, Backtesting, Paper Trading.
**Layout note:** if the second lines make 12 cards too heavy, move the tail into an accordion —
but don't cut any.

### 6 — What usually goes wrong *(new)*
**Goal:** priority #4 — *can they name the hard parts before I do?* This is the operator-vs-vendor
tell, it requires no client permission and no invented metrics, and EXPERTISE-PROOF's governing test
applies cleanly: a generalist agency cannot fake it in an afternoon.
**Contains:** a compact strip of 3–4 named failure modes, one line each, drawn from the 40 already
drafted in EXPERTISE-PROOF §2A. Candidates with the widest recognition:
cancel/fill race on the wire · market-data entitlement and non-display fees arriving as a surprise
bill · T+1 affirmation cutoff · reconciliation breaks from average-price rounding.
Ends in a link out: *"38 more, with what we do about each →"*
**Depends on:** a second surface — the **engineering notes page** proposed in EXPERTISE-PROOF §1.
Depth belongs there, not here; the landing page carries three small hooks that visibly lead
somewhere deeper. Scope that page separately.
**Needs from you:** an engineer to correct the drafted list and cut anything we can't stand behind.
Marketing edits for clarity and **cuts only** — nothing gets added downstream of the engineer.

### 7 — Security, compliance and ownership *(new)*
**Goal:** priority #3, plus the IP/exit question that BUYER-EVALUATION flags as *absent entirely*
and standard for procurement. For Level-3 buyers (~20%, arriving with an RFP) this section is a hard
qualification gate — if it's missing they may still send the RFP, but we start behind vendors who
published it.
**Contains:** a short factual band —
certifications held (and honestly, those not held) · regulatory regimes shipped under, named:
MiFID II / FINRA / MiCA / FCA as applicable · data residency options · secure SDLC and pen-test
practice · NDA/DPA readiness · **who owns the source code, and what happens if we part ways.**
**Tone rule:** an honest *"we work to X, we are not certified for Y"* outperforms silence. State
only what's true.
**Needs from you:** the actual certification and regime list. This is a management/legal input, not
something the page can be written around.

### 8 — The first step *(new)*
**Goal:** the offer. Right now there is no single named thing to say yes to, and the ask ("get a
proposal") is bigger and vaguer than what he's authorised to do. His realistic first move is an NDA
and a bounded technical conversation.
**Contains:** one named, scoped engagement with its contents stated —
*a 45–60 minute call with a named solution architect (not a salesperson), NDA signed first, agenda
published: your requirements → architecture sketch → integration options → risks → an indicative
range.* And critically, **what he receives afterwards**: a written summary, a one-page architecture
view, and an estimate with its assumptions listed.
**Why this shape:** he has to present to a committee we'll never meet. A vendor who hands him
board-ready material writes his slide for him — and gets recommended. A generic capabilities deck
makes him do that work and he resents it.
**Optional, your call (decision C):** a conditional guarantee — *"if the discovery architecture and
estimate aren't usable, we refund the discovery fee."* Currently a zero-competitors-have-it
differentiator. **Skip the manufactured scarcity**; in fintech, invented urgency costs more trust
than it buys.
**Adjacent asset:** the page currently offers **nothing to take away**, and his job output is a
document. A downloadable architecture/capability PDF — ungated, or email-only — travels into the
buying committee with our framing intact. Worth building even before the engineering page.

### 9 — How we work (engagement models)
**Goal:** priority #6 — mapped directly onto what his procurement can approve. Fixed price is often
the only model a board will sign for a first engagement.
**Contains:** the three existing models (Efficient Hours · Fixed Price · Outstaffing), unchanged —
both docs rate this section as already correct.
**Add:** an order-of-magnitude cost band with its conditions attached. He cannot open a board
conversation with "no idea," and absent a number from us he anchors on whichever competitor
published one. *"Integrations typically start at $X; full platforms $Y–Z depending on venues and
asset classes"* beats silence.
**Needs from you:** whether we're willing to publish a band at all.

### 10 — Testimonials and awards
**Goal:** third-party validation.
**Contains:** the 5 quotes as a real carousel (a static grid was explicitly rejected before), the
Clutch strip, and all 12 award badges in the marquee.
**Known weakness:** every quote praises *responsiveness and project management*; none says the
**system worked**. For a buyer whose fear is "the platform I recommended failed," that's the wrong
proof. Where possible source one quote about behaviour under load or through launch.
**Change:** move the strongest trading-relevant quote (the Risk Management Director, Investing Fund)
out of the carousel and pair it with its matching case study in section 3.

### 11 — FAQ
**Goal:** the objection dump. He comes here specifically for cost, timeline, IP, and NDA — nothing
else.
**Cut:** #8 *"How do I hire trading platform developers?"* and #7 *"I have an idea, where should I
start?"* — generic SEO questions that belong on a blog and dilute the buying-objection set.
**Keep:** cost · timeline · integrations · support · NDA · have-you-built-one-before.
**Add three:** who owns the source code and what happens at exit · which certifications and
regulatory regimes we've shipped under · **"Which brokers have you integrated, and what went
wrong?"** — one genuinely technical answer among the commercial ones, naming IBKR's daily gateway
restart and pacing limits, Alpaca's fractional-share restrictions, linking to the engineering notes.

### 12 — Contact
**Goal:** convert. He is judging *what happens if I fill this in* — if it reads like a lead form
routing to a salesperson, qualified evaluators leave and email a named person instead.
**Contains:** the 4-step process (which is good and stays) + a **shortened** form.
**Change:** current form is 5 fields + 2 checkboxes. Cut first contact to **work email + one open
field**, and either collect phone and detail on the first reply or split into a two-step form
(contact → detail revealed after step 1). Keep the existing microcopy tone — *"A sentence or two
about what you're building is enough"* — it measurably lowers perceived effort.
**Change:** the submit button and surrounding copy should promise the **architect conversation**,
matching section 8 and the header CTA word for word.

### 13 — Footer
No changes.

---

## 5. What gets removed

- Placeholder metrics — every instance, either replaced with real figures or deleted
- FAQ #7 and #8 (generic SEO questions)
- Three of the four different CTA wordings
- Three form fields + one checkbox from first contact
- Any remaining overlap between capability sections (GPT verdict flagged "Solutions We Develop /
  Must-haves / Solutions We Provide / Core Features" as four passes over the same ground)

Net: two new sections in, roughly equivalent length out. The page should not grow.

---

## 6. Blockers — none of these can be written from outside

Ordered by how much they hold up.

| # | Needed | Blocks |
|---|---|---|
| 1 | Real (or anonymised, ranged) case-study metrics | §3 — and by extension the credibility of everything else |
| 2 | Certifications held / not held, regulatory regimes shipped under | §7, one FAQ |
| 3 | Engineer review of the drafted failure modes | §6, capability second lines in §5 |
| 4 | Honest broker integration list — shipped vs evaluated vs read about | §6, one FAQ |
| 5 | Headcount, locations, timezone; cleared client logos | §2 |
| 6 | Decision on publishing a cost band | §9 |
| 7 | Decision on the guarantee | §8 |
| 8 | Decisions A (which hero) and B (Variant B weighting) above | §1, §4 |

Rule carried over from EXPERTISE-PROOF and worth restating: **no invented numbers, including
plausible-sounding ones.** One fabricated metric caught on the call destroys every real thing on
the page.

---

## 7. Locked — do not change

From [PAGE-COPY.md](PAGE-COPY.md) and [DESIGN-SYSTEM.md](DESIGN-SYSTEM.md):

- **Palette:** brand green `#25bb4d` / `#30d05a`, ink `#051320`, header `#3a5b5c`. No dark-mode/neon
  redesign — that was tried and rejected.
- **Type:** Heebo, self-hosted, weights 400/500/600. H1 40/48, H2 40/44, H3 24/28.8, body 14/19.6.
- **Tokens:** 16px card radius, 10px button radius, `0 4px 44px -9px rgba(0,0,0,.08)` card shadow,
  1312px content max-width.
- **Give every anchor an explicit colour** — the live site leaks browser-default `#0000ee` in 175
  places, visibly over the Coinstar logo.
- Testimonials must be a real carousel. All 12 award badges stay. All 3 capability screenshots stay.
- No stock candlestick/trading-floor imagery — a listed fast-cut trigger for this buyer.

---

## 8. Suggested build order

1. **Delete the placeholder metrics** (5 minutes, removes the worst liability on the page)
2. **Unify the CTA** to one named deliverable, four places (cheap, high leverage)
3. **Facts strip** (§2) — needs facts, not writing
4. **Capability second lines** (§5) + **failure-mode strip** (§6) — one engineer interview covers both
5. **Compliance/IP band** (§7) + FAQ surgery (§11)
6. **Offer section** (§8) + shortened form (§12)
7. **Real case-study metrics** (§3) whenever legal and the client relationships allow
8. **Engineering notes page** — separate scope, phased per EXPERTISE-PROOF §4
