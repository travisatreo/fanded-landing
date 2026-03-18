# Fanded Landing Page — Session Handoff

**Last updated:** 2026-03-18
**Branch:** main (pushed to GitHub)
**Repo:** https://github.com/travisatreo/fanded-landing
**NOT yet deployed** — needs Vercel project setup + domain pointing
**Design system:** DESIGN.md lives in the fanded-app repo (/Users/travis/Documents/Fanded M1/fanded-app/DESIGN.md)

## What We Built

Standalone landing page for fanded.com — the marketing site for Fanded's fan club platform. Built in the same single-file approach as MAWD demo. Three audience sections (creators, fans, investors) plus MAWD integration.

### Design System
- **Aesthetic:** Luxury/Editorial — premium positioning to differentiate from Patreon/Circle
- **Display font:** Instrument Serif (Google Fonts) — no competitor uses a serif
- **Body font:** Onest (matches existing Fanded app)
- **Primary:** #4A4AE6 (brand purple, shared with MAWD)
- **Accent:** #E8C547 (warm gold — VIP/premium signal)
- **Background:** Dark (#0A0A1A) with warm ambient gradient orbs
- **Ambient glow:** 6 parallax orbs (purple + sunset orange/amber/gold) that drift on scroll

### Page Sections
1. **Nav** — fixed, dark frosted glass, logo + For Creators / For Fans / For Investors + Sign In
2. **Hero** — "Where fans become *family*" (Instrument Serif), two CTAs
3. **Stats** — real numbers: 5,000+ members, 100+ clubs, $15K+ paid, $100+ avg/club
4. **For Creators** — "Your art deserves a *real* business" + 3 feature cards
5. **For Fans** — "Get closer than *ever*" + 3 fan club cards (Travis, Athlete, Pizza Co.)
6. **MAWD section** — dark card with agent roster, links to mawd.fanded.com
7. **For Investors** — "$905B market" + CAC + LTV metrics
8. **Final CTA** — "Ready to build your *inner circle*?"
9. **Footer** — links to app, MAWD demo, contact, terms, privacy

### Key Files
```
public/
  index.html    # The entire landing page (~400 lines)
vercel.json     # Vercel config
package.json    # Minimal
CONTEXT.md      # This file
```

## Current State

### What's Working
- Full landing page with all 9 sections
- Dark mode with warm ambient gradient glow (6 orbs, parallax on scroll)
- Scroll reveal animations (IntersectionObserver)
- Responsive layout
- Real traction numbers (not inflated)
- Instrument Serif + Onest + Gold design system
- Pushed to GitHub at travisatreo/fanded-landing

### NOT Yet Done
- **Not deployed to Vercel** — needs new project in Vercel dashboard, import the repo, then point fanded.com domain
- **No mobile hamburger menu** — nav links are hidden on mobile, only logo + Sign In show
- **No favicon** — needs the Fanded "F" icon
- **No OG image** — og:image meta tag is empty (needs a social preview card)
- **Stats are not animated** — they're static numbers, could count up on scroll like MAWD dashboard
- **Fan club cards use placeholder images** — gradient backgrounds with emojis, not real photos

## Related Projects

| Project | Repo | URL | Purpose |
|---------|------|-----|---------|
| MAWD Demo | travisatreo/Mawd-demo | mawd.fanded.com | AI management demo (live, working) |
| Fanded App | devfanded/fanded | app.fanded.com | The actual product (Next.js, Supabase) |
| Fanded Landing | travisatreo/fanded-landing | fanded.com (pending) | Marketing landing page (this repo) |

## Design System Location
Full DESIGN.md is at: `/Users/travis/Documents/Fanded M1/fanded-app/DESIGN.md`
Covers: typography, colors, spacing, layout, motion, brand relationship between Fanded and MAWD.

## Next Steps

### Deploy (do first)
1. Go to vercel.com/fanded → Add New Project → import travisatreo/fanded-landing
2. Deploy (no build command needed, serves public/)
3. Add fanded.com as custom domain (may need to remove from current Vercel project first)

### Polish
4. Add mobile hamburger menu
5. Add favicon (Fanded "F" gradient icon)
6. Create OG social preview image
7. Animate stat numbers on scroll (count up like MAWD)
8. Replace emoji club card images with real photos or better illustrations

### Fundraising Leverage
- The MAWD demo (mawd.fanded.com) is the "holy shit" moment — let investors type questions
- Travis as proof point — 420M streams, real data, real deal
- Template system — can spin up demos for other artists in 10 minutes
- The pitch: "Not building a better Patreon. Building the OS for talent."

## How to Resume

```bash
cd "/Users/travis/Documents/Fanded M1/fanded-landing"
# All on main, all pushed. Edit and push to deploy.

# To deploy to Vercel:
# 1. Import repo at vercel.com/fanded
# 2. Point fanded.com domain

# To edit locally: open public/index.html in browser
# Cmd+Shift+R to hard refresh after changes

# The fanded-app repo (production app) is at:
cd "/Users/travis/Documents/Fanded M1/fanded-app"
# Branch: staging. DESIGN.md is there.
```
