# The Shortlister — How the Real Buyer Reads This Page

Research into who actually lands on a "trading platform development" page with budget behind them,
what they are trying to accomplish in that visit, and how they judge what they see. Checked against
[PAGE-COPY.md](PAGE-COPY.md) / [page-v3.html](page-v3.html) so it doubles as a gap list.

Companion to [CONVERSION-RESEARCH.md](CONVERSION-RESEARCH.md), which covers offer mechanics. This
document covers the person.

---

## 1. Who he is

Two variants show up on this page, and they behave differently. The page currently speaks mostly to
the first.

**Variant A — "Build from scratch."** Head of Product / CTO / COO at a broker, prop firm, asset
manager, neobank, or a funded fintech startup. There is a licence application in progress, a
partnership signed, or a client base waiting. No platform exists. Budget is a program line, often
$300k–$2M+, approved in principle but not allocated to a vendor.

**Variant B — "Module into an existing app."** Head of Product / VP Engineering at an established
fintech (banking app, wealth app, payments, super-app). The company already has a live product with
real users and an internal engineering team. He is adding investing/trading as a feature. His
constraint set is completely different: he is not buying a platform, he is buying **capacity plus a
domain skill his team lacks**, and the integration surface into his existing stack is the whole
risk.

Both are what procurement literature calls the **champion or evaluator**, not the decision maker.
The economic buyer sits above him — a board, an IT steering committee, a CFO, sometimes a
group-level architecture review. He is one member of a buying group that averages **6–10
stakeholders**, each doing their own independent research and each arriving with different
conclusions ([Gartner](https://growthmethod.com/gartner-b2b-buying-journey/)).

### What he is actually being paid to do here

He has not been told "buy a trading platform." He has been told **"find out who can do this and come
back with options."** His deliverable is not a signed contract. It is a **slide, a comparison table,
or a short memo naming 3–5 companies with a recommendation.**

This is the single most important fact on this page, and it reframes everything below: he is not
shopping. **He is collecting evidence he can defend in a room you will never be in.**

### His actual fear

Not "will this be expensive." It is **"will I be the person who recommended the vendor that
failed."** In a trading system, failure is not a late release — it is a mispriced order, a
regulator letter, a client's money stuck in a broken settlement flow, a public incident. Vendor
choice is a career-visible decision here in a way it is not for a marketing site.

Everything he does on this page is risk-transfer behaviour. He is looking for proof he can point at
later and say: *this is why they were a reasonable choice.*

---

## 2. His priorities, ranked

Roughly the order he applies them, and roughly the weight in his head. He will not fill in the
bottom of this list from a website — that is what the call is for. He needs the top of it from the
page, in about ninety seconds, or he leaves.

| # | Priority | What it really means | Answered on the page? |
|---|---|---|---|
| 1 | **Have you built *this* before?** | Not fintech. Not "300+ projects." A system with orders, positions, market data, and money at risk. | ⚠️ Four case studies, three under NDA and described by feature only |
| 2 | **Domain vocabulary check** | Does the page use words that only someone who has shipped one uses — FIX, time in force, order types, market-data fan-out, reconciliation, pre-trade risk? | ✅ Strongest asset on the page today |
| 3 | **Regulatory / security posture** | KYC/AML, audit trail, data residency, PCI DSS, SOC 2, ISO 27001, and whether *they* understand which regime applies to him | ⚠️ PCI DSS on one case study; no certifications listed |
| 4 | **Can they name the hard parts before I do?** | The tell for a real partner vs a body shop. Latency in the hot path, market-data cost and licensing, broker SLA quality, reconciliation, failover during market hours | ⚠️ Implied by capability list, never stated as risks |
| 5 | **Scale of the shop / survivability** | Will they exist in three years, and can they staff this without pulling my team off the project | ⚠️ "Since 2013", 300+ projects, no headcount or team structure |
| 6 | **Engagement + commercial model** | Fixed price vs T&M vs staff aug — because different models need different board approvals | ✅ Three models, clearly explained |
| 7 | **Order-of-magnitude cost and time** | He cannot open a conversation with the board saying "no idea" | ⚠️ "3 months or more" in the FAQ; no cost band anywhere |
| 8 | **IP, source code, exit** | Who owns the code, what happens if we part ways, can my team take it over | ❌ Absent entirely |
| 9 | **References he can actually call** | Testimonials are marketing; a reference call is evidence | ⚠️ Testimonials + Clutch, no offer of a reference call |
| 10 | **Location / timezone / language** | Overlap hours with his team, and increasingly a compliance question about where data and people sit | ❌ Not stated on the page |

Note how much of the top half is **credibility**, and how little is **capability**. The twelve
capability cards address priority #2 well and priorities #1 and #4 not at all. He assumes any
serious vendor can list features; feature lists are table stakes and do not differentiate.

---

## 3. How he actually evaluates — the mechanics

### He does not read. He harvests.

He has 4–8 tabs open, one per candidate vendor, and a spreadsheet or Notion table beside them. He is
running the page as a **field extraction task**: pulling values into columns he has already defined.
Typical columns: *domain proof · relevant projects · team size · location · engagement model ·
compliance · rough cost · contact route.*

Design implication: anything that cannot be **copied into a cell** does not survive the visit.
Prose paragraphs lose to labelled facts. This is why specificity beats eloquence on this page.

### His scan order

1. **Hero — 5 seconds.** One question: *is this a real trading specialist or a generalist agency
   with a trading landing page?* The current H1 ("built by people who have shipped them before")
   plus the FIX/market-data/KYC subhead passes this test. This is the page's best-performing moment.
2. **Proof strip / logos — 5 seconds.** Looking for a name he recognises. Coinstar helps. Three
   "Under NDA" cards do not — to him, unnamed means unverifiable.
3. **Case studies — 60–90 seconds, the deepest read on the page.** He is trying to find *one*
   project close enough to his own that he can cite it upward. He wants: asset class, venue/broker
   integrations, scale, latency, timeline, team size, outcome.
4. **Capabilities — 20 seconds, skimmed for absence.** He is not reading twelve cards. He is
   scanning for the two or three terms specific to his own project (options? crypto? FIX 4.4?
   margin? multi-currency settlement?) and checking they appear. A missing term is a bigger signal
   than eleven present ones.
5. **How you work / engagement — 30 seconds.** Mapped directly onto what his procurement process can
   accept. Fixed price is often the only model a board will approve for a first engagement.
6. **FAQ — used as an objection dump.** He goes here specifically for cost, timeline, IP, and NDA.
7. **Contact — the decision point.** He is judging *what happens if I fill this in.* If it reads
   like a lead form that routes to a salesperson, a large share of qualified evaluators leave and
   email a named person instead — or leave entirely.

### The disqualifiers

He is looking for reasons to **cut** the list, not to extend it. Cutting is cheaper than evaluating.
Fast cuts on this category of page:

- Generic stock imagery of "trading" (glowing candlesticks, men in suits) — reads as a marketing
  page written by people who have not built one
- Zero named clients
- Feature lists with no architecture behind them
- No mention of compliance or security anywhere
- "Contact us" as the only interaction available
- Testimonials about *communication quality* only, never about *the system working* — a live
  weakness in the current testimonial set, which praises responsiveness and project management but
  never says the platform performed

### What he saves and sends

If the page works, one of two things happens: he **copies the URL into a Slack/Teams message or the
shortlist doc**, or he **downloads/screenshots something**. The second is far more valuable to you,
because it enters the company's internal record with your framing attached. There is currently
nothing on the page to take away — no PDF, no architecture overview, no capability deck. That is a
real gap for a buyer whose job output is a document.

---

## 4. How much does he actually know?

This is where most vendor pages guess wrong. He is **not** a blank slate, and he is **not** holding
a finished spec. Three maturity levels, and the page has to serve all three without insulting any.

*(The percentages below are estimates for framing, not measured data. If Itexus has inbound-lead
records, replacing them with your own distribution would make this section considerably more
useful — and would tell you which level the page should optimise for.)*

**Level 1 — Directional (roughly 30% of serious enquiries).**
Knows the business goal ("we want our users to be able to buy stocks in-app"), the target market,
and roughly the budget order of magnitude. Has no architecture, no venue selection, no view on
build-vs-buy. Often has already spoken to one incumbent vendor and been quoted something that
frightened him. **What he needs from you: help framing the problem.** He is highly receptive to a
discovery/architecture engagement, because it converts his ambiguity into something board-ready.

**Level 2 — Structured high-level requirements (the majority, ~50%).**
This is the modal visitor. He has a 5–20 page document or a deck: user roles, asset classes, target
markets, a feature list, a launch date driven by something external (a licence, a funding round, a
partner go-live), and a set of constraints (existing stack, existing broker relationship, a
regulator's expectations). He knows *what*, not *how*. Open questions he cannot answer alone:
which broker/liquidity provider, build vs licence the matching/execution layer, what the market-data
bill will be, what the regulator will require of the audit trail. **He has enough to hold a real
technical conversation and not enough to write an RFP that a vendor could bid on precisely.**

**Level 3 — Detailed spec / formal RFP (~20%).**
Usually a larger institution with procurement involved. He arrives with an SRS or an RFP document
and a scoring matrix. He is on your page to check eligibility before sending it, and to fill in
vendor-profile fields. For him the page is a **qualification gate**, not a sales asset: company
size, certifications, insurance, jurisdictions, references, financial stability. If those are
missing he may still send the RFP, but you will start behind vendors who published them.

**The through-line:** at all three levels he knows his *business* requirements considerably better
than his *technical* ones, and he knows he does not know the technical ones. He is not embarrassed
about this — but he will be embarrassed in front of his board, which is exactly why he wants a
partner who can fill that half. A page that assumes he has a spec loses Levels 1 and 2. A page that
assumes he knows nothing insults Level 3.

---

## 5. What next step does he want?

**Not a sales call.** The single most common mismatch on pages like this.

He is at a stage where a discovery/qualification call with an account manager costs him 45 minutes
and returns nothing he can put in his shortlist doc. He already knows he has a project; being asked
"so tell me about your project" by someone who cannot answer follow-up questions is a wasted
meeting, and increasingly buyers simply avoid it — Gartner finds a majority of B2B buyers now
prefer a **rep-free** path where one exists
([Gartner, 2026](https://www.gartner.com/en/newsroom/press-releases/2026-03-09-gartner-sales-survey-finds-67-percent-of-b2b-buyers-prefer-a-rep-free-experience)).

**What he wants is a technical conversation with someone who has built one**, framed and bounded:

- Named role on the other side — a solution architect or tech lead, not "a specialist"
- A stated agenda: his requirements, an architecture sketch, integration options, risks, a
  ballpark range
- 45–60 minutes, NDA signed first
- A written artifact afterwards he can forward: a summary, a high-level architecture, an indicative
  estimate with assumptions listed

The page already gestures at this in two places — the mid-page CTA "Need to talk to a trading
solution architect?" and step 2 of the contact process ("discuss your project with software
architects, fintech analysts"). **These are the strongest conversion assets on the page and they are
in the weakest positions.** The primary CTA is still "Get a proposal," which is both vaguer and
more committal-sounding than what he actually wants.

There is also a **sequencing** point. He is not authorised to buy. His realistic first ask is often
smaller than the page assumes — an NDA and a 30-minute technical sanity check, or a written response
to five questions his CFO raised. Making the first step small and technical is not a downgrade of
the sale; it is the shape of the sale at this stage.

### After the call, his real job starts

He now has to present. What he needs from you is **board-ready material**: a one-page architecture
view, a phased plan with a first milestone that de-risks the decision, a cost band with the
assumptions visible, a comparable project, and answers on IP, security, and exit. Vendors who supply
this well are frequently the ones recommended, because the champion presents *your* framing to the
committee — you are, in effect, writing his slide for him. Vendors who send a generic capabilities
deck make him do that work himself, and he will resent it.

---

## 6. Gaps on the current page, ranked by cost

| Gap | Why it costs conversions | Fix |
|---|---|---|
| **No outcome data on any case study** | Priority #1 for the buyer, and the page answers it with feature descriptions. "Under NDA" ×3 reads as unverifiable. | Even anonymised and bounded: *"European broker, 12 months, 40k accounts, sub-100ms order round-trip, FIX 4.4 to two prime brokers."* No client name required. Already flagged as an open gap in [PAGE-COPY.md](PAGE-COPY.md) — this is the highest-value thing to go and collect. |
| **No compliance/security block** | Priority #3, and for Level-3 buyers a hard qualification gate. | A short factual band: certifications held, standards worked to, data-residency options, secure SDLC, pen-test practice, NDA/DPA readiness. State only what is true — an honest "we work to X, we are not certified for Y" outperforms silence. |
| **The primary CTA is a proposal, not a conversation** | Misreads the stage. "Get a proposal" implies he has a spec (only ~20% do) and implies commitment he cannot give. | Make the architect conversation the primary CTA, with the agenda and the named role stated. Keep "get a proposal" as the secondary path for Level 3. |
| **Nothing to take away** | His deliverable is a document; the page gives him nothing to put in it. | A downloadable capability/architecture PDF, gated lightly or not at all. It travels into the committee with your framing intact. |
| **No cost or team-size anchoring** | He must open the board conversation with *some* number. Absent one, he anchors on a competitor who published one. | A band with conditions attached ("integration projects typically start at $X; full platforms $Y–Z depending on venues and asset classes") beats nothing. |
| **IP / source ownership / exit unaddressed** | Standard board question; its absence is noticed by procurement. | One FAQ line. Cheap to add, disproportionately reassuring. |
| **No risk-naming anywhere** | Priority #4 — the clearest signal separating an operator from a vendor. | A short section: *"What usually goes wrong in these builds"* — market-data licensing costs, broker SLA reality, reconciliation, failover during market hours. Naming the risks is the most credible thing you can do on this page, and costs nothing but honesty. |
| **Testimonials prove process, not product** | Five quotes about responsiveness and project management, none about the system working in production. | Where possible, source one quote that references the platform's behaviour under load or through launch. |
| **Location, team size, timezone absent** | Cheap spreadsheet fields he must fill and cannot. | A single facts strip. Anything he must email you to learn is friction at the shortlist stage, where he is comparing, not engaging. |

---

## 7. The one-line summary

He is not a customer yet. He is an internal advocate assembling a defensible recommendation, holding
solid business requirements and shaky technical ones, and what he wants from this page is **enough
verifiable, copyable evidence to justify putting you on a list — followed by a bounded technical
conversation with an architect that leaves him holding a document he can present.**

Every fix above is a version of the same move: **replace claims with facts he can lift.**

---

## Sources

- [Gartner B2B Buying Journey: 6-Stage Framework](https://growthmethod.com/gartner-b2b-buying-journey/) — buying group size, independent research behaviour
- [Gartner Sales Survey: 67% of B2B Buyers Prefer a Rep-Free Experience](https://www.gartner.com/en/newsroom/press-releases/2026-03-09-gartner-sales-survey-finds-67-percent-of-b2b-buyers-prefer-a-rep-free-experience)
- [B2B Buying Committee Benchmarks 2025 — The Starr Conspiracy](https://www.thestarrconspiracy.com/insights/benchmarks/b2b-buying-committee-benchmarks-2025)
- [Vendor Selection Process: Steps, Criteria & Checklist — Ivalua](https://www.ivalua.com/blog/vendor-selection-process/)
- [How to Write an RFP for Software Development — DashDevs](https://dashdevs.com/blog/how-to-write-rfp/)
- [What Is the RFP Vendor Selection Process — Responsive](https://www.responsive.io/blog/vendor-selection-tips)
- [Choosing a Fintech Software Development Partner — Artkai](https://artkai.io/blog/choose-fintech-development-partner)
- [The Guide to Fintech Development Outsourcing — DashDevs](https://dashdevs.com/blog/the-ultimate-guide-to-fintech-development-outsourcing-how-to-make-it-work/)
- [Institutional Trading Software: What to Look For in 2026 — Wyden](https://www.wyden.io/news/institutional-trading-software-2026/)
- [Build vs. Buy: A Guide for Financial Services Firms — eMoney Advisor](https://emoneyadvisor.com/blog/build-vs-buy-a-guide-for-financial-services-firms/)
- [OMS vs EMS vs OEMS — TS Imagine](https://tsimagine.com/insights/oms-vs-ems-vs-oems-trading-systems/)
