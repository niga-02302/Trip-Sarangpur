# TripSplit – Mobile Header and Closed Menu Fix

## Fixes in this package
- Rebuilt the header with a dedicated single-row flex container. The TripSplit icon/name and hamburger button cannot wrap onto separate rows on mobile.
- Changed the navigation to use the native HTML `hidden` attribute. It is explicitly hidden in the HTML, on page initialization, after login/session restoration, after changing screens, and when tapping outside the header or pressing Escape.
- The hamburger button is the only control that opens the menu. Tapping it again closes the menu.
- Kept Sign out inside the hamburger menu.
- Added a network-first service-worker strategy for HTML so installed home-screen apps are less likely to keep showing an old cached layout.
- No Supabase schema or data changes.

## Important: upload the files to the repository root
Extract the ZIP and upload the files **inside it** directly into the root of the GitHub repository (the same folder where the existing `index.html` is located). Do not upload the enclosing ZIP folder as a nested folder.

Replace these files:
- `index.html`
- `sw.js`
- `manifest.webmanifest`
- `icon-192.png`
- `icon-512.png`
- `apple-touch-icon.png`
- `favicon-16.png`
- `favicon-32.png`

Then commit the changes and wait for GitHub Pages deployment.

## Refresh on Android
1. Close the TripSplit installed app completely.
2. Open the website in Chrome and reload it once.
3. Reopen the installed app. If it still shows the old version, remove the old home-screen shortcut and add the website to Home Screen again after the site has loaded the new version.

No SQL changes are required.
