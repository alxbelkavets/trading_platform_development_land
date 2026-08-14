# Itexus — Trading Platform Development Page

Content and copy for a redesign pass in Claude Design. The hero section is final and out of
scope — it's included below only for context and visual continuity. Everything from Case
Studies down is open for a new visual treatment.

**Brand color scheme and typography below are the real Itexus brand values (measured off the
live site). They are locked — keep them as the palette and type family for any redesign. Do
not introduce a different palette (e.g. do not go dark-mode/neon — that was tried and rejected).**

---

## Brand system (locked — do not change)

### Colors

| Role | Hex | Notes |
|---|---|---|
| Brand green (primary) | `#25bb4d` | CTA fills, links, key accents |
| Brand green (hover/bright) | `#30d05a` | Hover/active state on green fills |
| Ink (primary text) | `#051320` | All body text and headings — the dominant text color site-wide |
| Header/nav background | `#3a5b5c` | Dark teal-navy, distinct from ink |
| Header dropdown / darker state | `#18313b` | |
| White | `#ffffff` | Card backgrounds, hero text, button text |
| Dark card fill | `#1f2432` | Used for dark UI-mockup card treatments |
| Gray scale | `#666666` → `#f6f6f6` | 7-step neutral ramp for secondary text, dividers, muted backgrounds |
| Accent blue (rare) | `#109cde` | One small badge use only |

Note: real anchors should always get an explicit color — the live site has a known bug where
unstyled links render as browser-default `#0000ee` blue over the Coinstar logo. Don't reproduce
that; give every link an explicit brand color.

### Typography

Font: **Heebo** (self-hosted, weights 100–900 available; site mostly uses 400/500/600).

| Role | Size / line-height | Weight |
|---|---|---|
| H1 | 40px / 48px | 600 |
| H2 | 40px / 44px | 600 |
| H3 | 24px / 28.8px | 600 |
| Lead / subhead | 18px / 28.8px | 500 |
| Body | 14px / 19.6px | 400 |
| Nav link | 14px / 22px | 400 |
| Button label | 16px / 22.4px | 500–600 |

### Other tokens

- Border radius: **16px** on cards (dominant value), **10px** on buttons
- Shadow: `0 4px 44px -9px rgba(0,0,0,.08)` on white feature cards
- Card style: white background, `1px solid rgba(0,0,0,.1)` border, 16px radius, the shadow above
- Primary button: `#25bb4d` background, white text, `12px 32px` padding, `10px` radius
- Content max-width: **1312px**, centered, 16px side padding

---

## Hero (final — keep exactly as-is)

**Eyebrow:** Trading platform development

**H1:** Trading platforms built by people who have **shipped them before** *(the bolded part is
rendered in brand green)*

**Subhead:** FIX gateways, market-data fan-out, KYC/AML, audit trails. We build trading and
investing products for fintechs and investment managers, and this is the stack we work in.

**Primary CTA:** Get a proposal
**Secondary CTA:** See the platforms we've built →

**Assurance line:** We reply within 24 hours and sign an NDA before you share the details.

**Proof strip:** 300+ projects · Building since 2013 · 4.9 on Clutch from 40 reviews

**Hero image:** trading app screens — wallet balance with deposit/withdraw controls, plus a live
candlestick price chart.

---

## Section 01 — Case Studies

**Eyebrow/label:** Case Studies
**H2:** Trading platforms we've built
**Lede:** Four production ecosystems, from anonymised trading systems to a $2.2B fintech's crypto wallet.

### Featured case study (full-width, leads the section)

- **Client:** Coinstar (logo lockup)
- **Title:** Cryptocurrency e-Wallet Ecosystem for a Global FinTech Enterprise
- **Body:** PCI DSS-compliant application ecosystem for Coinstar, a leading international fintech
  company with $2.2 billion in annual revenue: web and mobile crypto wallets, embedded kiosk
  software, and a cloud-based API server.
- **Tags:** Enterprise, Fintech
- **Image:** Coinstar crypto wallet application screens

### Three supporting case studies (grid, below the featured card)

1. **Automated Stock Trading Platform** *(tag: Under NDA)*
   An automated, real-time trading system that allows administrators to configure trading strategies.
   Tags: Fintech, Trading

