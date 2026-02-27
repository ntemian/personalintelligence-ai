# personalintelligence.ai

## What This Is
Landing pages for personalintelligence.ai — a service that builds personalised AI systems for senior professionals. Static site hosted on GitHub Pages.

**Live URL:** `https://ntemian.github.io/personalintelligence-ai/`
**Repo:** `https://github.com/ntemian/personalintelligence-ai`
**Custom domain:** `personalintelligence.ai` (DNS not yet configured — add CNAME file when ready)

## Target Audience
High-earning professionals in Greece (€200K+):
- Construction company CEOs
- Senior lawyers (defence industry, public sector)
- C-level executives in infrastructure/construction
- Tourism industry operators

They know AI is transformative but have hit the wall with ChatGPT. They need sophisticated, customised systems — not wrappers or slide decks.

## Brand Voice
- **Tone:** Peer who's already done it. Serious, confident, no hype.
- **Copy:** Tight, minimal. Not too many words. No fluff, no buzzwords.
- **No emojis** in the main English page (diamond ♦ icons instead).
- **Trust signals:** 20+ years in AI/knowledge management, government & enterprise clients.

## The Primary Page
`en/index.html` — the main English page we're iterating on. This is the one that matters.

## Key Differentiators (for copy)
1. 20+ years in AI and knowledge management (not a 2024 startup)
2. Systems built for governments and large enterprises
3. Personalised — every system is different because every business is different
4. Continuous upgrades — latest models deployed automatically
5. Direct WhatsApp access — no tickets, no SLAs
6. Data ownership — runs on client's infrastructure
7. We make these people superheroes. They can trust us.

## Project Structure
```
├── index.html              # Root homepage (Greek restaurant — legacy persona)
├── en/
│   └── index.html          # PRIMARY — English page for senior professionals
├── restaurant/
│   ├── index.html          # Greek restaurant persona (legacy)
│   └── en.html             # English restaurant persona (legacy)
├── founder/
│   ├── index.html          # Greek founder persona (legacy)
│   └── en.html             # English founder persona (legacy)
├── shared/
│   └── style.css           # Shared design system
└── CLAUDE.md               # This file
```

## Design System
- Dark theme (`#0a0a0a` background)
- Font: Inter (Google Fonts)
- Accent: `#6366f1` (indigo)
- All CSS in `shared/style.css` — pages link to it, no inline `<style>` blocks
- Mobile responsive
- Fade-up scroll animations via IntersectionObserver

## Navigation Links
All links must be **relative paths** (not absolute like `/en/`). GitHub Pages serves from `/personalintelligence-ai/` subdirectory, so absolute paths break.
- Root files: `./`, `en/`, `restaurant/`, `founder/`
- Subdirectory files: `../`, `../restaurant/`, etc.

## CTAs
All CTAs link to WhatsApp: `https://wa.me/306979088738` with pre-filled text.

## Testimonials
Real clients exist but are confidential. Testimonials are anonymized with realistic details:
- Senior Partner, law firm (defence & public sector)
- CEO, construction company (€20M+ revenue)
- Operations Director, hospitality group (boutique hotels)

## Pricing
Not on the main page. Discussed in person. May add later when numbers are finalised.

## Deployment
- Push to `main` branch → GitHub Pages auto-builds (takes ~30 seconds)
- No build step needed — pure static HTML/CSS/JS
- Verify with: `gh api repos/ntemian/personalintelligence-ai/pages --jq '.status'`

## When Custom Domain Is Ready
1. Configure DNS A records or CNAME for `personalintelligence.ai` → GitHub Pages
2. Add `CNAME` file with content `personalintelligence.ai`
3. Enable HTTPS enforcement via GitHub Pages settings
4. All relative paths will continue to work correctly
