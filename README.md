# Tshepo Monareng – Portfolio Website

A fully responsive, accessible 4-page personal portfolio website built with plain HTML5 and CSS3. No frameworks, no build tools — just clean, semantic web standards.

---

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero section with background image, about preview, featured projects |
| About | `about.html` | Bio, skills table, circular profile photo |
| Projects | `projects.html` | 6-card project grid with images and descriptions |
| Contact | `contact.html` | Fully accessible contact form with validation |

---

## Project Structure

```
portfolio/
├── index.html
├── about.html
├── projects.html
├── contact.html
├── css/
│   └── styles.css
├── images/
│   ├── hero.jpg
│   ├── Main.png
│   ├── About.png
│   ├── image 1.jpg
│   ├── image 2.jpg
│   ├── image 3.jpg
│   ├── Project 1.jpg
│   ├── Project2.jpg
│   ├── Project 3.jpg
│   ├── Project 4.jpg
│   ├── Project 5.jpg
│   └── Project 7.jpg
└── README.md
```

---

## Features

- Semantic HTML5 throughout (`header`, `nav`, `main`, `section`, `article`, `figure`, `figcaption`, `footer`)
- Fully responsive layout using CSS Grid and Flexbox
- Mobile-friendly navigation with responsive breakpoints (768px, 480px)
- Accessible forms with labels, ARIA attributes, fieldset/legend grouping, and keyboard navigation
- Inline JavaScript form validation with accessible error messages (`role="alert"`, `aria-live="polite"`)
- Full-width hero background image with dark gradient overlay
- Circular profile photo wrapped in `<figure>` + `<figcaption>` on About and Home pages
- Project cards with images, descriptions, and links
- Skills table on About page with `<caption>`, `<thead>`, `<tbody>`, and `scope` attributes
- Sticky navigation header with active page highlighting
- Reduced motion support (`prefers-reduced-motion`)
- CSS custom properties (variables) for consistent theming
- Skip-to-content link for keyboard users

---

## What Was Fixed & Built

### Round 1 – Initial Build
Starting from a 70% complete starter codebase, the following was completed:

