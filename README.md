# Little Lore

A minimal, pastel-themed digital diary and journal PWA.

## Included
- `index.html` — application
- `manifest.webmanifest` — PWA metadata and icon paths
- `service-worker.js` — app-shell caching and offline navigation fallback
- `icons/` — 192px and 512px standard and maskable app icons

## Deploy to GitHub / Vercel
1. Upload the contents of this folder to the root of the GitHub repository used by your Vercel project.
2. Keep the `icons/` folder and filenames unchanged.
3. Commit and push. Vercel should redeploy automatically.
4. Open the deployed site and test the diary, wish jar, and offline launch.

## Clean starting state
The built-in sample diary entry, planner tasks, scrapbook items, wish examples, affirmation suggestions, and sample mood history have been removed from the app's default state. New entries are created by the user.

**Existing browser data:** The app stores user-created content in browser local storage. If the same browser already has old sample content saved from an earlier version, that saved data can remain. Back up anything you want to keep before clearing the app's site data in browser settings.

## Icons
The provided 192px icon artwork was resized to create the 512px variants. Replace the generated variants if you have separate final 512px artwork.
