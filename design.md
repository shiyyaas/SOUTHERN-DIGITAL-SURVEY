# SOUTHERN DIGITAL SURVEY — Design System

## 1. Design Direction

Create a premium, minimal business website for **SOUTHERN DIGITAL SURVEY** that combines:

- **Apple-inspired minimalism:** generous whitespace, clear hierarchy, restrained motion, precise alignment, and purposeful simplicity.
- **Modern surveying / industrial character:** technical imagery, subtle coordinate grids, fine measurement lines, mapping contours, and equipment-focused photography.
- **The existing brand identity:** teal and purple from the logo, supported by deep navy, steel blue, and restrained signal-orange accents from the storefront.

The result should feel like a modern engineering company—not a generic construction template, a cluttered technical dashboard, or an imitation of Apple's website.

### Core principles
1. **Clarity first:** every section has one primary message and one clear action.
2. **Minimal, not empty:** whitespace is intentional; details appear only when they improve understanding.
3. **Technical precision:** consistent spacing, aligned layouts, fine rules, and measured proportions.
4. **Authentic imagery:** prioritize the company's real equipment, office, team, and completed projects.
5. **Brand restraint:** teal is the signature color; navy anchors the interface; orange is used sparingly.
6. **Mobile-first usability:** contact and directions must be easy to access on small screens.
7. **File-based data separation:** presentational layout classes remain decoupled from business text and metadata.

---

## 2. Color System

The values below are representative design tokens inspired by the supplied logo and storefront photo. They are not verified original brand color codes.

### Brand colors
| Token | Hex | Usage |
|---|---|---|
| `brand` | `#087C78` | Primary brand color, links, selected states |
| `brand-dark` | `#006B68` | Hover states, strong teal surfaces |
| `brand-purple` | `#35205F` | Small secondary accents reflecting the logo |
| `brand-light` | `#8CCBC5` | Fine borders, subtle highlights |

### Industrial supporting colors
| Token | Hex | Usage |
|---|---|---|
| `navy` | `#10182B` | Dark hero variant, footer, high-contrast sections |
| `steel` | `#345C7D` | Secondary technical details |
| `blueprint` | `#6BA6C8` | Subtle diagrams, contour lines, visual accents |
| `signal` | `#E87532` | Rare emphasis: key CTA, small status/detail |
| `charcoal` | `#252A32` | Main text on light surfaces |

### Neutral colors
| Token | Hex | Usage |
|---|---|---|
| `white` | `#FFFFFF` | Main page background and cards |
| `surface` | `#F7F8F8` | Quiet alternate section background |
| `surface-muted` | `#F1F3F5` | Secondary panels and subtle dividers |
| `text-secondary` | `#667085` | Supporting copy |
| `border` | `#E4E7EB` | Hairline borders and separators |

---

## 3. Typography

Use a compact font system that balances the narrow, technical feel of the logo with modern readability.

### Font families
- **Headings:** `Rajdhani` — technical, geometric, condensed character.
- **Body:** `Roboto` — neutral, clear, highly readable.
- **Technical labels:** `IBM Plex Mono` — coordinates, small metadata, eyebrow labels.
- **Optional secondary display:** `Barlow Condensed` — use only if a specific display treatment benefits from it; do not mix it into every section.

### Suggested Google Fonts import
```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=Rajdhani:wght@400;500;600;700&family=Roboto:wght@400;500;600;700&display=swap" rel="stylesheet">
```

### Type scale
| Style | Font | Size guidance | Weight | Notes |
|---|---|---|---|---|
| Hero headline | Rajdhani | `clamp(2.8rem, 6vw, 5.5rem)` | 600–700 | Tight line-height, short line lengths |
| H1 | Rajdhani | `clamp(2.5rem, 5vw, 4.5rem)` | 700 | Strong and concise |
| H2 | Rajdhani | `clamp(2rem, 3.5vw, 3rem)` | 600–700 | Section headings |
| H3 | Rajdhani | `1.35rem–1.75rem` | 600 | Cards and subsections |
| Body | Roboto | `1rem–1.125rem` | 400 | Line-height around `1.6–1.75` |
| Small copy | Roboto | `0.875rem` | 400 | Supporting details |
| Eyebrow / technical label | IBM Plex Mono | `0.7rem–0.8rem` | 400–500 | Uppercase, moderate letter spacing |
| Button | Roboto | `0.9rem–1rem` | 500–600 | Clear and readable |

### Typography rules
- Use sentence case for most headings; avoid excessive uppercase.
- Use uppercase only for short eyebrow labels and technical metadata.
- Avoid oversized letter spacing in paragraphs.
- Keep paragraphs narrow and readable.
- Use no more than two primary font families on most screens; IBM Plex Mono is only for small technical details.
- Do not use condensed display fonts for long paragraphs.