- Fixed all duplicate and conflicting CSS rules (3 separate `.hero` blocks merged into one)
- Corrected all image file paths to match actual filenames
- Updated all "Your Name" placeholders to "Tshepo Monareng"
- Fixed broken `resume.html` nav link (page didn't exist — removed)
- Added missing pages: `about.html`, `contact.html`, `projects.html`
- Added full CSS for hero background image, about grid, and project cards
- Fixed footer copyright name
- Added responsive styles for screens under 700px

### Round 2 – Feedback Fixes (v2.0)

#### HTML Structure & Semantics
- Added `<meta name="description">` to all four pages (was missing site-wide)
- Wrapped all profile photos in `<figure>` + `<figcaption>` for semantic correctness
- Replaced all inline `style=""` attributes with dedicated CSS classes
- Standardised image folder reference to lowercase `images/` across all HTML files

#### Navigation & Linking
- Added `.active` CSS class and `aria-current="page"` attribute to the correct nav link on every page
- Verified all internal links resolve correctly across all four pages
- Styled active nav state with accent colour and background highlight

#### Images & Alt Text
- Improved all `alt` attributes to be descriptive and context-specific (e.g. `"Responsive landing page showing a clean mobile-first layout with CSS Grid"` instead of `"Project One screenshot"`)
- Added `<figcaption>` (visually hidden) to profile photos for screen reader context

#### Forms & Accessibility (contact.html)
- Wrapped related fields in `<fieldset>` + `<legend>` groups ("Your Details" and "Your Enquiry")
- Added new input types: `date` (availability), `tel` with `pattern`, `checkbox` group (services), and `url`
- Added `minlength` and `pattern` validation attributes to name, email, phone, and message fields
- Added `aria-required="true"` to all required fields
- Added `aria-describedby` linking each input to its error message and hint text
- Added `<span class="field-error">` with `role="alert"` and `aria-live="polite"` for accessible inline errors
- Added `<span class="field-hint">` for helper text (e.g. phone format, minimum character count)
- Added JavaScript blur + submit validation with `aria-invalid` toggling
- Replaced inline `style=""` on submit button with proper `.btn` class

#### Skills Table (about.html)
- Added `<caption>` describing the table's purpose (was missing)
- Confirmed `<thead>`, `<tbody>`, `<th scope="col">`, and `<td>` all present and correctly structured

#### CSS Styling & Selectors
- Fixed nav hover contrast — changed from failing `#f0c040` on `#555555` to `#e8e8ec` on dark background (passes WCAG AA 4.5:1)
- Added CSS pseudo-elements (`::before`) for decorative accent lines on section headings
- Expanded selector coverage: ID selector (`#contact-form`), attribute selector (`th[scope="col"]`), `:nth-child(even)` zebra striping, `:last-child` border removal, `:focus-visible`, `:active`, `:disabled`
- Added `.btn:disabled` state with reduced opacity and `cursor: not-allowed`

#### Layout & Responsiveness
- Added `@media (max-width: 768px)` — stacked nav, single-column grid, column-direction about section
- Added `@media (max-width: 480px)` — tighter spacing, full-width buttons, smaller table font
- Added `@media (prefers-reduced-motion: reduce)` — disables all transitions and animations
- Added `.visually-hidden` utility class used on `<figcaption>` elements

#### Code Quality & Organisation
- Full CSS rewrite with 14 clearly labelled sections and consistent comments
- All CSS uses custom properties from `:root` for colours, spacing, typography, and transitions
- Removed all inline styles from HTML; moved everything to `styles.css`

---

## Known Issues Log

| # | File | Issue | Fix Applied |
|---|------|-------|-------------|
| 1 | All pages | Missing `<meta name="description">` | Added to all 4 pages |
| 2 | All pages | No active state on nav links | Added `.active` + `aria-current="page"` |
| 3 | All pages | Inline `style=""` attributes throughout | Moved to CSS classes |
| 4 | `index.html` | Profile image not in `<figure>` | Wrapped in `<figure>` + `<figcaption>` |
| 5 | `about.html` | Skills table missing `<caption>` | Added descriptive caption |
| 6 | `about.html` | Profile image not in `<figure>` | Wrapped in `<figure>` + `<figcaption>` |
| 7 | `contact.html` | No `<fieldset>` / `<legend>` grouping | Added two fieldset groups |
| 8 | `contact.html` | Only 3 input types (text, email, textarea) | Added `date`, `tel`, `url`, `checkbox`, `select` |
| 9 | `contact.html` | No `minlength` or `pattern` validation | Added to name, email, phone, message |
| 10 | `contact.html` | No accessible error messages | Added `role="alert"` + `aria-live` spans |
| 11 | `contact.html` | No `aria-required` or `aria-describedby` | Added to all required fields |
| 12 | `contact.html` | No JS validation feedback | Added blur + submit validation script |
| 13 | `projects.html` | Generic `alt` text on all images | Replaced with descriptive alt text |
| 14 | `css/styles.css` | Nav hover colour fails WCAG AA contrast | Fixed to high-contrast dark theme colours |
| 15 | `css/styles.css` | No responsive media queries | Added 768px and 480px breakpoints |
| 16 | `css/styles.css` | No `prefers-reduced-motion` rule | Added with motion-safe fallbacks |
| 17 | `css/styles.css` | Limited pseudo-class and selector variety | Added `::before`, `:nth-child`, `:last-child`, `[attr]` selectors |
| 18 | `css/styles.css` | No `.visually-hidden` utility | Added for accessible hidden text |

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Umuzi-skillslab/complete-website-tshepomonareng-web.git
   cd complete-website-tshepomonareng-web
   ```
2. Open `index.html` in your browser — no server needed.

Or open with VS Code Live Server:
1. Install the **Live Server** extension in VS Code
2. Right-click `index.html` → **Open with Live Server**

---

## Validation

- HTML validated with [W3C Markup Validator](https://validator.w3.org/)
- CSS validated with [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)
- Tested in Chrome and Firefox
- Accessibility checked with keyboard navigation and screen reader
- Colour contrast verified against WCAG 2.1 AA (4.5:1 minimum)

---

## Technologies Used

- HTML5
- CSS3 (Grid, Flexbox, Custom Properties, Pseudo-elements)
- Vanilla JavaScript (form validation)
- Git & GitHub

---

## Author

**Tshepo Monareng**  
Aspiring front-end developer | Umuzi  
[GitHub](https://github.com/Umuzi-skillslab/complete-website-tshepomonareng-web)

---

&copy; 2026 Tshepo Monareng. All rights reserved.
