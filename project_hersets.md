---
name: project-hersets
description: "HerSets landing page — tech stack, file layout, key sections, deployment, and integrations"
metadata:
  node_type: memory
  type: project
  originSessionId: 03e9b681-b6a1-45e3-bb3d-17cd34dbf05b
  modified: 2026-10-06T01:33:18.009Z
---

Static HTML/CSS/JS landing page deployed to GitHub Pages from the `master` branch.

**Why:** Marketing site for the HerSets iOS app. No framework — pure HTML files.

**How to apply:** All edits are direct file edits. No build step. Changes go live after a git push to master.

## Key files
- `index.html` — main landing page (all sections, nav, hero, features, etc.)
- `faq.html` — standalone FAQ page (SEO-optimised, JSON-LD schema)
- `legal/` — Privacy Policy, Terms of Service, Account Deletion, Cookie Policy, Support Contact
- `screenshots/` — app screenshot PNGs used in phone mockups
- `assets/logo/` — logo files: `hersets_h_standalone_transparent.png` (nav icon), `hersets_logo_transparent.png` (footer wordmark)

## Tech stack
- **Bilingual**: `data-en` / `data-uk` attributes + `setLang()` JS + `body.lang-uk` class; `uk-namu` class for Namu font in Ukrainian mode
- **Fonts**: Inter Tight + Inter (main); Namu (Ukrainian mode)
- **CSS variables**: `--bg`, `--ink`, `--pink`, `--pink-d`, `--pink-l`, `--pink-m`, `--pink-m`, `--border`, `--sage`, `--white`, etc.
- **Phone mockups**: `.iphone-sm` class, `--sw` CSS variable controls width; height via `calc(var(--sw) * 6.47 / 3.07)`
- **Analytics**: HeyCatch SDK v0.7.0 via `https://esm.sh/@heycatch/sdk@0.7.0`, project key `hck_pk_7_e8a0esbF0G3RS-2_0_TWz_qMaSM3jN`, installed in `<head>` of all 7 HTML files with `requestBatching: false`

## Page sections (index.html, top to bottom)
1. Hero — "I'm not a tech, I'm an artist." + Today screen phone + App Store CTA
2. Ticker
3. The App (`#app`) — "Every detail. Remembered." + 5 discipline phones
4. Templates (`#templates`) — Five built-in templates
5. Template Builder (`#builder`) — "Build it your way."
6. Salon View (`#salon`) — "Every chair. Every artist. One screen." (dark bg)
7. Specialties — "You do more than one thing."
8. Manifesto (`#manifesto`) — "Your client details are everywhere." (problem section)
9. Features (`#features`) — "Everything you need. Nothing you don't." (dark bg)
10. Testimonials
11. Mini FAQ — 4 quick answers + "See all questions →" link to faq.html
12. Download (`#download`) — App Store CTA (pink bg)
13. Footer

## Nav behaviour
- Transparent by default; background transitions to match section color on scroll
- Dark sections (Salon View, Features): nav links turn white
- Pink section (Download): nav links + CTA go white
- Active link highlights in `--pink-d` color
- Trigger offset: 80px ahead of section so transition leads slightly

## Legal docs
- Governing law: California (OLROM LLC)
- SMS provider: Infobip (TCPA/CTIA compliant)
- Last updated: August 17, 2026
