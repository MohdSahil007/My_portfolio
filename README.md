# Mohd Sahil — Data Analyst Portfolio

A static, dependency-free portfolio website built with HTML5, CSS3, and vanilla JavaScript. No frameworks, no build step, no backend — works directly on GitHub Pages.

## File structure

```
portfolio/
├── index.html              → All page content and structure
├── style.css                → All styling (colors, layout, responsive rules)
├── script.js                 → Nav menu, scroll reveal, KPI counters, back-to-top, contact form
├── README.md                 → This file
├── .nojekyll                  → Tells GitHub Pages to skip Jekyll processing
└── assets/
    ├── images/
    │   └── profile.png        → Your profile photo (already included)
    └── resume/
        └── resume.pdf          → Your resume (already included, wired to the Download Resume buttons)
```

## What's already in place

- **profile.png** — your uploaded photo, already placed and linked in the hero section.
- **resume.pdf** — your uploaded resume, already linked to both "Download Resume" buttons (navbar and hero).
- All text content (summary, experience, projects, certifications, skills) is taken directly from your resume. Nothing was invented.

## What you still need to add

### 1. Project screenshots (optional but recommended)
The three project cards currently show a styled placeholder (dashed teal pattern + icon + "Add project-1.jpg" label) instead of a fake image, since no real screenshots were provided.

To add real screenshots:
1. Save your dashboard screenshots as `project-1.jpg`, `project-2.jpg`, `project-3.jpg` (1200×800px recommended).
2. Place them in `assets/images/`.
3. In `index.html`, find each `.project-placeholder` div and replace it with:
   ```html
   <img src="assets/images/project-1.jpg" alt="Interactive Sales Performance Dashboard screenshot" loading="lazy">
   ```
   (repeat for project-2.jpg and project-3.jpg with matching alt text)

### 2. GitHub project links
All three "View on GitHub" buttons currently point to your general GitHub profile (`https://github.com/MohdSahil007/`) since individual repo links weren't provided. If you have separate repos for each dashboard, update the `href` in each `.project-actions` block in `index.html`.

### 3. Contact form behavior
The contact form is static (no backend, as required for GitHub Pages). Right now it opens the visitor's own email client with a pre-filled message via a `mailto:` link. If you'd prefer messages to land directly in your inbox without that step, connect a free service like [Formspree](https://formspree.io) or [EmailJS](https://www.emailjs.com/) — both work with plain HTML forms and require no backend of your own.

## Editing content later

- **Text** — everything is in `index.html`, organized by section with clear comments (`<!-- ===== SECTION ===== -->`).
- **Colors** — all defined once at the top of `style.css` under `:root` (`--teal`, `--coral`, `--bg`, etc.). Change a value there and it updates everywhere.
- **Fonts** — Sora (headings) and Inter (body), loaded from Google Fonts in `index.html`.

## Accessibility & performance notes

- Skip-to-content link, visible keyboard focus states, and semantic HTML (`<nav>`, `<main>`, `<section>`, `<article>`) throughout.
- Respects `prefers-reduced-motion` — animations are disabled for visitors who've turned that on.
- No external JS libraries; `script.js` is under 5KB.
- Project images use `loading="lazy"` once you add them.

---

Deployment to GitHub Pages will be covered in Step 4.
