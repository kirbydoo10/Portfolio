# Portfolio redesign — "Workbench" design system

> **Superseded (2026-09-22):** direction changed to a style adapted from thegr8binil.me —
> dark `#0e100f` / cream `#ffffe3`, Hanken Grotesk, pill UI, multi-colour accents
> (purple, amber, mint, pink, orange), stacked uppercase hero, numbered "What I do" rows,
> case rows with a metric on the right, giant footer wordmark. Dark by default; light
> theme kept. Content, ordering and bundled fixes below still apply. No content is hidden
> behind scroll animations.

**Date:** 2026-09-22
**Audience for the site:** recruiters and hiring managers for data analyst / BI roles.
**Problem:** the current neon-terminal look (scanlines, glow grid, custom cursor, typed text,
`//` tags, "∞ lines of code") reads as templated AI output and buries the real evidence.

## Direction

Direction B, "The Workbench": clean, structured, BI-tool flavour. Evidence first.

## Tokens

| Token | Light (default) | Dark |
|---|---|---|
| `--bg` | `#ffffff` | `#0f1419` |
| `--surface` | `#f5f7f9` | `#161c22` |
| `--text` | `#16202a` | `#e6eaee` |
| `--text-muted` | `#5b6875` | `#8d99a5` |
| `--border` | `#dde3e9` | `#26303a` |
| `--accent` | `#0b6e4f` | `#3fb68b` |

- Type: IBM Plex Sans (all text), IBM Plex Mono (figures, dates, tech tags only).
- Spacing on an 8px grid; radius 4px; no glows or shadows.
- Light theme by default; toggle persists choice in `localStorage` (guarded with try/catch).

## Removed

Scanlines, grid background, mouse glow, custom cursor, typed effect, `//` section tags,
filler stats, emoji icons.

## Page structure

1. **Nav** — name, section links, theme toggle (44px).
2. **Hero** — availability line, headline, stack sentence, 3 KPIs (8 transit segments,
   millions of rows, 5 certifications), CTAs (Download CV, See the dashboard work), photo
   as a rounded square (sleeping photo in dark mode).
3. **Experience** — AF Payments internship, then Education and Certifications, all visible
   (no tabs).
4. **Projects** — four project cards with stack tags and GitHub links.
5. **Skills** — grouped rows (category → tags).
6. **About** — short bio.
7. **Contact** — email (lancekirbylazaro@gmail.com), GitHub, LinkedIn.
8. **Footer** — © 2026.

## Fixes bundled in

- Stray `>` after the AF Payments logo.
- Google Data Analytics card used the IBM badge image → lettermark until a real badge exists.
- Descriptive alt text on every image.
- Placeholder email replaced; footer year updated; "Currently a graduating at" typo fixed.

## Constraints

- Stays a single static `index.html`; no build step, no framework.
- Works at phone width (single column below 760px), 44px minimum tap targets.
- Original preserved as `index.backup.html`.
