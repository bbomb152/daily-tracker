# Habits

A zero-dependency, mobile-first habit tracker PWA. Tracks four daily habits:

- 🎸 Practice guitar (with minutes)
- 🏋️ Go to the gym
- 🥤 Protein shake
- ✅ Did something productive

Features: streaks (current + best), a 16-week heatmap, weekly guitar-minutes
chart, 30-day completion rates, demo mode with 90 days of generated data,
and JSON export/import.

## Run it

Any static file server works. For example:

```
npx serve . -l 8642
```

Then open http://localhost:8642.

## Use it on your phone

**Same Wi-Fi (quick):** start the server as above, then on your phone open
`http://<your-pc-ip>:8642` (find the IP with `ipconfig`). Windows Firewall
must allow Node.js on private networks the first time.

**Anywhere (recommended):** push this folder to a GitHub repo and enable
GitHub Pages — it's a static site, no build step. Then on your phone, open
the page in the browser and "Add to Home Screen" to install it as an app
(the manifest + service worker make it installable and offline-capable).

## Data

Data is stored in the browser's `localStorage` (key `habitlog.v1`), so each
device keeps its own log. Use **Data → Export/Import** to move history
between devices. Demo mode uses a separate key and never touches real data.
