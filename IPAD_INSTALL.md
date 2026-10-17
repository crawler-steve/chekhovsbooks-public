# Install Chekhov's Gun on an iPad

## Why the HTML file will not open like an app
Safari on iPad does not treat an arbitrary HTML file in Files as an installable local web app. Progressive Web Apps also require the site to be served from a secure web origin (HTTPS) for the service worker/offline cache to work.

## Easiest workflow
1. Upload this PWA folder to any static HTTPS host (GitHub Pages, Cloudflare Pages, Netlify, or another host you control).
2. Open the HTTPS address in Safari on the iPad.
3. Tap **Share** → **Add to Home Screen**.
4. Launch **Chekhov's Gun** from the Home Screen once while online. The service worker caches the app assets, so the discovery interface can then run offline.

## What is already included
- manifest.webmanifest
- service-worker.js
- iPad/iPhone home-screen icon assets
- offline caching of the prototype, catalog data, logo, and store-image assets

## Truly local native wrapper
A fully local `.ipa` cannot be distributed as a simple unsigned download. iOS requires an app to be signed (normally through Xcode/TestFlight/App Store or managed enterprise distribution). If you later want that route, this same web app can be wrapped in a small WKWebView native shell without changing the recommendation logic.
