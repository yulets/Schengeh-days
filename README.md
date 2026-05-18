# Schengen Days

A quiet, offline-first tracker for the Schengen 90/180 rule. Tracks past trips, plans future ones, validates them against the rolling 180-day window. Data lives in your browser's local storage — nothing is sent anywhere.

## Deploy to GitHub Pages

### 1. Create the repo

1. Sign in to GitHub.
2. Click **New repository**.
3. Name it something like `schengen-days` (the name will appear in your URL).
4. Make it **Public** (required for free GitHub Pages).
5. Don't initialize with a README — you'll upload these files directly.
6. Click **Create repository**.

### 2. Upload the files

On the empty repo page, click **uploading an existing file** (or drag and drop). Upload **all** files in this folder:

- `index.html`
- `manifest.json`
- `sw.js`
- `icon-192.png`
- `icon-512.png`
- `icon-maskable.png`
- `apple-touch-icon.png`

Scroll down and click **Commit changes**.

### 3. Enable Pages

1. In the repo, go to **Settings** (top tab).
2. In the left sidebar, click **Pages**.
3. Under **Source**, select **Deploy from a branch**.
4. Branch: **main**, folder: **/ (root)**. Click **Save**.
5. Wait ~1 minute. The page will refresh and show your live URL — something like:

   `https://YOUR-USERNAME.github.io/schengen-days/`

That's your app.

## Install on iPhone

1. Open the URL above in **Safari** (must be Safari, not Chrome — only Safari can install PWAs on iOS).
2. Tap the **Share** button (square with arrow up at the bottom).
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add** in the top right.

The icon appears on your home screen. Tap it — it opens fullscreen, no Safari chrome, works offline. Your data persists between sessions.

## How the 90/180 rule works (quick refresher)

You may stay up to **90 days** in any rolling **180-day window** in the Schengen Area. Both your entry day and exit day count as full days inside the zone. The app shows:

- How many days you've used in the last 180 (as of today)
- How many you have left
- When the next day "rolls off" (you'll have +1 day available)
- When you'll have all 90 days available again

For future trips, it simulates the full window day-by-day and flags any date where you'd exceed 90.

## Updating the app later

If you want to make changes, just edit the file on GitHub (click the file → pencil icon → commit). The site rebuilds in about a minute. To get the new version on your phone, close the app fully and reopen it (the service worker pulls fresh HTML).

## Notes

- Bulgaria and Romania are included — they joined Schengen on 31 March 2024 (air/sea) and 1 January 2025 (land borders).
- This tool is not legal advice. For any border-crossing decision you're unsure about, check the official EU calculator: https://ec.europa.eu/assets/home/visa-calculator/calculator.htm
