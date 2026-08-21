# Budget App (PWA)

A personal expense tracker as a Progressive Web App. Works on iPhone Safari and can be added to the home screen like a native app, including offline use.

## Files

- `index.html` — the entire app (UI + logic)
- `manifest.json` — PWA config (name, icon, colors)
- `service-worker.js` — offline caching
- `icon-192.png`, `icon-512.png` — app icons

No build step needed. It's plain HTML/CSS/JS.

## Deploy (pick one, both are free)

### Option A: Netlify Drop (fastest, no account needed to try)
1. Go to https://app.netlify.com/drop
2. Drag the whole `webapp` folder onto the page
3. You get a live URL instantly (e.g. `https://random-name.netlify.app`)

### Option B: Vercel (good if you want a GitHub-connected setup)
1. Push this folder to a GitHub repo
2. Go to https://vercel.com, import the repo
3. Deploy (no build settings needed — it's static)

## Add to iPhone home screen

1. Open the deployed URL in Safari on your iPhone
2. Tap the Share icon → "Add to Home Screen"
3. It now opens full-screen like a native app, and works offline

## Data storage

Expenses are stored in the browser's `localStorage`, on-device. Note: if you clear Safari's website data/cache, the data will be lost. This is fine for casual personal use, but isn't a backup — keep that in mind.

## Notes

- Weekly budget is hardcoded to £70 in `index.html` (search for `WEEKLY_BUDGET`)
- Week starts on Monday
