# Tshepo Monareng – Portfolio Website

A fully responsive, accessible 4-page personal portfolio website built with plain HTML5 and CSS3. No frameworks, no build tools — just clean, semantic web standards.

---

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero section with background image, about preview, featured projects |
| About | `about.html` | Bio, skills table, circular profile photo |
| Projects | `projects.html` | 6-card project grid with images and descriptions |
| Contact | `contact.html` | Fully accessible contact form |

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
├── Images/
│   ├── hero.jpg
│   ├── Main.png
│   ├── About.png
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

- Semantic HTML5 throughout (header, nav, main, section, article, footer)
- Fully responsive layout using CSS Grid and Flexbox
- Mobile-friendly navigation
- Accessible forms with proper labels, ARIA attributes, and keyboard navigation
- Full-width hero background image with dark gradient overlay
- Circular profile photo on About and Home pages
- Project cards with images, descriptions, and links
- Skills table on About page
- sticky navigation header
- Reduced motion support for accessibility (`prefers-reduced-motion`)
- CSS custom properties (variables) for consistent theming

---

## What Was Fixed & Built

Starting from a 70% complete starter codebase, the following was completed:

- Fixed all duplicate and conflicting CSS rules (3 separate `.hero` blocks merged into one)
- Corrected all image file paths to match actual filenames
- Updated all "Your Name" placeholders to "Tshepo Monareng"
- Fixed broken `resume.html` nav link (page didn't exist — removed)
- Added missing pages: `about.html`, `contact.html`, `projects.html`
- Added full CSS for hero background image, about grid, and project cards
- Fixed footer copyright name
- Added responsive styles for screens under 700px

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Umuzi-skillslab/complete-website-tshepomonareng-web.git
   http://127.0.0.1:5500/contact.html
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
- Accessibility checked with keyboard navigation

---

## Technologies Used

- HTML5
- CSS3 (Grid, Flexbox, Custom Properties)
- Git & GitHub
---

SCREENSHOTS
<img width="1579" height="709" alt="title" src="https://github.com/user-attachments/assets/6b6237cb-960c-46f4-8502-c861b4e029c1" />
<img width="1555" height="477" alt="about" src="https://github.com/user-attachments/assets/3bf32cbe-306d-4265-a062-7ed837a20902" />
 <img width="1479" height="757" alt="cont" src="https://github.com/user-attachments/assets/6547d019-a66a-43b0-8916-f10906c0ae6a" />
<img width="1583" height="772" alt="projects" src="https://github.com/user-attachments/assets/a09d57b5-1964-462c-a06c-896f760bad78" />
<img width="1584" height="771" alt="skills" src="https://github.com/user-attachments/assets/b1517197-e5b5-44c0-b6b6-b455ac149db7" />
<img width="1417" height="623" alt="Screenshot 2026-04-18 083413" src="https://github.com/user-attachments/assets/75f2da99-6fa1-431c-adee-98a7e4dbe1a4" />

## Author

**Tshepo Monareng**  
Aspiring front-end developer | Umuzi  
[GitHub](https://github.com/Umuzi-skillslab/complete-website-tshepomonareng-web)

---

&copy; 2026 Tshepo Monareng. All rights reserved.
