# Istiyak Services - Website Package

This package contains a mobile-friendly HTML website with Google Analytics (GA4) integration, PWA manifest, service worker, Privacy/About/Contact pages, and instructions to publish to GitHub Pages and convert to Android app (TWA).

## Files
- index.html (main site) — edit GA4 measurement ID (G-XXXXXXXX)
- manifest.json (PWA manifest)
- service-worker.js (basic offline cache)
- privacy.html, about.html, contact.html
- icons/ (placeholder icon files)
- README.md (this file)

## Quick steps to enable Analytics
1. Create a Google Analytics GA4 property and copy the Measurement ID (G-XXXXXXXX).
2. Replace G-XXXXXXXX in index.html script block with your ID.
3. Publish site to GitHub Pages.

## Convert to Android App (Play Store) using TWA (short)
1. Make sure your site is HTTPS (GitHub Pages gives HTTPS).
2. Create a PWA: manifest.json and service worker are included.
3. Install Bubblewrap (Node.js): `npm install -g @bubblewrap/cli`.
4. Run: `bubblewrap init --manifest=https://<your-site>/manifest.json` and follow prompts.
5. Build: `bubblewrap build` -> produces an Android project; generate an AAB.
6. Register Google Play Developer account ($25) and publish the AAB.

## Notes
- Add a real Privacy Policy and contact email before publishing to Play Store.
- For assetlinks (Digital Asset Links) see Bubblewrap docs — required for TWA verification.
