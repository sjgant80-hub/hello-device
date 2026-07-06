# Hello Device

**See what your browser can silently do.**

A single HTML file that runs a first-contact handshake between the page and every capability your browser silently offers. Around forty modern Web APIs are checked live — from Bluetooth and USB to WebGPU, Web Crypto, Speech Recognition and the File System Access API. Each one gets a card that says whether your browser has it, what it does in plain English, and (for many) a **Try it** button that exercises the API right in front of you.

Nothing leaves your device. No trackers, no analytics, no network calls.

## Live

<https://sjgant80-hub.github.io/hello-device/>

## What it does

- Probes around 40 Web APIs grouped into seven ordinary categories: **Sense, Motor, Store, Link, Compute, Express, Dream**
- Shows a summary bar: *X of Y capabilities available*
- Lets you try any supported capability live (camera, microphone, location, Web Audio, vibration, wake lock, clipboard, WebGPU adapter, and more)
- Exports a JSON capability report of your browser you can save or share
- Works offline once loaded (installable as a PWA via `manifest.webmanifest` + `sw.js`)

## Why

Every modern browser is a small operating system. Most people — and most developers — have no idea how much sits behind `window` and `navigator`. This page is a friendly mirror: point it at your browser and it tells you, in ordinary English, what your device can already do without installing anything.

Useful for:

- Deciding whether a browser is capable enough for a project
- Debugging cross-browser gaps (open the same URL in Chrome, Firefox, Safari, and diff the JSON reports)
- Explaining browser capabilities to non-technical stakeholders
- Curiosity

## How it works

- One HTML file, vanilla JavaScript, no build step
- Uses only feature-detection (`'thing' in window`, `typeof x`) — nothing is invoked without your click
- Live tests are opt-in per card and only touch capabilities that don't require sensitive permissions unless you explicitly ask
- The exported report is built in memory and downloaded via a `Blob` URL

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole tool. Open it and go. |
| `manifest.webmanifest` | PWA manifest for install-to-home-screen |
| `sw.js` | Service worker for offline caching |
| `LICENSE` | MIT |
| `.nojekyll` | Tells GitHub Pages not to Jekyll-process the site |

## Licence

MIT. Do what you like with it. Attribution appreciated but not required.

## Publisher

Built by **AI-Native Solutions** — <https://ai-nativesolutions.com>
