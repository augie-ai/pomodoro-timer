# 🍅 Free Pomodoro Timer Online

A fully-featured, SEO-optimized, monetization-ready Pomodoro Timer web app.

**Live at:** [https://pomodoro-timer.example.com](https://pomodoro-timer.example.com) *(update with your Vercel URL)*

---

## Features

- ⏱ **Circular countdown timer** — Pomodoro (25 min), Short Break (5 min), Long Break (15 min)
- 🔄 **Auto-switch** between Pomodoro and breaks with session counter (1/4 → 2/4 → long break)
- ⌨️ **Keyboard shortcuts** — `Space` start/pause, `R` reset, `S` skip
- 🔔 **Sound alerts** via Web Audio API — no external files needed
- 📋 **Task list** — add, complete, delete, set active task; saved to `localStorage`
- ⚙️ **Settings panel** — customize all durations, auto-start, sound; saved to `localStorage`
- 📊 **Daily stats** — pomodoros completed + focus time today; saved to `localStorage`
- 📱 **PWA-ready** — Add to Home Screen on mobile
- 🌑 **Dark mode** — dark purple/blue gradient, beautiful circular timer ring

---

## Tech Stack

- **Pure HTML/CSS/JS** — zero dependencies, zero build step
- Single `index.html` file
- Web Audio API for sounds
- `localStorage` for persistence
- SVG for the timer ring animation

---

## Deploy on Vercel

```bash
# Install Vercel CLI (if not already)
npm i -g vercel

# Deploy from project directory
cd pomodoro-timer
vercel --prod
```

That's it. Vercel detects it as a static site automatically. `vercel.json` handles headers and rewrites.

---

## Monetization

### Google AdSense
Two ad slots are ready (currently hidden). To enable:

1. Replace `ca-pub-XXXXXXXXXXXXXXXX` with your Publisher ID
2. Uncomment the AdSense `<script>` tag in `<head>`
3. Uncomment the two `<ins class="adsbygoogle">` blocks (above timer + below task list)

### Affiliate Links
Bottom section has 4 affiliate card placeholders:
- Notion, Todoist, Forest App, RescueTime
- Replace `href="#"` with your affiliate links

---

## SEO

- **Title:** "Free Pomodoro Timer Online — Focus & Productivity Tool"
- **Meta description** targeting: `pomodoro timer online free`, `focus timer`, `study timer`
- **Open Graph** + **Twitter Card** tags
- **Structured data** — `WebApplication` schema
- **robots.txt** + **sitemap.xml** included
- **Canonical URL** — update `https://pomodoro-timer.example.com/` to your domain

---

## Customization

### Update domain everywhere:
Search and replace `pomodoro-timer.example.com` with your actual domain in:
- `index.html` (canonical, OG tags, structured data)
- `sitemap.xml`
- `robots.txt`

### Change default durations:
Edit the `settings` object in the `<script>` section of `index.html`:
```js
let settings = {
  pomo: 25,   // Pomodoro minutes
  short: 5,   // Short break minutes
  long: 15,   // Long break minutes
  ...
};
```

---

## File Structure

```
pomodoro-timer/
├── index.html      # Main app (all-in-one)
├── manifest.json   # PWA manifest
├── robots.txt      # SEO robots
├── sitemap.xml     # SEO sitemap
├── vercel.json     # Vercel deployment config
└── README.md       # This file
```

---

## License

MIT — free to use, modify, and deploy.

---

*Built with ❤️ | © 2026*
