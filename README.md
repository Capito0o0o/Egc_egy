# 🏗️ EGC El Gezawy Construction Website

Complete responsive multi-page website for EGC (El Gezawy Construction) — an Egyptian construction and finishing company.

## 📄 Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero, badges, about teaser, services, projects, why us, CTA |
| Services (hub) | `services.html` | 16 service cards linking to full individual pages |
| Services (detail) | `services/*.html` | 16 standalone SEO-optimized landing pages — one per service, each with a hero image, sales copy, feature grid, process steps, FAQ (with schema), CTA band, and links to related services |
| Projects | `projects.html` | 12 projects with category filter — click any card to open a detail popup |
| About | `about.html` | Company story, stats counter, team, vision & mission |
| Contact | `contact.html` | Working contact form, contact info, embedded Google Map |

### The 16 services

`villa-finishing`, `electrical-works`, `plumbing-works`, `plastering-works`, `gypsum-decor`, `flooring-works`, `painting-works`, `carpentry-works`, `aluminum-glass`, `interior-design`, `project-management`, `landscaping`, `fences-entrances`, `gates-entrances`, `interlock-paving`, `hashimi-stone`

## 🎨 Design System

- **Colors:** Gold (#C9A258), Navy Dark (#0B1120)
- **Font:** Cairo (Google Fonts)
- **Direction:** Arabic RTL
- **Framework:** Pure HTML + CSS + Vanilla JS (no dependencies)

## 🚀 Deploy to GitHub Pages

1. Create a new repository on GitHub
2. Upload the 5 root HTML files, the `services/` folder (16 files inside), and the `assets/` folder — keep the folder structure intact
3. Make sure the empty file named `.nojekyll` is included in the root (prevents Jekyll from interfering with plain HTML)
4. Go to **Settings → Pages** → Source: "Deploy from a branch" → Branch: `main` / `(root)`
5. Your site will be live at: `https://yourusername.github.io/repo-name/`

> If a deployment ever fails with **"Deployment failed, try again later"**, this is a known, temporary GitHub-side issue — not a problem with the files. Toggling Source to "GitHub Actions" and back to "Deploy from a branch" in Settings → Pages usually resolves it, or simply retry after a few minutes.

## 📱 Responsive Breakpoints

- Desktop: > 1100px
- Tablet: ≤ 1100px / ≤ 900px
- Mobile: ≤ 600px

## ✅ Features

- [x] Fixed navbar with scroll effect + mobile hamburger menu
- [x] All 16 standalone, SEO-optimized service pages (`services/*.html`) live — each with unique meta title/description, Open Graph tags, Service + BreadcrumbList + FAQPage schema.org markup, sales-copy intro, feature grid, 4-step process, FAQ, CTA band, and related-services cross-links
- [x] Footer service links point to the actual individual service pages (not just the hub)
- [x] 12 project cards with category filter, each opening a detail popup (image, category, location, year, description)
- [x] Animated stats counter (IntersectionObserver)
- [x] Contact form that actually sends submissions via [FormSubmit](https://formsubmit.co) — no backend required
- [x] Embedded Google Map on the contact page
- [x] Shared placeholder graphic extracted to `assets/placeholder-service.svg` (previously inlined 14 times across pages — now a single reusable file, smaller page weight)
- [x] Full SEO meta tags (per page)
- [x] Schema.org JSON-LD
- [x] Open Graph / Twitter Cards
- [x] Semantic HTML structure
- [x] All internal links verified — no broken hrefs/srcs anywhere in the site

## ⚙️ Before going live — update these placeholders

| What | Where | Current placeholder |
|------|-------|----------------------|
| Phone / WhatsApp | all pages (footer, contact page, `tel:`/`wa.me` links) | `01000725551` |
| Contact form destination email | `contact.html` (form `action` + JS `fetch` URL) | `ahmed.capito@gmail.com` |
| Facebook / Instagram links | footer + contact page | `#` (not linked yet) |
| Exact company address | `contact.html` map embed | generic "Cairo, Egypt" |
| Real project & team photos | `services.html`, `services/*.html`, `projects.html`, `about.html` | Unsplash stock photos (reused across pages) + one shared placeholder SVG — swap for real project photos when available |

**Note on the contact form:** the first time someone submits it, FormSubmit sends a one-time confirmation email to the destination address — it must be clicked once to activate delivery of future submissions.

**Note on images:** a real project-photo album was shared for this project, but it's hosted on Google Photos, which serves images via JavaScript and doesn't expose stable direct-download links through automated fetching. To use those photos on the site, download them (individually or as a zip via Google Photos' "Download all") and upload them here, or add them directly to the `assets/` folder before deploying.
