# Design system — Itexus Trading Platform page

Pulled from the live rendered page at `stage.itexus.com/trading-platform-development/`,
not guessed from screenshots. Two methods were used together: reading `getComputedStyle()`
on real elements in the browser (ground truth for what actually renders), and grepping the
19 theme CSS files in [`css/`](css/) for hex values and rules (source, including states not
visible in one snapshot). Captured 2026-08-13 at a 1440px viewport.

Machine-readable version: [`tokens.css`](tokens.css). Local page copy: [`page-source.html`](page-source.html).

## Typography

Font: **Heebo**, self-hosted, 9 weights (Thin 100 → Black 900). Files in [`fonts/`](fonts/),
loaded in `tokens.css`. Not a Google Fonts CDN link — the original theme ships the woff2s directly.

| Role | Size / line-height | Weight | Where measured |
|---|---|---|---|
| H1 | 40px / 48px | 600 | Hero: "Trading Platform Development Services" |
| H2 | 40px / 44px | 600 | Section title: "Trading Software Solutions We Develop" |
| H3 | 24px / 28.8px | 600 | Card heading: "Trading Platforms" |
| Lead / hero subhead | 18px / 28.8px | 500 | Hero paragraph |
| Body | 14px / 19.6px | 400 | Card and FAQ copy — this is the workhorse size, 92 uses site-wide |
| Nav link | 14px / 22px | 400 | Header nav |
| Button label | 16px / 22.4px | 500–600 | "Book a consultation" etc. |

The theme's CSS source also defines a larger scale — 64px / 56px / 32px / 20px steps — used
on other templates or wider breakpoints. Don't assume those apply here; the table above is
what this specific page renders at desktop width. Confirm on the actual element before reusing
a size at a new breakpoint.

Color note: 396 of the elements measured resolve to `#051320` for text — that is effectively
*the* ink color for this page, not a dark gray among several. Use it as the one body/heading color.

## Color

| Token | Hex | Role |
|---|---|---|
| `--color-brand-green` | `#25bb4d` | Primary CTA fill, links, key accents (26 uses) |
| `--color-brand-green-bright` | `#30d05a` | Hover/active state on green fills |
| `--color-ink` | `#051320` | All body text and headings outside the hero |
| `--color-header-bg` | `#3a5b5c` | Header/nav bar background |
| `--color-header-bg-dark` | `#18313b` | Dropdown/darker header state |
| `--color-white` | `#ffffff` | Card backgrounds, hero text |
| `--color-gray-900` | `#1f2432` | Dark UI-mockup card fills (the dark screenshots in the grid) |
| `--color-gray-600…50` | `#666 → #f6f6f6` | Secondary text, dividers, muted backgrounds — see `tokens.css` for the full 7-step ramp |
| `--color-accent-blue` | `#109cde` | One small badge use — verify before reusing elsewhere |

**Known bug, not a token:** `rgb(0, 0, 238)` / `#0000ee` — the browser's default unvisited-link
blue — appears 175 times as an inherited text color. It's visible in the live page as blue text
misaligned over the "Coinstar" case-study logo (see the design critique for the screenshot). This
is unstyled anchors leaking the user-agent default, not an intentional brand color. If you're
matching this page's palette, leave it out; if you're fixing the page, that's the actual bug to fix
— give every anchor an explicit color.

## Shadows

Three-step scale, all sharing the same offset and blur — only the opacity changes:

```
--shadow-sm  0 4px 44px -9px rgba(0,0,0,.03)
--shadow-md  0 4px 44px -9px rgba(0,0,0,.04)
--shadow-lg  0 4px 44px -9px rgba(0,0,0,.08)   ← the white feature cards use this one
```

## Radius

`16px` is the dominant non-zero radius (43 uses) — that's the feature-card radius. Buttons use
`10px`. Full scale in `tokens.css`: 4 / 6 / 8 / 10 / 12 / 16 / 24px, plus `50%` for avatars/dots.

## Layout

- Content is centered in a `.general-container` at **max-width: 1312px**, with **16px** side padding.
- Section vertical rhythm varies by block (each `template-parts/blocks/*` component ships its own
  spacing) — no single consistent section-padding token to extract; check the relevant block CSS
  in `css/blocks_*` if you're matching a specific section.

## Components (as measured)

**Primary button** — "Book a consultation," "Contact Us"
```
background: #25bb4d
color: #fff
padding: 12px 32px
border-radius: 10px
font: 500 16px/22.4px Heebo
```

**Feature card** — the "Data & Analytics" / "Execution & Middleware" boxes
```
background: #fff
border: 1px solid rgba(0,0,0,.1)
border-radius: 16px
box-shadow: 0 4px 44px -9px rgba(0,0,0,.08)
```

## Source files

```
site/
├── page-source.html   raw HTML pulled from the live URL
├── tokens.css          @font-face + CSS custom properties, ready to @import
├── DESIGN-SYSTEM.md    this file
├── css/                 19 theme stylesheets as served (header, footer, and one per content block)
├── fonts/                Heebo woff2, all 9 weights
└── img/                  logo + hero/CTA background images
```

## Working with this locally

`tokens.css` is written to be dropped into a new build directly — `@import` it, or copy the
custom properties into whatever your existing stylesheet setup is. It does not attempt to
reconstruct the full theme (grids, breakpoints, block-specific layout); it captures the
tokens — color, type scale, radius, shadow — that keep a redesign visually on-brand. For a
specific component's exact CSS, the matching file in `css/blocks_*` is the source of truth.

If you want the raw page open locally as a visual reference while you work, `page-source.html`
still points at `stage.itexus.com` for its assets, so it renders correctly over a network
connection — it's a snapshot for diffing against, not an offline archive.
