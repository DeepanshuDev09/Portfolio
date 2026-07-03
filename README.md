# Deepanshu Joshi — Portfolio

A single-page developer portfolio built as one self-contained HTML file — no build step, no dependencies to install. Just open it in a browser.

**Live preview:** open `index.html` directly, or deploy it (see below).

---

## About this site

A dark, terminal-inspired portfolio for a CS graduate with a background in Web3/crypto operations, Android development, and full-stack web (React/Node). The design leans into that identity:

- A **terminal window** in the hero that types out and cycles through roles (`frontend developer`, `android developer`, `problem solver`, `web3 developer`)
- Work experience laid out as a **commit log**, styled like `git log` output
- Skill groups organized like a config file: Languages, Web Development, Web3 & Operations, Mobile & Debugging

## Structure

```
.
├── index.html   → entire site: markup, styles, and scripts in one file
└── README.md    → this file
```

Everything — HTML, CSS, and JavaScript — lives in `index.html`. There's nothing to `npm install`.

## Sections

| Section | What's there |
|---|---|
| Hero | Name, tagline, cycling role terminal, open-to-work badges |
| About | Bio, CGPA, quick stats |
| Experience | Android internship + freelance Web3/crypto work, as a commit log |
| Skills | Languages, Web Development, Web3 & Operations, Mobile & Debugging |
| Education | Don Bosco Institute of Technology, B.Tech CS, 9.2 CGPA |
| Contact | Email + social links |

## Before you publish

A few placeholders still need your real info — search `index.html` for these:

- [ ] `your.email@example.com` → your actual email (in the Contact section)
- [ ] The `LinkedIn` and `GitHub` buttons currently link to `#` → add your profile URLs
- [ ] Add a **Projects** section if you want to showcase specific repos (structure suggestion below)

## Customizing

- **Colors** — all defined as CSS variables at the top of the `<style>` block (`:root { --bg, --surface, --amber, --blue, ... }`). Change them once, they apply everywhere.
- **Fonts** — Space Grotesk (headings), Inter (body), JetBrains Mono (terminal/labels/tags), loaded from Google Fonts in the `<head>`.
- **Terminal roles** — edit the `roles` array near the bottom of the file, inside the `<script>` tag:
  ```js
  const roles = [
    "frontend developer",
    "android developer",
    "problem solver",
    "web3 developer"
  ];
  ```
- **Experience entries** — each is a `.commit` block inside `<section id="experience">`. Copy the block to add a new role.

## Deploying

Since it's a static single file, any of these work in a few minutes:

**GitHub Pages**
1. Push this repo to GitHub.
2. Repo → Settings → Pages → set source to the `main` branch, root folder.
3. Your site will be live at `https://<username>.github.io/<repo-name>/`.

**Netlify / Vercel**
1. Drag and drop the folder onto [netlify.com/drop](https://app.netlify.com/drop), or connect the repo on Vercel.
2. No build command needed — it's static HTML.

**Any static host**
Just upload `index.html`. That's the whole site.

## Browser support

Uses modern but widely-supported CSS (custom properties, `backdrop-filter`, CSS Grid) and vanilla JS (`IntersectionObserver`). Works in current versions of Chrome, Firefox, Safari, and Edge. Respects `prefers-reduced-motion` for anyone with motion sensitivity.

---

Built by Claude, for Deepanshu Joshi.
