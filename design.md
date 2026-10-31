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

### Color usage rules
- Keep approximately **75–85% of the interface neutral** (white and very light gray).
- Use teal for primary actions and recognizable brand moments.
- Use navy for selected high-contrast areas, especially the footer or one feature section—not every section.
- Use purple sparingly for small brand details.
- Use orange only for occasional emphasis; do not make it a competing primary color.
- Maintain strong text contrast and never rely on color alone to communicate state.

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

## 4. Layout and Spacing

- Use a centered content container with a maximum width of approximately `1200–1280px`.
- Use a consistent spacing scale based on `4px` or `8px`.
- Give major sections generous vertical spacing: approximately `80–120px` on desktop and `56–80px` on mobile.
- Use a grid that collapses cleanly from desktop to mobile.
- Keep content aligned to a consistent page edge.
- Prefer open layouts and fine separators over nested cards and heavy borders.
- Use a modest corner radius: `12–18px` for images and cards, `999px` for pill buttons only when appropriate.
- Avoid excessive shadows; use subtle borders and low-elevation shadows only when needed.

---

## 5. Components

### Navigation
- Clean white or slightly translucent background.
- Logo on the left; only essential links on the right.
- One clear teal contact CTA.
- Sticky navigation is acceptable if compact and unobtrusive.
- Mobile navigation should be simple and accessible.

### Buttons
- Primary: teal background, white text.
- Secondary: transparent or white background with a thin neutral border.
- Use concise labels such as “Call us” and “Get directions”.
- Hover and focus states should be clear but restrained.
- Provide visible keyboard focus indicators.

### Cards
- Use simple surfaces with subtle borders and minimal shadow.
- Avoid overly rounded, floating-card-heavy layouts.
- Service cards may use a small line icon, concise title, and one short description.
- Keep all cards consistent in spacing and alignment.

### Icons
- Use a consistent line-icon set, such as Lucide.
- Keep icons secondary to the content.
- Avoid mixing filled, outlined, and 3D icon styles.

### Imagery and technical graphics
- Prefer genuine photos of surveying instruments, field work, site layouts, mapping, and completed projects.
- Use contour lines, coordinates, grid marks, and drafting lines as subtle decorative layers.
- Technical overlays must not reduce text readability.
- Avoid generic AI-looking equipment imagery where real business photos are available.

---

## 6. Motion and Interaction

- Use motion only to clarify state or create a subtle sense of polish.
- Keep transitions around `150–250ms`.
- Prefer gentle opacity and small translate transitions.
- Avoid parallax-heavy effects, scroll hijacking, constant animation, and elaborate page transitions.
- Respect `prefers-reduced-motion`.
- All interactions must work with keyboard and touch.

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
- Do not invent service claims or credentials.

### About / Why choose us
- Use short, factual copy and real business details.
- Emphasize reliability, precision, experience, and service quality only where supported by the business.

### Projects
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
- Use navy or white, depending on page balance.
- Include logo, key navigation, contact details, and directions.
- Keep it compact and uncluttered.

---

## 8. Tailwind CSS v4 Tokens

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

If using Tailwind CSS v3 instead, translate these tokens into `theme.extend.colors` and `theme.extend.fontFamily` in `tailwind.config.js`.

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
- Preserve teal as the recognizable brand color.
- Use navy, steel blue, and technical graphics in moderation.
- Use real company imagery and verified information.
- Keep copy short, direct, and useful.
- Make phone and directions actions obvious.

### Don't
- Don't make every section dark.
- Don't use orange and purple as competing primary colors.
- Don't overuse gradients, glassmorphism, shadows, or rounded cards.
- Don't cover every surface with grids or contour patterns.
- Don't use multiple display fonts indiscriminately.
- Don't invent services, experience, credentials, reviews, or project results.
- Don't imitate Apple's exact layouts or branding; take inspiration from its restraint, clarity, and polish.

## Final Design Goal

A calm, premium surveying-company website: **Apple-like simplicity, industrial precision, and the original Southern Digital Survey identity**. Every visual element should feel intentional, and the company’s real work should remain the focus.
