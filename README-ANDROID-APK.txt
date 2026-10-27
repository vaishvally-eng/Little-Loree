# Little Lore — Android APK preparation (free)

This package updates the existing static website with the files PWABuilder needs to recognize it as a Progressive Web App.

## Files included
- `index.html` — your existing Little Lore page with PWA manifest and service-worker registration added.
- `manifest.webmanifest` — app name, colors, launch URL, and icon metadata.
- `icons/icon-192.png` and `icons/icon-512.png` — app icons.
- `service-worker.js` — caches the app shell and provides a cached page fallback when offline. External fonts may still require an internet connection.

## Put these files into your existing GitHub repository
1. Download and extract this ZIP on your computer.
2. Open the GitHub repository that Vercel deploys.
3. Upload/replace `index.html` at the repository root; also upload `manifest.webmanifest` and `service-worker.js` at the root.
4. Upload the `icons` folder with both PNG files, preserving the folder name and paths.
5. Commit the changes. Vercel should redeploy automatically.
6. Once deployment is complete, open `https://little-lore-sigma.vercel.app/manifest.webmanifest` in a browser. You should see the manifest JSON rather than a 404.
7. Go to https://www.pwabuilder.com/ and re-enter `https://little-lore-sigma.vercel.app/`. Confirm the manifest is detected, then choose the Android packaging option and follow its signing/package steps.

## Important notes
- This ZIP prepares the website; it is **not itself an APK**. The APK is generated after the changes are deployed and PWABuilder can read the live manifest.
- Keep the signing key and password private and backed up. An APK update generally needs the same signing key.
- This app's existing diary content appears to be stored in browser local storage. It may remain on each device separately; this package does not add cloud sync, encryption, or cross-device backup.
- The service worker caches the app shell, not every external resource. Test the application online and offline after deployment.
