QUESTBOARD — DARK DEVELOPER EDITION

FILES
- index.html: complete app (HTML, CSS, JavaScript in one file)
- manifest.webmanifest: installable-app metadata
- sw.js: offline cache, enabled after first load over HTTPS
- icon-192.png / icon-512.png: app icons

OPTION A — USE ON A MAC RIGHT AWAY
1. Download Questboard-Offline.html (the standalone file outside this ZIP).
2. Move it to Documents/Questboard and double-click it.
3. Data is stored in that browser on that Mac. Use Export backup regularly.

OPTION B — INSTALL ON MAC + PHONE AS A WEB APP
The PWA must be hosted from HTTPS for service-worker offline caching. A free static host such as GitHub Pages can be used.
1. Create a GitHub repository for this app.
2. Upload the CONTENTS of this folder (index.html, manifest.webmanifest, sw.js, and both PNG icons) to the repository root.
3. In repository Settings, open Pages and publish from the main branch and /(root). Use the HTTPS URL GitHub Pages provides.
4. Open the URL on your Mac. In Chrome, choose the install icon in the address bar if offered, or use the browser's install option.
5. On iPhone, open the HTTPS URL in Safari, tap Share, then Add to Home Screen. On Android, open in Chrome and use the menu's Install app or Add to Home Screen option.
6. Launch it once while online, then open it again to verify offline behaviour. The service worker caches the app shell after the initial successful load.

NOTES
- This app is self-contained and does not use a remote API.
- Progress is saved separately in each browser/device. It does not automatically sync across devices.
- Export backup downloads a JSON file. Import restores that backup and replaces the currently saved data in that browser.
- Browser data can be erased by browser cleanup/reset. Keep a backup if the progress matters to you.
