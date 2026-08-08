# Simple Calendar

A lightweight **Progressive Web App (PWA)** calendar you can install on desktop or mobile. All data stays on your device — no account, no server.

![PWA](https://img.shields.io/badge/PWA-ready-6c5ce7)
![License](https://img.shields.io/badge/license-MIT-green)
![Offline](https://img.shields.io/badge/offline-supported-00cec9)

## Features

### Calendar & events
- Monthly grid with today highlight and day selection
- Notes and timed events (12h / 24h)
- Emojis, text styles (bold / italic / strikethrough)
- Built-in and **custom categories** (with their own colours)
- **Recurring** events: daily, weekly, fortnightly, yearly  
  - Complete **this occurrence only** (does not mark the whole series)
- Mark days with a custom brush colour
- Auto-mark past days (optional)
- Search notes, marks, and recurring items

### Look & feel
- Multiple theme presets + full colour pickers
- Save / load custom themes
- 20+ Google Fonts
- UI scale control
- Month photo: fixed monthly, random, or custom upload
- Languages: **English**, **Tagalog**, **Norwegian**

### Notifications & sound
- In-app toast reminders + built-in alarm sound
- Optional system / lock-screen notifications (where the browser allows)
- Notify days-ahead, toast duration, sound volume / length / repeat
- **Snooze 5 minutes** (works while the app is open)

### Data & PWA
- Everything stored in **localStorage** on your device
- **Backup / restore** as JSON
- Export to **.ics** (iCal) for other calendar apps
- Installable (Add to Home Screen / Install app)
- Service worker caching for offline use of the app shell

> **Note:** Timed alarms and snooze need the app open or in the background. Fully closed-app push would need a server (not included).

## Files

| File | Purpose |
|------|---------|
| `index.html` | App (HTML, CSS, and JavaScript) |
| `manifest.json` | PWA install metadata |
| `sw.js` | Service worker (cache + notification click) |
| `LICENSE-Calendar` | MIT license |

## Quick start

### Use online
Host the three main files on any static host (GitHub Pages, Netlify, etc.) over **HTTPS**, then open the site in a modern browser.

### Test locally

```bash
# Python 3
python -m http.server 8080

# or Node
npx serve .

# or PHP
php -S localhost:8080
```

Open `http://localhost:8080` in your browser.

### Install as an app
1. Open the site in Chrome / Edge (desktop or Android).
2. Use **Install** / **Add to Home Screen**.
3. On iOS Safari: Share → **Add to Home Screen** (system notifications need a recent iOS version and the installed app).

## Backup & restore

1. **Settings → Backup (JSON)** — downloads your marks, notes, recurring events, categories, theme, settings, and photos.
2. **Restore (JSON)** — replaces current data with the file.

Settings such as notify days-ahead, sound, language, scale, and mark brush colour are included in the backup.

## Privacy

- No analytics or third-party tracking in the app logic.
- Data never leaves your browser unless **you** export a backup or `.ics` file.
- Month photos may load from [Picsum](https://picsum.photos) when using monthly/random photo mode (network required for those images).
- Google Fonts are loaded from Google when online.

## Browser support

- Chrome / Edge (desktop & Android) — full PWA + notifications  
- Firefox — works; install support varies  
- Safari / iOS — works as a Home Screen web app; notification support depends on iOS version  

Use **HTTPS** for notifications and a reliable install experience.

## License

MIT © 2025–2026 [0MrCrazy0](https://github.com/0MrCrazy0) — see `LICENSE-Calendar`.

---

**Simple Calendar** — your schedule, on your device.
