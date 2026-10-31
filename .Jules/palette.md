# Palette's Journal - Critical UX & Accessibility Learnings

## 2025-10-31 - Static Tailwind Landings Keyboard & ARIA Hygiene
**Learning:** Single-page static brochure sites often rely heavily on fixed header navigation without a `<main>` landmark or skip navigation link, forcing keyboard users to tab through entire topbars and navigation menus on every page view. Furthermore, mobile slide-out navigation drawers frequently miss ARIA disclosure states (`aria-expanded`, `aria-controls`) and the expected `Escape` key close listener.
**Action:** Always provide a high-contrast, focus-visible skip link targeting `<main id="main-content">` and wire hamburger toggle buttons with `aria-expanded`, icon state transitions, and `Escape` key dismissal.
