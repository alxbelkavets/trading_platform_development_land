# Proving Trading-Domain Expertise — Asset Plan

What to add to the landing page, and to a dedicated engineering page it links to, so that a CTO
evaluating vendors concludes we have actually shipped trading systems rather than written about them.

Companion to [BUYER-EVALUATION.md](BUYER-EVALUATION.md) (who reads the page) and
[CONVERSION-RESEARCH.md](CONVERSION-RESEARCH.md) (offer mechanics). This document covers **proof of
competence** specifically — priority #4 in the buyer evaluation, *"can they name the hard parts
before I do,"* which the current page does not address at all.

---

## 0. The one structural insight

Three of our four case studies are under NDA. That blocks the obvious proof route — named clients,
outcome metrics, architecture of *their* system — and it is not a blocker we can engineer our way
past.

**But the strongest proof for a technical buyer isn't the client list. It's demonstrated knowledge
of the failure modes.** A vendor who can describe, unprompted, what happens when a cancel and a fill
cross on the wire has obviously been on the wrong end of it. That kind of content:

- requires no client permission
- requires no invented metrics
- cannot be produced by a marketing writer or a general-purpose LLM without an engineer in the loop
- is exactly what our buyer says he is looking for and cannot find

So the plan below is built almost entirely out of **domain knowledge we can publish freely**, with
NDA-safe case-study material layered on top wherever legal clears it.

The governing test for every asset here:

> **Would this be expensive for a competitor who has never built a trading system to fake?**

If a generalist agency could produce it in an afternoon with an LLM, it isn't proof. It's decoration.

---

## 1. Where the content lives

**Do not bolt all of this onto the landing page.** The page is already flagged as too long in
[GPT_Conversion verdict.md](../GPT_Conversion%20verdict.md). Depth belongs on its own surface.

| Surface | Purpose | Audience |
|---|---|---|
| **Landing page** (`/trading-platform-development/`) | Sell. Route. Three *small* proof hooks that visibly link somewhere deeper. | Everyone, 90-second scan |
| **Engineering page** (`/trading-platform-development/engineering/`) — proposed | Prove. Long, dense, interactive, no CTA pressure above the fold. | The evaluator who already believes we might be real and is now checking |
| **Takeaway artifacts** (PDF/print) | Travel into the buying committee | The 6–10 stakeholders we never meet |

Working title for the second surface: **"How trading systems actually break"** or **"The Engineering
Notes."** Avoid "Our Expertise" / "Why Choose Us" — the title itself is a slop tell.

### The three hooks on the landing page

Each hook is a small, high-signal element placed where the buyer's scan already stops
(per [BUYER-EVALUATION.md §3](BUYER-EVALUATION.md)):

1. **After the capability grid** — a strip titled *"The parts of this that usually go wrong"*, three
   named failure modes with one line each, then → *"38 more, with what we do about each."*
2. **Inside the Integrate card** (Section 02) — a broker logo row (IBKR, Alpaca, and the others we
   have actually integrated) → *"What each of these gets wrong, and how we work around it."*
3. **In the FAQ** — one genuinely technical question among the commercial ones, e.g.
   *"Which brokers have you integrated, and what broke?"* — answered honestly, linking out.

---

## 2. Asset catalogue

Ordered by proof-per-hour-of-effort. Each entry states what it proves, how it renders, and what we
need in order to build it truthfully.

### A. The Edge Case Ledger  ⭐ highest value, lowest risk

A filterable list of **~40 concrete edge cases** in order handling, market data, settlement, and
onboarding. Each entry is one card:

- **Trigger** — the exact condition
- **What a naive implementation does** — the bug
- **What it costs** — money, a support ticket, a regulator letter, a reconciliation break
- **How we handle it** — the actual mechanism
- **Where it bites** — which broker / venue / asset class

Filters: category (order · market data · settlement · corporate actions · onboarding · reporting),
broker (IBKR · Alpaca · generic FIX · crypto), severity.

Why it works: it is a **field-extraction artifact**, which is exactly how our buyer reads
([BUYER-EVALUATION.md §3](BUYER-EVALUATION.md)). He can copy three rows into his shortlist doc. It
also survives being skimmed — each card is independently valuable.

