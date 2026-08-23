# Love Utah

**Utah real estate market intelligence for the Wasatch Front**

Live site: [loveutah.pages.dev](https://loveutah.pages.dev)

## Overview

Wasatch provides comprehensive market analysis, neighborhood insights, and buyer intelligence for Utah real estate. Updated monthly with data from:

- Utah Association of REALTORS
- Salt Lake Board of REALTORS (via KSL)
- Freddie Mac PMMS
- Best Utah / UtahRealEstate.com
- Gardner Policy Institute

## Features

- **Live Market Data** — Statewide, county-level, and city-specific medians with YoY trends
- **City Profiles** — Eagle Mountain, Lehi, Saratoga Springs, South Jordan, Draper, St. George, and more
- **School District Rankings** — Alpine, Canyons, Jordan, and Washington County districts
- **Livability Scores** — Walk/bike/transit scores plus outdoor access (editorial)
- **2034 Olympics Impact** — Venue-proximity appreciation estimates
- **Buyer Programs** — Utah Housing Corporation loans, grants, and first-time buyer assistance
- **Mortgage Rate Tracker** — Weekly Freddie Mac PMMS updates

## Tech Stack

- **Static HTML/CSS** — No framework overhead, instant load times
- **Modern CSS** — CSS Grid, custom properties, mobile-first responsive design
- **Zero dependencies** — Pure HTML/CSS, no build complexity
- **$0 hosting** — Cloudflare Pages free tier

## Local Development

```bash
# Serve locally on port 8000
npm run dev
```

Then open [http://localhost:8000](http://localhost:8000)

## Build

```bash
# Build for production
npm run build
```

Output: `dist/` directory with all static assets

## Cloudflare Pages Deployment

### Project Settings

- **Project name**: `loveutah`
- **Production branch**: `main`
- **Build command**: `npm run build`
- **Build output directory**: `dist`
- **Root directory**: `/` (default)

### Deploy via Cloudflare Dashboard

1. Connect GitHub repository: `biosync-tech/loveutah`
2. Set build command: `npm run build`
3. Set build output directory: `dist`
4. Deploy

Production URL: `https://loveutah.pages.dev`

### Deploy via Wrangler CLI

```bash
# Install wrangler globally
npm install -g wrangler

# Login to Cloudflare
wrangler login

# Build and deploy
npm run build
wrangler pages deploy dist --project-name=loveutah
```

## Data Updates

Market data is updated monthly. To update:

1. Pull latest data from UAR, Salt Lake Board, Freddie Mac
2. Update figures in `index.html`
3. Update "Last updated" date in footer and JSON-LD
4. Commit and push to trigger automatic deployment

## SEO & AI Crawlers

- `robots.txt` — Allows helpful AI search crawlers (OAI-SearchBot, Claude-SearchBot, PerplexityBot); blocks training scrapers (GPTBot, ClaudeBot, Google-Extended)
- `llms.txt` — Provides structured briefing for LLM-based search systems
- JSON-LD structured data — RealEstateAgent, WebSite, NewsArticle schemas

## Agent

**Sruthi** — Licensed Utah Real Estate Agent

Contact: [hello@loveutah.pages.dev](mailto:hello@loveutah.pages.dev)

## Data Sources

All data is cited from public sources:

- **Utah Association of REALTORS** — Statewide and county-level data (July 2026)
- **Salt Lake Board of REALTORS / KSL** — Single-family Q2 2026 by ZIP
- **Freddie Mac PMMS** — Weekly mortgage rates (Aug 20, 2026)
- **Best Utah / UtahRealEstate.com** — City-level all-types medians (July 2026)
- **Gardner Policy Institute** — Economic forecasts and data center reports
- **KUER** — Gardner/Wood housing forecast (Jan 2026)
- **Realtor.com** — Utah County rental market trends

## Last Updated

August 22, 2026

---

Built by Biosync for Utah homebuyers.
