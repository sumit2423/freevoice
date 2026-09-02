# FreeVoice

A free, open-source AAC (Augmentative and Alternative Communication) app — a tap-to-speak talk board for non-verbal children and adults, built as an installable, offline-first web app.

<!-- screenshot placeholder: add a screenshot of Talker Mode here, e.g. docs/screenshot.png -->

**Live app:** https://sumit2423.github.io/freevoice/

## Why

Commercial AAC tools are expensive and often clinically rigid. FreeVoice started as a communication tool for a non-verbal 4-year-old, built by his father, and grew into a small open-source project for other families in the same situation. It's free and will stay that way — no monetization, ever.

Every design choice follows from one constraint: this is used by a child, so the app has to get out of the way. It launches straight into the talk board with zero setup screens, and every feature — fixed tile positions for muscle memory, offline caching, a fatigue-aware tap filter — exists to keep that path as short and reliable as possible.

## Features

- **Talker Mode** — tap a tile to hear it spoken and add it to a sentence strip; tap Speak to read the full sentence aloud
- **Fixed motor-planning grid** — tiles keep their position permanently (the core clinical premise behind LAMP-style AAC), so tapping becomes muscle memory over time
- **Parts-of-speech color coding** — the standard Fitzgerald key (nouns yellow, verbs green, etc.) used across clinical AAC boards
- **Clinical symbol library** — live search against [ARASAAC](https://arasaac.org)'s ~20,000 pictograms for vocabulary that can't easily be photographed, cached locally after selection for offline use
- **Custom photo & voice tiles** — camera capture for personalized tiles, plus recorded custom voice per tile as an alternative to text-to-speech
- **Open Board Format (.obf) import/export** — boards are portable to and from other AAC tools (Cboard, CoughDrop, TouchChat)
- **Usage reports** — local tap logging with a weekly summary and CSV export, useful for sharing with a speech therapist
- **Installable PWA** — offline-capable via service worker, with an in-app update banner so a kiosk-locked device can still pick up new releases
- **Admin/Parent Mode** — PIN-gated tile and category management, manual tile rearranging, full JSON backup/restore, and a print stylesheet as an offline fallback

## How it's built

Single-file HTML/CSS/JS, no framework, no build step, no backend — a deliberate choice given the actual constraint (a tablet in a child's hands, sometimes offline). Data lives in `localStorage` on-device by default; nothing leaves the device unless a future sync feature is explicitly opted into.

See [`GUIDE.md`](GUIDE.md) for day-to-day setup and troubleshooting.

## Status

Actively used and actively developed. Symbol library search, the fixed motor-planning grid, color coding, usage logging, and offline/PWA support are all shipped. A public roadmap is coming soon.

## License & credits

App code is free and open source. Pictogram symbols are provided by [ARASAAC](https://arasaac.org) — property of the Government of Aragón, created by Sergio Palao, distributed under a Creative Commons BY-NC-SA license. Full attribution and license terms are available in-app (Help → Credits & Licensing) and at [arasaac.org/terms-of-use](https://arasaac.org/terms-of-use).

## Author

Built and maintained by [Sumit Deshmukh](https://github.com/sumit2423).
