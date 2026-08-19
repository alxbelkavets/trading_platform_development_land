# Trading Platform Development page — v4 rebuild

This repo contains a rebuilt version of [stage.itexus.com/trading-platform-development](https://stage.itexus.com/trading-platform-development/). The new version lives at [`site/page-v4.html`](site/page-v4.html) and is ready to hand off to marketing for review and publishing.

This document explains what changed, why, and what still needs marketing/legal input before it goes live.

## How to look at it

Open [`site/page-v4.html`](site/page-v4.html) in a browser. Don't just double-click the file — relative paths for fonts and CSS won't resolve correctly. Serve the `site/` folder locally instead:

```bash
python3 -m http.server 4173 --directory site
```

Then visit `http://localhost:4173/page-v4.html`.

The original page is preserved for comparison at [`site/page-source.html`](site/page-source.html) (a saved copy of the live stage page).

## Why we touched it

The original page is a features list: a grid of "solutions we develop," a grid of "core features," a generic FAQ. It tells a visitor what Itexus *can* build, but not why they should believe Itexus can build *their* specific, hard, regulated system — which is the actual question a trading-platform buyer has. There's no proof of past delivery, no explanation of how an engagement actually starts, and no honest answer on cost.

The rebuild is organized around answering that buyer's real questions in order: has this company done this before, what would working with them actually look like, and what would it cost.

## What changed, section by section

**Hero.** Old headline: "Trading Platform Development Services" — a service-category label. New: *"We've built trading platforms before. We can build yours."* — a direct claim of experience, backed immediately by a sub-line naming the actual technical scope (FIX connectivity, market data infrastructure, risk controls, KYC/AML, web and mobile terminals) instead of marketing-speak.

**Facts strip (new).** A row of concrete, verifiable numbers right under the hero: Clutch rating, years building, projects delivered, reply time, typical MVP timeline. Nothing here is a number we can't back up — we deliberately left out team size and client logos because we don't have a citable figure for them yet, rather than filling the row with a placeholder.

**Case studies (new section, "Trading platforms we've built").** Leads with actual delivered projects and real metrics, e.g. a retail brokerage card built to handle **50 transactions/second at 130ms average latency with zero errors**. This section didn't really exist on the old page — proof-of-work is now the second thing a visitor sees, right after the hero.

**"Build, modernize or integrate" (new).** A short section that routes visitors by intent — are they building new, replacing an old system, or integrating a piece into what they already have — instead of making everyone read the same generic capabilities list regardless of what they actually came for.

**Capabilities.** Reorganized into a compact tab interface instead of a long scrolling list, so the depth is there without the page feeling endless.

**"What we've actually built and integrated" (Engineering Notes, rebuilt).** Rewritten to cite specific, real integration work — named brokers (Interactive Brokers, Alpaca, Blackwell Global), named data/KYC/payment providers, and a specific engineering detail (Interactive Brokers' paper-trading account only allows one test a day, so we built an emulator to get around it). This kind of specific, checkable detail is what signals real experience to a technical buyer — generic claims don't.

**"What Happens Next" (new — this is the biggest structural change).** The old page has no explanation of what happens after someone submits the contact form. The new page walks through it: a short 30–45 minute call first (no slides, NDA signed beforehand), then — if it's a fit — an actual team (architect, fintech analyst, designer) spends one to two weeks on a written architecture outline, integration plan, and cost range, delivered free and with no obligation. This reflects how the business actually works: the first call is with a BD rep, not an architect, and we say so plainly instead of implying otherwise.

**Engagement Models.** Clarified and synced against how the company actually describes itself elsewhere (`itexus.com/how-we-work`), including a straight answer on IP/source-code ownership (the client owns it on payment, or from day one if the engagement starts with a deposit) instead of leaving it as a FAQ hedge.

**FAQ.** Cut generic questions, kept the ones buyers actually ask (cost, timeline, ownership, NDA, brokers integrated, support after launch), and rewrote the cost answer to explain *what drives cost* (how much has to be built vs. integrated) with a real anchor: **an MVP — client-facing app, admin panel, basic middleware, plus KYC/broker/banking integrations — starts at around $100k.** This is the only price figure on the page, stated as a floor by deliberate choice, not a fixed quote.

**Removed: the security/compliance section.** The old page implicitly leaned on this messaging; an early version of the rebuild had a dedicated "How We Handle Risk" section, but it was cut after an audit found it mostly duplicated claims made elsewhere on the page word-for-word, with no unique regulatory content to justify its own section. The one genuinely new claim it would have needed (which regulatory regimes we've shipped under) was never given a real answer, so rather than publish a hedge ("ask us"), the section was removed and its one legitimate point (source-code ownership) was folded into Engagement Models instead.

## Ground rules we followed

- **No invented numbers.** Every metric, certification claim, or headcount on the page is either a real figure or omitted. Where we didn't have a verifiable number, we cut the claim rather than write around it with vague language.
- **No overstated regulatory claims.** Two claims from an earlier draft were corrected after checking primary sources: a clock-sync tolerance that actually applies to a specific category of market participant, not universally, and a settlement-affirmation claim that overstated what the underlying SEC rule requires.
- **Copy sounds like a person wrote it.** Passed through multiple rounds of tone editing specifically to strip AI-generated phrasing patterns (templated "built by people who've X'd" constructions, rule-of-three rhythms, reveal-and-zinger sentence shapes).

## What still needs marketing/legal input before publishing

- **Pricing:** the page now states one number ($100k MVP floor). If marketing wants a fuller pricing picture (e.g., a range for smaller integrations vs. full platforms), that data doesn't exist in the current copy and would need to come from sales/finance.
- **IP/source-code ownership claim:** this is now a firm, public statement on the page. Recommend legal sign-off before publishing, since it wasn't previously stated this plainly anywhere public.
- **SEC citation:** an earlier draft referenced a specific SEC rule number for the T+1 affirmation claim; it's deliberately left unnamed on the current page because we couldn't verify the citation against a primary source we could access. If marketing/legal can confirm the rule number, it could be added back.
- **Team size, delivery locations, client logos:** left off the facts strip because we don't have citable figures. If marketing has approved numbers for these, they'd strengthen that section.
- **Case study / testimonial depth:** the page could use one more performance-focused client testimonial and additional case-study metrics if marketing has more to draw on.

## Where things live

- [`site/page-v4.html`](site/page-v4.html) — the new page (this is what to review/publish)
- [`site/page-source.html`](site/page-source.html) — a saved copy of the original live page, for comparison
- [`site/PAGE-COPY-V4.md`](site/PAGE-COPY-V4.md) — the full copy deck for the new page, with notes on why specific lines were written the way they were
- [`site/PAGE-PLAN.md`](site/PAGE-PLAN.md) — section-by-section outline and the judgment calls made along the way
- [`site/css/`](site/css), [`site/img/`](site/img), [`site/fonts/`](site/fonts) — assets the page depends on
