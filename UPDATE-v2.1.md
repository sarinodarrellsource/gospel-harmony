# Gospel Harmony v2.1 — Install and remember device
Export study backup before updating. Upload app.js, index.html and service-worker.js to the same repository root (replace existing files). Keep manifest.json, icons, style.css and data/harmony.json. No Cloudflare changes required.

Open the deployed website, refresh; if old content persists, close all app/browser tabs for this site and reopen. Install using Chrome on Android or Safari Share > Add to Home Screen on iOS/iPadOS. On each device open the installed app, unlock using APP_ACCESS_TOKEN, and opt in to Remember on this device. Close and reopen to test. Lock licensed Bibles removes saved login in that browser. Clear site data also removes it (and local notes, so back up first).

The bearer token is saved unencrypted in browser localStorage only on opt-in. Scripts running on the origin (including third-party scripts), browser extensions with access, or someone with access to the browser may obtain it. Use only on trusted devices. Do not reuse passwords. Rotate APP_ACCESS_TOKEN in Cloudflare if compromised; unlock again on every device. Never enter API_BIBLE_KEY in the app. No credentials in source or study backup. Notes do not sync across devices. Internet and provider access required for licensed passages. Existing rate limiting and FUMS verification limitations remain.

Checks: JavaScript syntax and ZIP integrity. Live installation, authentication and persistence require device testing.
