# Slidev Theme — Inloop Studio

Brand‑accurate Slidev theme for Inloop Studio (fonts, colors, logo, backgrounds), using a clear README structure similar to neversink.

## Install

- npm: `npm i -D @inloopstudio/slidev-theme-inloopstudio`
- pnpm: `pnpm add -D @inloopstudio/slidev-theme-inloopstudio`
- yarn: `yarn add -D @inloopstudio/slidev-theme-inloopstudio`

## Use in your deck

Add to the frontmatter of your `slides.md` (quote the value to satisfy YAML):

```yaml
---
theme: "@inloopstudio/slidev-theme-inloopstudio"
---
```

Optionally set the primary accent color:

```yaml
---
theme: "@inloopstudio/slidev-theme-inloopstudio"
themeConfig:
  primary: '#7147FF'
---
```

## What you get

- Type system: Inter (sans), Instrument Serif (serif), Fira Code (mono/labels)
- Headings: Instrument Serif globally for h1–h6; body text in Inter
- Background: Vector dotted canvas by default (clean, scalable)
- Logo: Inloop wordmark shown on every slide (auto light/dark)
- Brand tokens: full color palette and semantic tokens

## Layouts

- `default` — standard slide
- `cover` — cover slide with optional background image
- `center` — centered content (logo included)
- `intro`, `section`, `statement`, `quote`, `fact` — lightweight variants

Use via frontmatter on a slide:

```yaml
---
layout: center
---
```

## Typography helpers

- Display (Inter, Bold): `.display-300` … `.display-700`
- Serif headings (Instrument Serif): `.heading-200` … `.heading-600` (+ `-italic` variants)
- Eyebrow labels (Fira Code): `<span class="eyebrow">[FEATURE]</span>`

## Fonts configuration (Slidev)

This theme ships local fonts and recommends disabling the Google provider:

```yaml
---
fonts:
  provider: none
  sans: Inter
  serif: Instrument Serif
  mono: Fira Code
  weights: '300,400,500,600,700,800,900'
  italic: true
---
```

## Brand colors (tokens)

The palette is provided as CSS variables in `:root` and mapped to semantic tokens (primary, secondary, accent, background, text). You can override in your deck if needed.

## Local development

- Install deps: `pnpm install` (or `npm i`, `yarn`)
- Start dev server: `pnpm dev` → open `http://localhost:3030`
- Build/export: `pnpm build` / `pnpm export`

The sample `slides.md` in this repo can run the theme locally:

```yaml
---
theme: ./
---
```

## Notes

- Vector dots are the default background; no class required.
- Logo automatically switches light/dark based on Slidev dark mode.
- If you add/remove font weights, update `styles/theme.css` @font-face rules to match files under `assets/fonts/`.
