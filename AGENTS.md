# AGENTS.md

Static GitHub Pages site, no build step. Pushes to `main` deploy immediately to `mladenstojanovic.art` / `tntstupido.github.io`.

## File Naming
App pages: `[app-name]-[type].html` (types: `landing`, `privacy-policy`, `account-deletion`, `age-suitability`).

## New Page Checklist
- Add to `sitemap.xml` with `lastmod` (YYYY-MM-DD) and priority: 1.0 (index), 0.9 (landing), 0.5 (privacy), 0.4 (other)
- Update footer policy links in `index.html`

## Key Paths
- `assets/`: Static assets (images, videos, screenshots)
- `CNAME`: Points to `mladenstojanovic.art`
- `sitemap.xml`, `robots.txt`, `manifest.json`: SEO files

## Die Laughing landing — known follow-ups
Captured 2026-06-09 after the production-launch + mobile-polish pass. Not urgent, but worth doing when there's bandwidth.

- **Re-export the hero video tighter.** `assets/gameplay_video/web_video_square.mp4` is ~16 MB. Target 2-3 MB at 720p square, H.264, ~8-12s gameplay loop. Big win for mobile data and time-to-first-frame.
- **Add a small screenshots strip to the desktop hero.** Right now the autoplaying video is the only above-the-fold visual on desktop. A row of 3-4 thumbnail screenshots next to or below the video gives desktop users a static preview option.
- **Wire info-card copy to real visuals.** "How to Install" and "It's Live, Not Perfect" cards are text-only. A small in-card screenshot or icon would break up the text wall and make scanning easier.
- **Consider a 9:16 portrait cut of the video.** Square works in the hero, but a portrait version would fit the existing 9:16 framing used in the screenshots section, making the visual language more consistent.
- **Optimize the screenshot PNGs for web.** The 6 mockups at 1080x1920 are ~9.7 MB total. They're displayed at 160-240px wide. Re-exporting at 480x854 (or converting to WebP) would cut that by ~70% with no visible quality loss.
- **Move to Cloudflare Pages + Cloudflare Web Analytics for ad-blocker-proof tracking.** Captured 2026-06-12. Current setup uses `cloud.umami.is` (cloud-hosted Umami, cookieless, free tier). `cloud.umami.is` is on the EasyPrivacy list — desktop ad-blocker users are invisible to it. Mobile browser ad-blockers are less common (1Blocker, AdGuard for iOS exist but penetration is low — most mobile users see the script), so the data loss is mostly desktop. The signal we care about (mobile landing → app store click → install) is probably ~80-90% intact. Watching the numbers for a few weeks before deciding to migrate. If migration happens: switch `tntstupido.github.io` CNAME to Cloudflare Pages, enable Cloudflare Web Analytics (free, same-origin beacon so not blocked by host-based filters, no cookie consent needed). Also covers portfolio pages (`index.html`, `yurui-landing.html`, `roomli.html`, `rule-rings-landing.html`) for free.