---

## 4. File-Based Data Architecture & Dynamic Content Bridge

To maintain clean separation between layout styling and business information, all content is managed in `public/data.json`.

### Schema Guidelines
- **Immutability of styles:** Tailwind utility classes remain defined in `index.html` structure or template fragments.
- **Dynamic Content Injection:** Elements with specific IDs or `data-field` attributes receive text values safely via `element.textContent` or attributes (`href`, `alt`, `src`) without risking HTML injection.
- **Dynamic List Iteration:** Repeating items (Services, Equipment, Fieldwork items) utilize `<template>` elements or container prototypes that preserve all hover styles, transitions, borders, and typography while iterating through JSON records.

### Dynamic Content Flow
1. Page loads with baseline layout scaffolding and accessible fallback structure.
2. `DOMContentLoaded` event triggers client-side fetch targeting `public/data.json`.
3. The content bridge parses JSON payload and binds keys to DOM nodes.
4. If fetch fails (e.g. offline testing without local server), gracefully falls back or logs clear diagnostics without breaking page functionality.

---

## 5. Components

### Imagery and technical graphics
- Prefer genuine photos of surveying instruments, field work, site layouts, mapping, and completed projects.
- Use contour lines, coordinates, grid marks, and drafting lines as subtle decorative layers.
- Technical overlays must not reduce text readability.
- Avoid generic AI-looking equipment imagery where real business photos are available.

---

## 7. Website Visual Direction

### Hero
- Minimal headline, one short supporting sentence, and up to two actions.
- Use a high-quality surveying image or a restrained technical composition.
- Keep the text readable and the primary CTA obvious.
- Do not crowd the hero with badges, statistics, or multiple competing buttons.

### Services
- Present only services confirmed by the business.
- Use a clean grid with concise copy and restrained line icons.
- Rendered cleanly via dynamic iteration from `public/data.json`.

### About / Why choose us
- Use short, factual copy and real business details.
- Emphasize reliability, precision, experience, and service quality only where supported by the business.

### Projects & Fieldwork
- Prefer real project photographs with short captions.
- Use a clean gallery rather than decorative image collages.

### Reviews
- Use only genuine customer reviews and preserve their meaning.
- Do not fabricate testimonials, star ratings, or customer names.

### Contact
- Make the phone number, office address, opening hours, and map directions easy to find.
- Use tap-to-call links on mobile.
- Verify all business details before publishing.

### Footer
- Use navy or dark ink depending on page balance.
- Include logo, key navigation, contact details, and directions.
- Keep it compact and uncluttered.

---

## 8. Tailwind CSS Tokens

Use these tokens as the single source of truth. Do not introduce arbitrary colors throughout components without a clear reason.

```css
@import "tailwindcss";

@theme {
  --color-brand: #087C78;
  --color-brand-dark: #006B68;
  --color-brand-purple: #35205F;
  --color-brand-light: #8CCBC5;

  --color-navy: #10182B;
  --color-steel: #345C7D;
  --color-blueprint: #6BA6C8;
  --color-signal: #E87532;

  --color-white: #FFFFFF;
  --color-surface: #F7F8F8;
  --color-surface-muted: #F1F3F5;
  --color-text: #252A32;
  --color-text-secondary: #667085;
  --color-border: #E4E7EB;

  --font-heading: "Rajdhani", sans-serif;
  --font-body: "Roboto", sans-serif;
  --font-technical: "IBM Plex Mono", monospace;
  --font-secondary: "Barlow Condensed", sans-serif;
}
```

---

## 9. Accessibility and Quality

- Meet WCAG AA contrast targets where practical.
- Use semantic HTML landmarks and a logical heading hierarchy.
- Add meaningful alt text to informative images; use empty alt text for decorative graphics.
- Ensure visible keyboard focus and accessible mobile navigation.
- Use appropriately sized touch targets.
- Optimize images and avoid layout shifts.
- Keep page load fast; avoid unnecessary libraries.
- Test at narrow mobile widths, tablet, and desktop.
- Check reduced-motion preferences.

---

## 10. Do / Don't

### Do
- Keep layouts spacious, calm, and precise.
- Preserve brand colors and technical styling.
- Rely on `public/data.json` for content updates.
- Keep copy short, direct, and useful.
- Make phone and directions actions obvious.

### Don't
- Don't make every section dark.
- Don't hardcode business text in markup when it belongs in `data.json`.
- Don't overuse gradients, glassmorphism, shadows, or rounded cards.
- Don't cover every surface with grids or contour patterns.
- Don't use multiple display fonts indiscriminately.
- Don't invent services, experience, credentials, reviews, or project results.
