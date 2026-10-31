# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack
HTML, CSS, JavaScript, Tailwind CSS (v4 CDN), Centralized JSON Data Layer (`public/data.json`)

## Users
Property owners, real estate developers, engineers, and individuals in Aluva and across Kerala requiring professional land measurement and surveying services.

## Product Purpose
To provide a polished, responsive digital presence for Southern Digital Surveyors, communicating professional precision, trust, and modern surveying expertise.

## Positioning
Total land survey solutions anchored in Aluva, Kerala, offering accurate Total Station surveys, boundary demarcations (including Nilam and Purayidam), plot division, and contour mapping with authentic equipment and local presence.

## Operating Context
Clients visiting on mobile or desktop seeking reliable contact numbers, office directions in Aluva, and clear descriptions of land surveying services.

## Architecture & Data Separation
The application uses File-Based Data Separation to decouple static presentational HTML from business domain information:
- **Central Data Source**: All copy, service definitions, equipment inventory, fieldwork metadata, and contact credentials live in `public/data.json`.
- **Dynamic Content Hydration**: On `DOMContentLoaded`, a client-side vanilla JavaScript bridge loads `public/data.json`, securely populates text elements through descriptive data/ID bindings, and renders repeating components (services grid, equipment showcases, fieldwork galleries) using clean DOM cloning and safe `textContent` injection.
- **Design Stability**: Tailwind CSS utility classes and visual scaffolding in `index.html` remain fully intact, preventing layout shifts or visual degradation while making content updates zero-markup operations.

### Data Schema Overview
`public/data.json` provides structured contracts across key modules:
- `company`: Name, tagline, location label, registration/established details.
- `contact`: Primary phone, display phone, WhatsApp number, email address, physical address lines, GPS coordinates, and Google Maps link.
- `businessHours`: Weekday and weekend operating hours.
- `hero`: Eyebrow badge, main headline, narrative description, action button labels/targets, and featured operational tag.
- `services`: Array of 8 official surveying services, each featuring an index code, category badge, service title, description, and key badge text.
- `about`: Firm heading, descriptive paragraphs, and highlight statistics/cards.
- `equipment`: Array of hardware instruments featuring instrument tag, title, description, image path, and alt text.
- `fieldwork`: Array of real fieldwork operational photos with phase tag, project title, image path, and alt text.

## Capabilities and Constraints
- Complete catalog of 8 surveying services rendered dynamically from data source.
- Real business photos of team, owner, and surveying equipment stored in asset paths.
- Tap-to-call and map directions wired directly from centralized contact data.
- Strict adherence to design tokens from design.md.
- Zero external client framework dependencies (pure standard DOM API).

## Brand Commitments
- Business Name: SOUTHERN DIGITAL SURVEYORS
- Tagline: TOTAL LAND SURVEY SOLUTIONS
- Primary Brand Color: Teal (#087C78)
- Typography: Rajdhani, Roboto, IBM Plex Mono

## Evidence on Hand
- Company visiting card and brand assets.
- Real photographs in `Public/`.

## Product Principles
1. Technical precision and Apple-inspired minimalism.
2. Complete authenticity without fabricated statistics or testimonials.
3. Instant accessibility for mobile users (tap-to-call and directions).
4. Strict separation of concerns between presentation and content data.

## Project Progress & Status
- [x] Initial design system and brand tokens specified in `design.md`.
- [x] Static HTML layout created with Tailwind CSS v4 and Google Fonts.
- [x] Responsive navigation with accessible mobile drawer and keyboard traps.
- [x] Architecture shift: File-Based Data Separation implemented.
- [x] Central schema compiled into `public/data.json`.
- [x] Dynamic JavaScript loader and DOM hydration bridge wired into `index.html`.
- [x] Responsive and visual consistency checks verified.
