# Lightloom Stories — Setup Guide

## 1. Put it live (GitHub Pages + Cloudflare)

1. Create a GitHub repository (e.g. `lightloomstories`).
2. Upload `index.html` to the repository root (and later an `images/` folder).
3. In the repo: **Settings → Pages → Source: Deploy from branch → main → / (root)** → Save.
4. Still in Pages settings, set **Custom domain** to `lightloomstories.com`.
5. In Cloudflare DNS for lightloomstories.com, add:
   - `A` records for `@` → 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153
   - `CNAME` record for `www` → `<your-github-username>.github.io`
6. Back in GitHub Pages, tick **Enforce HTTPS** once the domain verifies (can take ~15–60 min).

## 2. Customize — search the file for "EDIT ME"

Every spot you must personalize is marked with a `▸ EDIT ME` or `▸ REPLACE` comment:

- [ ] **Your name** in the story section signature
- [ ] **Location** in the hero eyebrow + meta keywords (currently "Newark, Delaware")
- [ ] **Instagram URL** in the contact section (currently a placeholder)
- [ ] **Email** in the contact section (currently hello@lightloomstories.com)
- [ ] **Pixieset URL** on the "Open client galleries" button
- [ ] **Testimonials** — placeholders included; swap in real ones as they arrive

## 3. Add your photos

1. Create an `images/` folder in the repo.
2. Export photos as JPG, longest side ~2000px, quality ~80 (keeps the site fast).
3. Replace each placeholder block like this:

   Before:
   `<div class="ph hero-photo"><span class="ph-label">Your hero photo</span></div>`

   After:
   `<img src="images/hero.jpg" alt="A family laughing together at golden hour" class="hero-photo">`

   Do the same for the story photo and the six portfolio tiles
   (`folio-1.jpg` … `folio-6.jpg`). Write a short, honest `alt` text for each —
   good for accessibility and Google.

## 4. Tips

- **Pixieset free plan**: your client galleries live at `yourname.pixieset.com` —
  paste that exact URL on the galleries button.
- **Journal**: the three post cards are starter ideas. When you write a post,
  create e.g. `journal/ordinary-tuesdays.html` and point the card's link to it.
- **Instagram first**: pin your best 9 photos there — the site sends people to your DM.
