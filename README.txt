ELEMENTAL DUEL — ANDROID PWA PACKAGE

Contents
- index.html: the existing standalone game, with PWA metadata and service-worker registration added.
- manifest.webmanifest: app name, icon, standalone display and portrait preference.
- service-worker.js: caches the app shell for offline use after the first successful online visit.
- icons/: Android/PWA launcher icons.

IMPORTANT
A PWA must be hosted on an HTTPS website (or localhost) to install and use its service worker. Opening index.html directly from Downloads is not enough to install it as a PWA.

PHONE-ONLY DEPLOYMENT (GitHub Pages)
1. Create/sign in to a GitHub account in Chrome.
2. Create a new public repository, for example: elemental-duel.
3. Upload the CONTENTS of this folder to the repository root (index.html, manifest.webmanifest, service-worker.js, icons folder). Do not upload only the ZIP.
4. In the repository, open Settings → Pages.
5. Under Build and deployment, choose Deploy from a branch; select main and /(root), then Save.
6. Wait for GitHub Pages to publish. Open the HTTPS address it provides.
7. In Chrome on Android, open the game URL, wait for it to finish loading, then use the browser menu → Install app or Add to Home screen (wording varies).
8. Open the installed app once while online. Then enable Airplane mode and relaunch to test offline caching.

UPDATES
When replacing the game later, upload the new index.html. If you change the service worker's cached file list or want to force a fresh cache, change CACHE_NAME in service-worker.js (for example v2).

NOTES
- The game logic and monster images are embedded in index.html.
- This package does not add online multiplayer, accounts, cloud saves, payments or analytics.
- Offline availability begins only after a successful first load while online.
- Keep the original Elemental-Duel.html and Claude artifact as separate backups.
