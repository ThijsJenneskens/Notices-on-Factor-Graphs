# Notices on Factor Graphs — Single-Page Site

A minimal GitHub Pages site (Jekyll + Minima) implemented as a **single page with in-page navigation**.

## Structure
- `_config.yml` — site config (Minima theme)
- `index.md` — the entire site (Agenda, Materials, Contact) as sections with anchors
  - Sticky top menu with smooth scrolling
  - Automatic active-link highlighting via a tiny IntersectionObserver script

## Publish on GitHub Pages
1. Create a public repo (e.g., `notices-on-factor-graphs`).
2. Upload these files to the default branch.
3. In **Settings → Pages**, enable Pages (deploy from a branch).  
4. Done — GitHub Pages builds it with Minima.

## Editing
Edit `index.md`. Menu links: `#agenda`, `#materials`, `#contact`.
