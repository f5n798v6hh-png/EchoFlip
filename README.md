# ECHOFLIP — Følg Lykken Edition

ECHOFLIP is a one-touch arcade game (PWA) with the branded Følg Lykken launch screen, original 8-bit music, narrow gates, difficulty selection, mock ads and offline support.

## Play on iPhone

When published with GitHub Pages, open `https://f5n798v6hh-png.github.io/EchoFlip/` in Safari, tap Share, then Add to Home Screen.

## Configure GitHub Pages

This repo was initially private. Public GitHub Pages on GitHub Free requires a public repository. To intentionally change visibility: Settings → General → Danger Zone → Change repository visibility → Public. This makes the code publicly visible. Then Settings → Pages → Source: GitHub Actions. The included workflow builds and publishes the app when changes land on main.

The compressed source bundle in this repository is decoded by the deployment workflow. This is an implementation workaround, not an encryption measure. The app works offline after first visit, once its assets are cached. No real advertisement network is connected.