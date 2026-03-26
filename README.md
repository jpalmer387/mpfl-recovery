# MPFL Recovery Tracker

A progressive web app for tracking a 16-week MPFL (medial patellofemoral ligament) recovery training program, built to get a 15-year-old soccer player back to game-ready.

## What it does

- **4-phase training plan** with daily exercise checklists (foundation → progressive loading → power/agility → return to sport)
- **XP and streak system** to keep motivation up through a long rehab
- **Boss battles** at each phase gate — advancement criteria framed as a challenge to beat, with PT confirmation required
- **Weekly benchmarks** with D3.js trend charts (wall sit hold, single-leg balance, squat depth, hop distance)
- **Training log** showing session history and XP earned
- **Offline-capable** — works without internet after first load
- **Installable** — add to home screen on iOS/Android, runs like a native app

## Tech

Single HTML file + service worker + manifest. No build step, no framework, no backend.

- Vanilla JS with D3.js (CDN) for benchmark charts
- localStorage for all data (stays on device)
- Service worker for offline support

## Deploy to GitHub Pages

```bash
git init
git add .
git commit -m "initial commit"
git remote add origin git@github.com:YOURUSERNAME/mpfl-tracker.git
git branch -M main
git push -u origin main
```

Then in the GitHub repo: **Settings → Pages → Source: Deploy from a branch → Branch: main, / (root) → Save**

The app will be live at `https://YOURUSERNAME.github.io/mpfl-tracker/` within a few minutes.

## Install on phone

1. Open the GitHub Pages URL in Safari (iOS) or Chrome (Android)
2. **iOS:** Tap Share → "Add to Home Screen"
3. **Android:** Tap the browser menu → "Add to Home Screen" or "Install app"

## Data

All training data is stored in the browser's localStorage on the device. Nothing is sent to any server. Use Settings → Export to back up data as JSON.

## Important

This is a training framework, not medical advice. All phase advancement should be coordinated with and approved by a physical therapist. Any swelling or pain = back off.