2. **Stock Trading Signals Platform** *(tag: Under NDA)*
   Intelligent investment assistant that performs technical analysis for a number of stocks.
   Tags: Fintech, Trading

3. **Algorithmic Intraday Stock Trading System** *(tag: Under NDA)*
   SaaS system for automated intraday stock trading, allowing investors to connect their brokerage accounts.
   Tags: Fintech, Trading

> **Open gap, flagged, not fabricated:** these cards describe features, not outcomes. Even
> anonymized figures (order latency, orders/day, users onboarded) would strengthen this section
> for a risk-averse buyer — but no such numbers exist yet to put here.

---

## Section 02 — What We Build (Trading Platform Capabilities)

**Eyebrow/label:** What We Build
**H2:** Trading Platform Capabilities
**Lede:** The parts a trading platform needs to actually go live.

This section pairs three product screenshots with twelve capability cards. In the current build
it's a bento/mosaic grid; feel free to propose a different layout, but keep all three screenshots
and all twelve capabilities — a previous version quietly dropped the screenshots and got called
out for it.

**Screenshots (in this order):** onboarding screen → order entry screen with a limit price slider
→ order confirmation screen after a trade.

**The 12 capabilities:**

1. **Integration With Brokers** — We help select and integrate brokers based on market coverage, API quality, latency, and SLA.
2. **Trading Execution Middleware** — Messaging, market-data fan-out, FIX and proprietary protocols in one low-latency layer.
3. **Order Management** — Order types, quantity, leverage, time in force, stop-loss and take-profit strategies.
4. **Investor Interfaces** — Web, mobile, and desktop with fast presets, hotkeys, and watchlists.
5. **Market Data Storage** — Multi-source database with historical intraday data for equities, futures, FX, options.
6. **Trading Algorithms** — We implement your strategy and provide a no-code builder with parameter checks and safeguards.
7. **Strategy Builder** — Visual builder and a code editor for custom indicators and algorithms.
8. **Backtesting** — Test and optimize strategies using historical market data before risking real money.
9. **Real-Time Alerts** — Fine-tuned asset alerts notify users within seconds of a target price change.
10. **Trade Log** — Detailed trading histories make it possible to identify mistakes and adjust strategies.
11. **Paper Trading** — Simulated trades under real market conditions, no real money at risk.
12. **Other Features** — Extend broker capabilities with portfolio management, FIX gateways, and scalable matching components.

---

## Mid-page CTA band

**Headline:** Need to talk to a **trading solution architect?** *(bolded part in brand green)*
**Body:** We're here to contribute our expertise and can take over the entire project, from
discovery to design, coding, and scaling.
**CTA:** Get a proposal

---

## Section 03 — Engagement Models (How We Work)

**Eyebrow/label:** How We Work
**H2:** Engagement Models
**Lede:** Three real cooperation models, no invented figures.

1. **Efficient Hours (Agile with Budget Control)** — *marked "Recommended"*
   Delivered in two-week sprints with a demo at the end of each one. You only pay for efficient
   hours within an agreed estimate, and can adjust requirements as new ideas come up.

2. **Fixed Price**
   Requirements, price, and timeline are documented and signed before work starts. Suits projects
   with a scope that's already well defined and unlikely to change.

3. **Outstaffing / Development Team as a Service**
   Vetted engineers join your team directly and work under your own project management, billed at
   a pre-agreed monthly rate.

**Footer link:** See the full breakdown of each model on our Cooperation Models page → (`/how-we-work/`)

---

## Section 04 — Testimonials

**Eyebrow/label:** What Clients Say
**H2:** What our clients say about us

Must render as an actual carousel (prev/next controls), not a static grid — a previous version
that used a static grid was explicitly rejected. Five testimonials:

1. "Itexus delivered the app according to the requirements. The team met all development
   milestones and deliverables. They were efficient, friendly, and cooperative. Itexus team was
   very timely with updates, a regular meeting cadence, and ad-hoc questions and answers via
   Slack. The team was very responsive and still is."
   — **Risk Management Director**, Investing Fund

2. "Itexus' work positions the business well for an imminent launch. They excel at managing
   their team, presenting frequent product demos to ensure that the project is aligned with
   development goals. An affordable price structure coupled with remarkable technical skill
   makes them an attractive partner."
   — **Phill Osolinski**, CEO Ryze Rewards

