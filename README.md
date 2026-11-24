# ECHOFLIP — Følg Lykken Home-Screen App (PWA)

This is a **playable, installable Progressive Web App** (PWA) edition of ECHOFLIP Zero Margin, with your **Følg Lykken** logo on its startup screen and a branded home-screen icon. It is a standalone recreation of the Floot-hosted game, not an exact source export of the Floot React app.

## What it has

- Flappy-style narrow gates; Flow, Arcade, and Expert difficulties.
- Home button on the pause/results menu, 8-bit music, Prism pickups, score tracking, 4.8-second Overdrive, one-tap gravity flips.
- Simulated (not paid) ad screen after rounds.
- Følg Lykken **launch splash** on every opening, plus compatible iPhone startup art.
- Browser manifest for *Add to Home Screen*; full-screen standalone mode and offline play after first load (service worker).
- No account, analytics, tracking, paid ads, or downloads required beyond visiting the game URL.

## Install on an iPhone

**You first need an HTTPS-hosted website.** Unzipping the package or opening `index.html` as a local file does **not** enable an iPhone installation or offline caching.

1. Upload this whole folder to **GitHub Pages** or another HTTPS static web host.
2. Open the published address in **Safari** on your iPhone.
3. Tap Safari's **Share** icon, choose **Add to Home Screen**, then **Add**. (Depending on iOS version, use the share sheet's More options if needed.)
4. Launch **ECHOFLIP** from its icon. The Følg Lykken startup screen appears and the game opens without the Safari browser bars.
5. The original chiptune begins when the browser allows audio. iOS may require the first tap to enable sound.

On Android/Chrome, open the hosted game and choose **Install app** from the browser menu or the in-game install button if prompted.

## Publish on GitHub Pages

Create a **public** GitHub repository, e.g. `echoflip-app`, and upload the *contents* of this directory to its root. Go to **Settings → Pages** → Deploy from a branch → `main` → `/(root)` → Save. Once GitHub Pages deployment finishes, navigate to `https://USERNAME.github.io/echoflip-app/` and install from Safari.

All file references are relative so GitHub Pages subfolder hosting works. Publish all files including `manifest.webmanifest`, `sw.js`, and `icons/`, `assets/`, and `splash/`.

## App Store / native apps

This is **not** an `.ipa` for Apple's App Store and does not install through the App Store; it is a home-screen web app. Publishing a native app requires native packaging, signing, Apple Developer account and store review.

## Security and offline behavior

Only same-origin resources are cached. The service worker does not intercept third-party requests. Scores are stored locally in this browser profile. The simulated ad is a visual placeholder with no SDK or personal-data collection.

## Source

- `index.html` game UI and startup screen
- `assets/game.js` gameplay and procedural 8-bit soundtrack
- `assets/style.css` responsive layout
- `assets/pwa.js` install instructions and startup transition
- `manifest.webmanifest` app metadata/icons
- `sw.js` offline cache
- `assets/folg-lykken-logo.jpg` your exact logo artwork
- `splash/` iOS portrait launch assets

Built as a separate package because changes to the linked Floot web app were blocked by that service's daily action limit. The original hosted preview remains unchanged.