**Seed content — order edge cases.** These are real, publishable, and none require a client's
permission:

| # | Trigger | The bug |
|---|---|---|
| 1 | Cancel request and the final fill cross on the wire | Client sees `PendingCancel`, then `Filled`, and shows the user a cancelled order that actually executed. Position and cash go wrong until reconciliation |
| 2 | `OrderCancelReject` (35=9) arrives with `CxlRejReason=1` (unknown order) | Naive clients treat it as a transport error and retry, sending a second cancel for an order that is already done |
| 3 | Partial fills across multiple executions | `AvgPx` (6) recomputed client-side from fills instead of trusting `CumQty`/`AvgPx`, drifting by fractions of a cent, then failing reconciliation at end of day |
| 4 | `ExecType=D` (Restated) with `ExecRestatementReason` | Broker corrects a fill after the fact. Systems that treat executions as immutable never apply it |
| 5 | Cancel/replace chain: `ClOrdID` (11) vs `OrigClOrdID` (41) vs `OrderID` (37) | Keying order state on `ClOrdID` alone breaks the moment a replace is rejected and the chain forks |
| 6 | Replace rejected — which order is live, the old one or the new one? | Both assumptions are wrong somewhere; the correct answer depends on `OrdStatus` in the reject, and counterparties differ |
| 7 | `PossDupFlag=Y` (43) after a session recovery | Replaying a duplicate execution and double-counting the fill. Idempotency has to key on `ExecID`, not arrival |
| 8 | `PossResend=Y` (97) — an application-level resend, not a session one | Frequently conflated with tag 43. Different handling, and getting it wrong duplicates orders rather than executions |
| 9 | Sequence gap → `ResendRequest` (35=2) → `SequenceReset`/`GapFill` (35=4) | Engines that resend admin messages, or reset sequence numbers on reconnect when the counterparty did not agree to it, get logged out mid-session |
| 10 | Order sent, no ack, connection drops | The genuinely hard one. Did it reach the venue? Resolvable only by order-status request or drop-copy reconciliation on reconnect — never by resending |
| 11 | Time in force semantics: DAY across a session boundary, GTC across a corporate action, IOC vs FOK partial handling | GTC orders surviving a 1:8 reverse split at the un-adjusted price. Some venues cancel, some adjust, some do neither |
| 12 | Stop orders during a LULD pause or a limit state | Stop triggers on a print that occurs inside a halt auction, or on the reopening print, and fills far from where the user expected |
| 13 | Reg SHO Rule 201 short-sale circuit breaker active (−10% from prior close) | Short sells can only rest above the NBB. Orders that ignore this get rejected at the venue after the client already showed "working" |
| 14 | Fractional share orders | Restricted order types, no shorts, no extended hours at most brokers, and residual dust after a corporate action that nobody's ledger accounts for |
| 15 | Self-match / wash trade prevention rejects | Two of the platform's own users, or one user in two accounts, cross. Broker rejects; the platform has no explanation to show the user |
| 16 | Odd lots | Not protected quotes under Reg NMS Rule 611. UI showing the odd-lot NBBO as the tradeable price misleads the user |
| 17 | Extended-hours and after-hours sessions | Different order-type support, different liquidity, and `TimeInForce`/routing flags that must be set explicitly or the order rejects at 16:01 |
| 18 | Market orders on an illiquid symbol at the open | No pre-trade guardrail → fill 40% away from the last print → a support ticket that becomes a complaint |
| 19 | Duplicate `ClOrdID` after a client restart | Monotonic-counter schemes reset to zero. Venue rejects, or worse, accepts the second one against a stale order |
| 20 | Rate limit / pacing violation under a burst | The order that gets dropped is the cancel you needed most |

**Seed content — settlement, cash, and lifecycle:**