3. "The assigned team was easy to work with and they are especially strong collaborators and
   communicators. They demonstrated flexibility, professionalism, and trust in everything they
   did, and completed the work on time and budget."
   — **Sue Wollan Fan**, CEO Mango Connects

4. "Itexus excelled at both experimental AI and sprint-oriented UI/UX tasks. Itexus did strong
   project management work, too, a necessity in such a complicated project."
   — **Jesse Dubin**, Senior PM Standard&Poors

5. "They're a great group of developers who really understand the reality of business."
   — **Andreea Vanacker**, CEO SPARKX5

**Clutch strip:** 40 reviews on Clutch — 4.9 rating (with reviewer avatars)

**Award badges (12, shown as a scrolling marquee in the current build — keep all 12, don't
trim):** GoodFirms, YouTeam, Clutch, Expertise, SelectedFirms, TopDevelopers, Top Rated Custom
Software Development Companies, ITFirms, TrustFirms, Top Software Developers, Top Rated Mobile
App Companies, techreviewer.co.

---

## Section 05 — FAQ

**H2:** Frequently asked questions

Real accordion (single question expands at a time or independently — either is fine), keyboard
operable.

1. **How much does trading platform development cost?**
   Cost depends on the engagement model. Efficient Hours (Agile with Budget Control) bills only
   efficient hours against an agreed estimate. Fixed Price sets the full cost upfront once
   requirements are documented. Outstaffing bills a pre-agreed monthly rate per engineer. See the
   Engagement Models section above.

2. **How long does it take to build a trading platform?**
   Trading platform software development usually takes about 3 months or more, and directly
   depends on the features you want to implement. Get in touch to find out the estimated
   development time for a project like yours.

3. **Can you integrate with a third-party service?**
   Yes, we integrate third-party APIs and services according to your business goals: brokers,
   payment gateways, KYC providers, news providers, market data providers, crypto exchanges, and
   more.

4. **Do you offer support services?**
   Yes, we offer post-production support on a regular basis or on demand.

5. **Do you sign an NDA agreement?**
   We are comfortable signing legal agreements when developing a trading platform. We can either
   sign your NDA contract or create our own and send it to you.

6. **Have you built a trading platform before?**
   Yes, we have extensive experience in trading software development, with a specialty in stock
   market application development. See our trading platform case studies above.

7. **I have an idea. Where should I start?**
   Your next step depends on whether you have a clear product vision and detailed requirements.
   If not, we recommend that you start with the discovery phase. Contact us to discuss your idea.

8. **How do I hire trading platform developers?**
   Define your project scope and tech stack, then look for a team with experience in financial
   software, security protocols, and relevant technologies. Assess candidates through technical
   interviews, and prioritize a proven track record in secure, scalable trading platforms.

---

## Section 06 — Contact

**H3:** Let's discuss how we can help with your project

**Form fields:** Your name*, Company name, Email*, Phone number, "Tell us about your project"
message box*, NDA Required checkbox, Privacy Policy agreement checkbox* (links to `/privacy-policy/`)

**Submit button:** Send (reply within 24 hours)

**Process steps (shown alongside the form):**

1. **Share your project idea** — and we'll get back to you within 24 hours to sign the NDA and
   discuss the next steps.
2. **Discuss your project** — with a team of expert software architects, fintech analysts, and
   UI/UX designers.
3. **Receive a detailed proposal** — including software architecture, functionality, UI/UX
   design, and a detailed cost estimate.
4. **We start development** — Contract signed and development starts within 1–2 weeks; MVP live
   in 3–4 months.

---

## Header / nav (persistent across the page)

Logo: Itexus (white/dark variant depending on background)
Nav links: Services, Our Products, Case Studies (→ `/portfolio/`), Hire Developers, About Us
Header CTA button: Contact Us (→ `/contacts/`)

---

## Known content gaps (don't invent numbers to fill these)

- No outcome metrics for any case study (latency, throughput, users, etc.)
- No public pricing figures — engagement models describe structure only
- No team/stack bios (a previous section covering this was removed at the user's request)
- No compliance/certification detail beyond "PCI DSS-compliant" (Coinstar) and NDA willingness
