# Code Studio Pro

## GitHub Pages installation
1. Extract this ZIP.
2. Upload all files from the ZIP to the same GitHub Pages folder/repository root, replacing the old `index.html` and `sw.js` with these updated versions.
3. Keep `index.html`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, and `icon-512.png` together.
4. Open the published HTTPS site in Chrome while online once. Wait for the page to finish loading and the service worker to install.
5. Use Chrome's Add to Home screen / Install option.

## Importing tools
- Use **Import → Select HTML files** to import one or more `.html` / `.htm` files.
- Use **Import → Select folder** to scan a selected folder and import its HTML files.

## Data compatibility
- The main launcher continues using the existing IndexedDB database name `CodeLauncherDB`, so previously imported launcher tools should remain available in the same browser profile and origin.
- Code Studio projects continue using localStorage and attempt to load earlier v8-v11 project keys.
- Keep the same GitHub Pages origin/repository path to retain browser-stored data.

## Offline limits
The app shell, launcher, saved HTML code, and Code Studio interface are available offline after the first successful online load and service-worker installation. Individual saved tools that themselves depend on remote APIs, remote fonts, CDNs, images, or network data still need those resources bundled locally or an internet connection. A service worker cannot make a remote API work offline automatically.

## Important
Browser storage is local to the browser profile and website origin. Clear site data, switching browsers/devices, or changing the GitHub Pages origin can make locally stored projects/tools inaccessible. Export backups regularly.
