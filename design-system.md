# BrainBridge — Design System

Source of truth for all visual specs (color, type, spacing, components).
Referenced by `CLAUDE.md` — keep this file in sync with `styles.css`.

## Colors

### Brand — deep blue (primary)
| Token | Hex | Use |
|---|---|---|
| `--blue-700` | `#14293D` | Hover / emphasis state for primary color |
| `--blue-600` | `#1C3D5A` | Site-wide primary — logo, nav headings, buttons |
| `--blue-100` | `#EAF0F6` | Icon chip background |
| `--blue-050` | `#F1F5F8` | Section tint (About, article body, related resources) |

### Brand — sage green (accent)
| Token | Hex | Use |
|---|---|---|
| `--green-600` | `#5E8B7E` | Eyebrows, tags, icon strokes, quote borders |
| `--green-100` | `#EBF3EE` | Section tint (Newsletter) |
| `--green-050` | `#EDF3EF` | Reserved |

### Neutrals — warm
| Token | Hex | Use |
|---|---|---|
| `--surface` | `#FBFAF6` | Page shell background (warm white) |
| `--surface-plain` | `#FFFFFF` | Cards, inputs |
| `--surface-alt` | `#FBFCFB` | Contact form input fill |
| `--ink-900` | `#24303A` | Primary text |
| `--ink-600` | `#48586A` | Body text |
| `--ink-500` | `#5A6B78` | Muted / supporting text |
| `--ink-300` | `#93A0A8` | Faint — captions, © |
| `--line` | `#EDEAE3` | Hairline borders, dividers |
| `--line-cool` | `#CDD7DE` | Input / control borders |
| `--bg-page` | `#EEF1F3` | Body background behind the page shell |

### Home hero — local override
The hero section on `index.html` scopes its own palette (via CSS custom
property override on `.hero`, not the global tokens):

| Token | Hex | Use |
|---|---|---|
| `--color-primary` (local) | `#16323D` | Hero heading + "Come In" button + "Join the newsletter" link |
| `--color-primary-strong` (local) | `#0F242C` | Hero button/link hover state |
| Hero background | `#F5F2E9` | Beige band behind the two-column hero |

This is the only place these two hex values are used; everywhere else on the
site continues to use `--blue-600` / `--blue-700` as primary.

### Semantic aliases
```
--color-primary: var(--blue-600);
--color-primary-strong: var(--blue-700);
--color-accent: var(--green-600);
--on-primary: #FFFFFF;
```

## Typography

Fonts loaded via Google Fonts `<link>` in each page `<head>` (not `@import`,
to avoid double-fetching):
`Newsreader:ital,opsz,wght@0,6..72,400;0,6..72,500;0,6..72,600;1,6..72,400`
`Work+Sans:wght@400;500;600`

| Token | Value | Use |
|---|---|---|
| `--font-display` | `"Newsreader", Georgia, "Times New Roman", serif` | Headings, pull quotes, article body copy |
| `--font-body` | `"Work Sans", -apple-system, "Helvetica Neue", Arial, sans-serif` | Nav, buttons, UI text, captions |

Weights: `--fw-regular: 400` · `--fw-medium: 500` · `--fw-semibold: 600`

### Scale
| Token | Size / line-height | Where |
|---|---|---|
| `--fs-hero` / `--lh-hero` | 48px / 1.08 | Hero `<h1>` |
| `--fs-h2` / `--lh-h2` | 40px / 1.15 | Section `<h2>` (Three ways, About, Articles) |
| `--fs-h3` / `--lh-h3` | 22px / 1.3 | Feature card `<h3>` |
| `--fs-lead` / `--lh-lead` | 20px / 1.65 | Hero paragraph, article subtitle |
| `--fs-body` / `--lh-body` | 16px / 1.6 | Feature card body |
| `--fs-small` / `--lh-small` | 15px / 1.6 | Article card excerpt, byline |
| `--fs-eyebrow` / `--ls-eyebrow` | 13px / letter-spacing 0.16em | Eyebrow labels (uppercase) |

Article-page-specific sizes (not tokenized, set directly in `.article-*`
rules): title 46px/1.12, body copy 19px/1.75, body `<h2>` 28px/1.25, pull
quote 23px/1.55.

## Spacing, radii, shadow

| Token | Value |
|---|---|
| `--space-1` … `--space-7` | 8 / 14 / 20 / 28 / 40 / 56 / 84 px |
| `--content-max` | 1200px |
| `--radius-button` | 10px |
| `--radius-card` | 16px |
| `--radius-image` | 18px |
| `--radius-pill` | 999px |
| `--shadow-cta` | `0 14px 28px -10px rgba(28,61,90,.55)` |
| `--shadow-card` | `0 24px 60px -30px rgba(20,41,61,.35)` |
| `--shadow-page` | `0 30px 80px -40px rgba(20,41,61,.40)` |

## Layout

- Page shell: `.shell` — max `min(94vw, 1200px)`, centered, rounded 20px,
  `--shadow-page`, clips overflow. Article page uses `.shell--article`
  (`min(92vw, 1000px)`).
- Grid sections collapse to a single column below **900px**; hero heading
  and a few section titles shrink further below **560px**.

## Components (see `styles.css` for full rules)

- **Buttons** — `.btn` base + `.btn-primary` (filled), `.btn-outline`
  (bordered), `.btn-cta` (larger hero variant). All colors derive from
  `--color-primary` / `--on-primary`, so they follow local overrides (e.g.
  inside `.hero`) automatically.
- **Eyebrow** (`.eyebrow`) — uppercase label, sage green, 13px, letter-spacing
  0.16em. **Tag** (`.tag`) is the smaller 12px/0.1em variant used on article
  cards.
- **Image slot** (`.image-slot` + `.slot-*` modifiers) — dashed placeholder
  for images not yet supplied. Real images (e.g. `hero.webp`) skip this and
  use `.hero-image-img` / plain `<img>` with `--radius-image` instead.
- **Cards** — `.feature-card`, `.article-card` (plain), `.article-card--boxed`
  (bordered, used in "Related resources"), `.contact-card`.
- **Forms** — `.input` (newsletter), `.input-plain` (contact form), both
  `outline: none` with a `--color-primary` focus border.

## Pages

- `index.html` — Hero (two-column: copy + `hero.webp`), Three ways, About,
  Featured articles, Newsletter + contact, Footer.
- `article.html` — Article intro, hero image, body copy, Related resources,
  Footer.