| # | Trigger | The bug |
|---|---|---|
| 21 | US equities settle **T+1** (since 28 May 2024); FX is T+2; crypto is instant; UK/EU/CH move to T+1 on **11 Oct 2027** | Multi-asset platforms with a single settlement assumption in the ledger |
| 22 | Affirmation/allocation cutoff on trade date | Miss it and the trade goes to a fail. The compressed T+1 window turned a back-office nuisance into an engineering deadline |
| 23 | Cash-account settled-funds tracking | Good-faith violations and free-riding under Reg T §220.8, and the 90-day cash-only restriction after three violations. Buying power must distinguish *settled* from *unsettled* cash — most naive ledgers do not |
| 24 | Pattern day trader: 4 day trades in 5 business days, \$25k minimum equity (FINRA 4210) | Enforced by the broker but experienced by the user in your UI. If you don't count day trades the same way the broker does, the user gets blocked with no warning |
| 25 | Reg T initial margin, maintenance calls, and intraday buying power | Two ledgers (yours and the broker's) drifting apart during a volatile session |
| 26 | Corporate actions: splits, reverse splits, dividends, spin-offs, symbol changes, mergers, delistings | Positions, cost basis, open orders, historical charts, and the tax lot ledger all have to move together. This is where most platforms discover their data model was wrong |
| 27 | Cost basis and wash sales (30-day window, across accounts) | 1099-B reporting that doesn't reconcile with the clearing firm's, discovered in January |
| 28 | Fails to deliver / buy-ins | Rare, but the flow has to exist somewhere in the platform or someone handles it in a spreadsheet |
| 29 | Reconciliation: positions, cash, and executions against the broker's end-of-day file | If the platform has no automated three-way reconciliation, it *has* a reconciliation process — it's a person, and they find breaks late |
| 30 | Clock synchronization | CAT requires industry members within 50 ms of NIST; MiFID II RTS 25 is far tighter for algorithmic flow. Audit trails with sloppy clocks are not audit trails |

**Seed content — KYC / KYB / onboarding:**

| # | Trigger | The bug |
|---|---|---|
| 31 | CIP identity verification fails on a legitimate user (address mismatch, thin file, recent immigrant, name transliteration) | Hard-fail flows lose real customers. The design question is the **step-up path and the manual review queue**, not the happy path |
| 32 | Sanctions/PEP screening false positives | Common name → hit against an OFAC SDN entry. Needs adjudication UI, a four-eyes process, and an audit record of *why* the analyst cleared it |
| 33 | KYB: beneficial ownership through layered entities (25% threshold plus the control prong) | An org chart, not a form field. Nested LLCs, trusts, and foreign parents break every "add UBO" UI built as a flat list |
| 34 | Ongoing monitoring and periodic re-KYC | Onboarding is not a one-time event. Risk-rating changes, document expiry, and re-screening on sanctions-list updates all need scheduled jobs and a case system |
| 35 | Tax documentation: W-9 vs W-8BEN, treaty rates, FATCA/CRS, 1099-B vs 1042-S | Non-resident onboarding that ignores this produces incorrect withholding, which is expensive and retroactive |
| 36 | GDPR erasure request vs AML retention obligation (typically 5 years post-relationship) | Directly conflicting requirements. The platform needs a documented answer before a regulator asks, not after |
| 37 | Suitability / appropriateness gating (FINRA 2111, Reg BI; MiFID II appropriateness for complex instruments) | Options approval levels, leverage eligibility, and knowledge tests are product logic, not a compliance afterthought |
| 38 | Audit trail completeness | Every state change, every override, every manual approval, immutably stored (SEC 17a-4 WORM-equivalent, FINRA 4511). Retro-fitting this is a rewrite |
| 39 | Vendor outage in the IDV chain | Onboarding stops. Does the platform queue, fail over to a second provider, or degrade to manual? |
| 40 | Market data entitlements and non-display fees | Per-user reporting to the exchange, redistribution licensing, and an audit that arrives with a bill. A cost line that surprises product teams |

> **Effort:** 2–3 engineer-days to write, 1–2 days to build the UI. Everything above is already
> drafted here — it needs an engineer to correct it, cut what we can't stand behind, and add the
> ones we hit that aren't listed.

---

### B. Broker Integration Matrix  ⭐ the un-fakeable one

A comparison table of every broker/venue/data vendor we have actually integrated. The first four
columns are public knowledge. **The last column is the proof.**

| Broker | Protocol | Sandbox fidelity | Reconnect / state recovery | What surprised us |
|---|---|---|---|---|
| **IBKR** | TWS/Gateway API (socket), FIX CTCI for institutional | Paper account, close to live | Open orders placed under a different `clientId` aren't visible to yours — only `clientId 0` sees TWS-manual orders | Daily gateway restart, ~50 msg/sec pacing limit, default ~100 concurrent market-data lines, `orderId` sequencing after reconnect |
| **Alpaca** | REST + WebSocket (`trade_updates`), OAuth; Broker API separate from Trading API | Paper environment; Broker API sandbox behaves differently from live | `client_order_id` gives true idempotency — use it or you will double-send | Fractional-share order-type restrictions, PDT enforcement timing, corporate actions applied overnight, journaling (cash/securities) in Broker API |
| *(each other broker we've shipped)* | | | | |

Rows to fill from real experience only. Candidates based on the market: Tradier, DriveWealth, Apex,
Saxo, LSEG/Refinitiv, Polygon, Databento, Coinbase Prime, Kraken, Fireblocks. **Leave out any we
haven't touched** — a padded matrix is detectable in one question on the call, and it costs more
than the row was worth.

Add a footnote that is itself a credibility move:

> *Broker APIs change. Everything above was verified on [date]; where it's now wrong, tell us and
> we'll fix the row.*

> **Effort:** half a day per broker, from an interview with the engineer who did the integration.

---

### C. C4 architecture set, with failure modes attached

Standard C4 (Context → Container → Component) for a **reference retail brokerage platform** — not a
client's system, a generic one we author, which sidesteps NDA entirely.

**A C4 diagram on its own is decoration.** Every competitor can generate one. What makes it proof is
the annotation layer:

- Each container carries a **"what usually goes wrong here"** note on hover/tap
- Each arrow is labelled with the **actual protocol and message type** — `FIX 4.4 NewOrderSingle
  (35=D)`, not "orders"
- Each boundary carries its **latency budget** and its **failure behaviour** (what happens when this
  link is down during market hours)
- A toggle for **"what changes if you self-clear"** vs **"introducing broker"** — a decision our
  Level-1 and Level-2 buyers genuinely don't know how to make

Levels worth building:

1. **L1 Context** — the platform, its users, and the eleven external systems it depends on (broker,
   market data, clearing, KYC vendor, sanctions screening, payments/ACH, tax reporting, CAT/regulatory
   reporting, custodian, notifications, and the client's existing core). The count alone is
   informative: most buyers underestimate it by half.
2. **L2 Container** — order gateway, OMS, risk engine, market-data fan-out, ledger, reconciliation,
   onboarding/case management, reporting, the user-facing apps.
3. **L3 Component, on the OMS only** — order state machine, ClOrdID chain manager, execution store,
   position keeper, pre-trade risk checks, drop-copy reconciler. One L3 done properly beats five done
   shallowly.

Also worth doing: a **deliberately naive version** of L2 — the architecture teams actually build
first — with the four things that will break it circled. Showing the wrong answer next to the right
one is a strong expertise signal and reads as generous rather than promotional.

> **Rendering:** hand-authored SVG or Mermaid `C4Context`. Mermaid is faster and stays editable;
> hand SVG gives us control over the annotation layer and the zoom transitions. Recommendation:
> **Mermaid for L1, hand-authored SVG for L2/L3** where the interaction matters.

---

### D. Animated sequence diagrams  ⭐ the "engaging" asset

This is where the interactivity budget should go. Six scenarios, each a self-contained player.

**Build them from real (sanitized) message logs, not from imagination.** A replay of an actual
session — timestamps preserved, identifiers scrubbed — looks different from a drawn diagram, and
technical readers can tell.

| # | Scenario | What it proves |
|---|---|---|
| 1 | **Cancel/replace race** — cancel sent, fill returns first, `OrderCancelReject` follows | We understand that order state is a distributed-systems problem, not a CRUD problem |
| 2 | **FIX session recovery** — gap detected, `ResendRequest`, `SequenceReset-GapFill`, duplicate execution suppressed on `ExecID` | Session-layer competence, which almost nothing on the public web explains well |
| 3 | **Partial fills across venues** — five executions, running `CumQty`/`LeavesQty`/`AvgPx`, the user's position updating | Correct execution accounting |
| 4 | **T+1 settlement timeline** — trade date through affirmation cutoff to settlement, with a fail branch | Post-trade literacy, which is where most "trading platform" vendors stop |
| 5 | **Onboarding with a step-up** — IDV soft-fail → document upload → sanctions hit → manual adjudication → approval, with the audit record written at each step | KYC as a system, not a vendor SDK call |
| 6 | **Broker disconnect mid-session** — reconnect, order-status request, drop-copy reconcile, divergence found and resolved | The scenario every experienced buyer has personally lived through |

**Interaction spec** (this matters more than the animation):

- **Scrub and step, not autoplay.** A play button, a timeline scrubber, forward/back by message,
  speed control. Autoplaying loops are decorative; a scrubber says "study this."
- **Two panes.** Left: the actors and arrows. Right: the raw message with tags, updating in sync.
  Clicking any tag explains it.
- **A state chip per actor** that visibly changes — `New → PartiallyFilled → PendingCancel → Filled`
  — so the reader watches the bug happen.
- **Annotation callouts at the critical frame**: *"Here. This is where a naive client shows the user
  'cancelled'."*
- **Deterministic** — same input, same playback, every time. No randomness.
- **Deep-linkable** — `#cancel-replace-race?t=4` so a reader can paste a link to the exact frame into
  his team's Slack. This directly serves the "what he saves and sends" behaviour in
  [BUYER-EVALUATION.md §3](BUYER-EVALUATION.md).
- **Reduced motion** — honour `prefers-reduced-motion` with a static, fully-labelled frame set.
- **Works without JS** as a static annotated diagram. Some of these get opened on a phone in a taxi.

> **Rendering:** hand-authored SVG + a small JS timeline driver, ~300 lines. Mermaid `sequenceDiagram`
> can produce the static fallback frames but cannot do the stepped animation or the synced message
> pane. Do not reach for a heavy diagramming library; these are six fixed scenarios, not a general
> diagram engine.

---

### E. FIX Message Teardown

An annotated log viewer. A real session, scrubbed, rendered as a scrollable log where hovering any
tag reveals: name, meaning, and *the bug caused by getting it wrong*.

Then the engaging part: **"This log contains three bugs. Find them."** Click to reveal. Something
like a sequence reset that shouldn't have been sent, an `ExecID` reused across sessions, an
`OrdStatus`/`ExecType` combination that no compliant counterparty should emit.

Nothing signals "we have debugged this at 3am" more efficiently than a bug hunt in a real log. It is
also genuinely fun, which is rare on a vendor site — and it is the single asset here most likely to
get shared into someone's engineering Slack.

Adjacent short piece, worth a paragraph rather than a page: **"FIX version reality"** — 4.2 vs 4.4 vs
5.0 SP2/FIXT 1.1, why counterparties are still on 4.2 in 2026, custom tags above 5000, and what
counterparty certification testing actually involves (weeks, a test script, a conformance window).

---

### F. The Architecture Configurator  ⭐ highest strategic value

Six questions:

1. Asset classes (equities · options · futures · FX · crypto · funds)
2. Geography / regulatory regime
3. Licensed broker-dealer, introducing broker, or building for one
4. Self-clearing or via a clearing firm
5. Retail, professional, or institutional users
6. Latency sensitivity (long-only investing → active retail → algorithmic → low-latency)

Output, generated live:

- A tailored **C4 L2 diagram** for that configuration
- The **integration list** it implies (broker candidates, market-data sources, KYC vendor type,
  reporting obligations)
- The **risk list** — the six things most likely to bite this specific configuration
- A **phased delivery outline** — what ships first to de-risk the decision
- **PDF export**

This is the asset that most directly serves what the buyer is actually paid to do. Per
[BUYER-EVALUATION.md §5](BUYER-EVALUATION.md), he has to present a recommendation to a committee. If
we hand him a tailored architecture and risk list with our name in the footer, **we write his slide
for him**, and our framing goes into a room we are never in.

It also converts the "nothing to take away" gap into a strength without gating anything behind a form.

> **Effort:** the largest item here — a week or more, mostly in getting the decision logic right
> rather than in the UI. Phase 3. But it is the one competitors will not copy.

---

### G. Post-incident notes (anonymized)

Three or four short technical narratives, ~400 words each: *what broke, how we found it, what we
changed.* No client names, no dates, no identifying detail — the incident classes are generic enough
that sanitization is straightforward.

Candidate shapes, to be replaced by our real ones:

- A reconciliation break traced to average-price rounding
- A duplicate order after a reconnect, and the idempotency scheme that replaced the retry logic
- A market-data gap during a volatile open that a naive gap-detector missed
- An onboarding funnel where the IDV vendor's soft-fail rate was double the contracted number

Admitting a bug is the highest-trust move available on a vendor site, and almost nobody does it. The
one requirement: it must end in a **systemic fix**, not "we were more careful afterwards."

---

### H. Live paper-trading sandbox (stretch)

A real order ticket on the page, wired to a paper/sandbox broker account. The visitor places an
order and watches the actual lifecycle — including the ability to trigger a cancel/replace race
deliberately.

Highest proof-per-pixel of anything here, and the highest cost and operational risk (rate limits,
abuse, sandbox downtime showing an error to a prospect). Phase 4, only if the earlier assets land.

---

### I. Takeaway artifacts

Because the buyer's job output is a document ([BUYER-EVALUATION.md §3](BUYER-EVALUATION.md)):

- **Configurator PDF** (asset F) — the tailored version
- **"41 questions to ask a trading platform vendor"** — a genuinely useful checklist, not a rigged
  one. It will be used against us too; that's the point, and we should be able to answer all of them
- **RFP response pack** — the standard vendor-qualification fields (company facts, security posture,
  IP terms, insurance, jurisdictions, references) pre-answered, for the ~20% of Level-3 buyers
- **The edge-case ledger as a printable PDF**

Ungated, or gated with email only. A form in front of a proof asset costs more evaluators than it
captures leads.

---

### J. Rewrites on the landing page itself

Cheapest changes, worth doing regardless of whether the engineering page ships.

**The 12 capability cards currently describe features.** Give each a second line naming the hard
part. Two examples:

> **Order Management** *(current)*
> Order types, quantity, leverage, time in force, stop-loss and take-profit strategies.
>
> **Order Management** *(proposed)*
> Order types, time in force, leverage, stop-loss and take-profit — with the state machine that
> holds up when a cancel and a fill cross on the wire, when a replace is rejected, and when the
> session drops with an unacknowledged order outstanding.

> **Integration With Brokers** *(current)*
> We help select and integrate brokers based on market coverage, API quality, latency, and SLA.
>
> **Integration With Brokers** *(proposed)*
> Broker selection on market coverage, API quality, and reconnection semantics — because the SLA
> tells you about uptime and nothing about what your open orders look like after a gateway restart.
> We've integrated IBKR, Alpaca, and others, and we keep notes on what each one gets wrong.

Same treatment for Trading Execution Middleware (FIX version reality, session recovery), Market Data
Storage (entitlements and non-display fees), Backtesting (survivorship bias, look-ahead bias,
realistic fill assumptions), and Paper Trading (why a naive simulator is optimistic).

**One new FAQ entry:**

> **Which brokers have you integrated, and what went wrong?**
> IBKR, Alpaca, [others]. Each has its own gotchas — IBKR's daily gateway restart and message
> pacing limits, Alpaca's fractional-share order-type restrictions and overnight corporate-action
> processing. We keep a public list of what we've hit and how we handle it → [engineering notes]

---

## 3. Anti-slop rules

The buyer is scanning for reasons to cut ([BUYER-EVALUATION.md §3](BUYER-EVALUATION.md)). These are
the tells that get a page cut.

**Never:**

- Stock imagery of glowing candlesticks, trading floors, or people in suits pointing at screens
- "Cutting-edge", "robust", "seamless", "leverage", "empower", "in today's fast-paced markets",
  "we understand that", "at the end of the day"
- Diagram arrows labelled "data", "requests", or "integration"
- Rounded claims with no unit — "high performance", "low latency", "enterprise-grade"
- A capability list where every item is equally weighted and equally vague
- Any number we cannot source, including plausible-sounding ones. The existing docs flag this
  repeatedly and they are right: one invented metric, caught on the call, destroys everything else
  on the page

**Always:**

- Every claim carries a tag number, a protocol version, a venue name, a date, or a regulation
- Name the version and the date: "FIX 4.4", "T+1 in the US since May 2024", "verified March 2026"
- Prefer the specific negative — *"we have not built a matching engine; we've integrated three"* —
  over the vague positive. Honest limits read as confidence
- Show artifacts: a log, a state table, a config, a schema fragment
- Write in the first person plural about things we actually did, and in the third person about
  general domain facts. Don't blur the two
- Let the reader disagree — publish the trade-off, not just the choice

**Process rule, and the one that actually determines whether this works:** an engineer who has
shipped one of these writes the first draft or sits for the interview. Marketing edits for clarity
and **cuts only**. Nothing gets added downstream of the engineer. Every failure mode in this
document should be checked by someone who has hit it; anything nobody can vouch for gets cut, not
softened.

Also: **date and own the content.** A byline ("written by [name], who built the FIX gateway on
[project]") and a "last verified" date do more for credibility than any amount of polish, and they
make the page structurally hard to fake.

---

## 4. Rollout

| Phase | Assets | Effort | Why this order |
|---|---|---|---|
| **1** | Edge Case Ledger (A) · Broker Matrix (B) · landing-page rewrites (J) | ~1 week | All three are writing, not engineering. Highest proof per hour. The ledger alone closes the biggest gap in the buyer evaluation |
| **2** | C4 set (C) · two sequence animations (D1 cancel/replace, D4 settlement) · FIX teardown (E) | ~2 weeks | The visual/interactive layer. Two animations done properly beat six done cheaply |
| **3** | Configurator (F) · takeaway PDFs (I) · post-incident notes (G) | ~2 weeks | Converts proof into something that travels into the buying committee |
| **4** | Remaining animations (D2/3/5/6) · live sandbox (H) | open | Only if phases 1–3 measurably move enquiry quality |

**Measure:** time on the engineering page, scroll depth, animation step-throughs, PDF downloads,
deep-links shared, and — the one that matters — whether enquiries start arriving that reference
specific content on it. When a prospect opens the call with *"I read your note about the cancel/fill
race"*, the page is working.

---

## 5. What we need from the team

None of this can be finished from the outside. Required inputs:

1. **Two 90-minute interviews** with the engineers who built the four platforms in our case studies.
   Agenda: what broke, what surprised you, what you'd do differently, which broker cost you the most
   days. Record and transcribe — this is the raw material for A, B, E, and G.
2. **Sanitized FIX/API logs** from any engagement, cleared by legal. Needed for D and E. Scrubbing
   requirements: no account numbers, no client identifiers, no counterparty CompIDs, no real
   symbols/quantities where they'd identify a strategy.
3. **The honest broker list** — which integrations we have actually shipped, versus evaluated,
   versus read about. Rows in B must be earned.
4. **Legal review** of the post-incident notes and the anonymized case-study details.
5. **A decision on the compliance/security block** flagged in
   [BUYER-EVALUATION.md §6](BUYER-EVALUATION.md) — which certifications we hold, which we don't. The
   honest version ("we work to X, we are not certified for Y") outperforms silence, but only
   engineering and management can supply it.

Everything in §2 that is domain knowledge — FIX semantics, settlement mechanics, regulatory
obligations — can be drafted immediately and needs only technical review. Everything that is a claim
about Itexus needs a source. The line between the two must stay visible in the finished page; the
credibility of the first half depends on the second half being unpadded.

---

## Appendix — accuracy caveats

Regulatory and vendor details move. Before publishing, verify against primary sources: FIX
specifications (FIX Trading Community), current IBKR and Alpaca API documentation, SEC/FINRA rule
text, FinCEN guidance on beneficial ownership reporting (which has changed recently and may change
again), and current ESMA/FCA timelines for the European T+1 transition. Items in this document were
drafted from working knowledge and are marked for verification rather than presented as verified.

A page that gets a rule detail wrong is worse than one that omits it — the reader who spots it is
exactly the reader we are trying to convince.
