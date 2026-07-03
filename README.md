# My Pet Grace
### A Faith-Inspired Pet Care & Pet Loss Support Platform

> "A righteous man cares for the needs of his animal." — Proverbs 12:10

**Live Demo:** Deploy to Cloudflare Pages in under 2 minutes (see deployment guide)  
**Stack:** React 19 + Vite 6 + Cloudflare Pages  
**Niche:** Pet care + pet loss grief support — 90.5M+ US pet-owning households  

---

## What's Included

A complete, production-ready digital business. Source code, buyer documentation, deployment guides, and a monetization roadmap — everything a buyer needs to take this live and earning.

### Pages (12 total)
- **Home** — Hero, features, testimonials, newsletter capture
- **Tools** — Quality of Life Assessment, grief stages, memorial creator, resource library
- **AI Pet Advisor** — Claude API integration with pet-specific persona
- **Resources** — 20+ affiliate partner categories, pre-researched commission rates
- **Blog** — 6 original long-form articles (1,500–2,500 words each)
- **About, FAQ, Contact** — Fully written, no placeholder content
- **Legal Suite** — Privacy Policy, Terms of Service, Disclaimer, Affiliate Disclosure

### Features
- **Quality of Life Assessment Tool** — unique to this platform, not found on competing pet sites
- **AI Pet Advisor** — working Claude API integration, pet-specific system prompt
- **Grief Support Center** — 6-stage grief framework with compassionate, faith-anchored content
- **Pet Memorial Creator** — interactive memorial tool
- **AdSense placeholders** — pre-positioned on Home and Resources pages
- **Newsletter capture** — styled form ready for Mailchimp or Kit integration
- **Dark/Light mode** — CSS variable system, localStorage persistence
- **Cookie consent banner** — GDPR-aware
- **Community board** — local pet community feature

### Monetization (Ready to Activate)
| Stream | Partners | Est. Commission |
|---|---|---|
| Affiliate — Food | Chewy, Ollie, JustFoodForDogs | 4–28% |
| Affiliate — Insurance | Embrace, Lemonade | Per lead |
| Affiliate — Health | 1800PetMeds, HolistaPet | 15–35% |
| Affiliate — Subscription | BarkBox, Farmer's Dog | $15–25/sale |
| Affiliate — Memorial | Pet Perennials | 15% |
| Display Ads | Google AdSense → Mediavine | $8–$15 CPM |
| Digital Products | Grief journal, pet care binder | $9–$47 |

### SEO
- Dynamic meta tags per page (title, description, canonical)
- Open Graph + Twitter Card on every page
- JSON-LD structured data
- `robots.txt` and `sitemap.xml` included
- Google Fonts optimized with `preconnect`

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 19 |
| Build Tool | Vite 6 |
| Routing | React Router v7 |
| Styling | CSS Variables + CSS Modules |
| Icons | Lucide React |
| Notifications | React Hot Toast |
| AI | Anthropic Claude API (claude-sonnet-4-6) |
| Hosting | Cloudflare Pages (free tier) |
| DNS | Cloudflare DNS |
| Domain | Cloudflare Registrar (recommended) |

---

## Folder Structure

```
pet-grace/
├── public/
│   ├── favicon.svg
│   ├── robots.txt
│   ├── sitemap.xml
│   └── manifest.json
├── src/
│   ├── components/
│   │   ├── calculators/     # Quality of Life tool
│   │   ├── layout/          # Navbar, Footer
│   │   ├── sections/        # Hero, Features, Newsletter, Testimonials
│   │   └── ui/              # AdSense, CookieBanner, SiteNotice, BackToTop
│   ├── data/
│   │   ├── siteData.js      # All editable content — affiliates, FAQs, grief stages
│   │   └── blogPosts.js     # All 6 blog posts
│   ├── hooks/
│   │   ├── useTheme.jsx     # Dark/light mode context
│   │   └── useScrollReveal.js
│   ├── pages/               # All 12 pages
│   └── styles/
│       ├── variables.css    # All colors and fonts — edit here to rebrand
│       └── global.css
├── index.html               # SEO meta, OG tags, structured data
├── vite.config.js
└── BUYER/                   # Complete buyer documentation package
    ├── README.md
    ├── WHATS_INCLUDED.md
    ├── TRANSFER_CHECKLIST.md
    ├── DEPLOYMENT_GUIDE.md
    ├── CHANGELOG.md
    └── ROADMAP.md
```

---

## Installation

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/my-pet-grace.git
cd my-pet-grace

# Install dependencies
npm install

# Start development server
npm run dev
# → http://localhost:5173

# Build for production
npm run build

# Preview production build locally
npm run preview
```

---

## Environment Variables

The AI Pet Advisor requires an Anthropic API key.

Create a `.env.local` file in the project root:

```
VITE_ANTHROPIC_API_KEY=sk-ant-your-key-here
```

Get your key at: https://console.anthropic.com

In Cloudflare Pages, add this under:
**Settings → Environment Variables → Production**

---

## Cloudflare Pages Deployment

See `BUYER/DEPLOYMENT_GUIDE.md` for the complete step-by-step guide.

**Quick start:**
1. Push code to GitHub
2. Go to dash.cloudflare.com → Workers & Pages → Create → Pages
3. Connect your GitHub repository
4. Set build command: `npm run build`
5. Set output directory: `dist`
6. Click Deploy

**Live in under 2 minutes.** Free hosting. Automatic SSL. Global CDN.

---

## Custom Domain

Cloudflare offers domain registration at cost (no markup) through Cloudflare Registrar.

1. Search for your domain at: dash.cloudflare.com → Domain Registration
2. Register and it's automatically on Cloudflare DNS
3. In Pages → Custom Domains → add your domain
4. SSL certificate provisions automatically

---

## How to Edit Content

**All affiliate links, FAQs, testimonials, and grief stages:**
→ `src/data/siteData.js`

**All blog posts:**
→ `src/data/blogPosts.js`

**Colors, fonts, brand identity:**
→ `src/styles/variables.css`

**After any edit:**
```bash
git add .
git commit -m "describe your change"
git push origin main
# Cloudflare Pages auto-deploys in ~60 seconds
```

---

## Transfer Guide

See `BUYER/TRANSFER_CHECKLIST.md` for the complete transfer process.

**Summary:** GitHub repository transfer + Cloudflare Pages project transfer. Takes under 30 minutes. Zero downtime.

---

## License

MIT License — buyer receives full ownership and may use, modify, and resell freely.

---

## Support

Code is clean, well-documented, and built on standard React/Vite patterns. Any React developer can maintain and extend it. Questions during the Flippa transfer window? Message through Flippa.

---

*Built by KingdomShift Media Corp*  
*"A righteous man cares for the needs of his animal." — Proverbs 12:10*
