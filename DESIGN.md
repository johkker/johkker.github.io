# Design

The visual system is **Editorial Street**, the same one the app uses (source of truth: `raptrak/mobile/DESIGN.md` and `mobile/src/styles/theme.ts`). The site is the brand version of it: more scale, more poster, same tokens.

## Theme
Dark, always. The scene: a fan or MC at night, phone in hand, on the way to the battle in the square. Color strategy: **Restrained** on most of the surface, with **Committed** moments of fuchsia (a solid band per page, CTAs).

## Color (tokens in `src/styles/global.css` → `@theme`)
- Canvas and surfaces: `bg #0A0A0A`, `surface #141414`, `elevated #1F1F1F`, `darkest #050505`.
- Accent (the only one): `accent #C21BDA`, `accent-dark #9A12AD`, `accent-soft rgba(194,27,218,.14)`. On text-sized elements, the accent is for actions, links, and state. As a surface it can drench a whole section, with white text on top (≈4.7:1).
- Text: `text #F2F2F2`, `text-2 #B8B8B8`, `muted #8C8C8C` (AA body), `dim #6E6E6E` (large text or decoration only).
- Semantic: `success #3DD68C`, `warning #E0A800`, `error #E5484D`.
- Borders: `hairline #242424`.

## Typography
- **Barlow Condensed** 700/800, uppercase: headlines, poster energy, wordmark.
- **Archivo** 400/500/600/700: body, UI, buttons.
- **Roboto Mono**: numbers, metadata, days and times, like the app.
- Fluid scale with `clamp()` on headlines (h1 ≤ 6rem). Body text at 17–18px, line-height 1.6, max 68ch.

## Shape, depth, motion
- Radius: 8 / 12 / 20 / full, as in the app. Hairline borders, soft shadows. No glow, no glass, no gradient text.
- Motion: headlines enter with a mask reveal on first load, 150–250ms on interactions, ease-out-quart. Reduced motion means instant, with no movement.

## Components
- `Logo.astro`: "Marcador · Coroa" mark (the app's real path) plus the RAP/TRAK wordmark.
- `Phone.astro`: phone frame around a real app screenshot.
- Buttons: `.btn-primary` (solid fuchsia), `.btn-ghost` (hairline border). Minimum height 48px.
- Chips (`.chip`): the same filters and badges as the app (1v1, sangue, Minha cidade…).
