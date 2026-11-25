# Gospel Harmony — Parallel Bible Study

Version 1.0 starter release. A static, no-build web application.

## Deploy on GitHub Pages
1. Extract the ZIP. Create a public GitHub repository named `gospel-harmony`.
2. On the repository page, choose Add file > Upload files. Upload the contents of the extracted folder, including the `data` folder. `index.html` must be at the repository root, not inside another folder. Commit to `main`.
3. Open Settings > Pages. Under Build and deployment choose Deploy from a branch, main, /(root), then Save.
4. Open the URL displayed by GitHub Pages, typically `https://YOUR-USERNAME.github.io/gospel-harmony/`.
5. On Android Chrome, open the deployed site and use the browser menu > Install app or Add to Home screen (if available).

For local testing with Python installed, run `python -m http.server 8000` in this directory and visit `http://localhost:8000`. Double-clicking index.html is not supported because the JSON database is fetched over HTTP.

## Features
- 209 manually transcribed event rows, 16 categories, all six source pages.
- Four horizontal Gospel columns, show/hide, per-column translations, resizing, approximate synchronized scroll, full screen and three reading themes.
- Translation mode (select public-domain translations to see actual parallel text), custom references and single-column reader.
- Event/reference-string filter, event favorites, yellow verse highlights, autosaved notes, saved comparisons, backup/restore and printing.
- Public-domain text fetched from https://bible-api.com/ (WEB, ASV, KJV); internet needed for uncached passages. Requests are spaced to reduce service load. The app shell and successfully fetched public-domain passages can be cached on supported browsers.
- NIV, ESV and NLT are external reading links only. No licensed full text, API keys or copyrighted Bible datasets are included. KJV use is subject to local rights (notably the UK).

## Limitations and roadmap
This is a starter release, not the complete multi-phase specification. Local storage is used instead of IndexedDB. No full-text concordance, fuzzy search, verse-range alignment, multi-color highlights, cloud backup, note tags, or licensed Bible API backend. The Bible reader uses typed references. Notes and highlights are local to this browser and can be lost when clearing site data; export backups regularly. The source PDF is not redistributed; verify rights to publish its arrangement and event titles before using a public repository. No claim of theological equivalence between parallels.

## Testing
JavaScript syntax and JSON structure checked in the build environment. Live API access and browser execution were not verified there because network access was unavailable. After deployment, test Feeding of the five thousand (four columns), The good Samaritan (one column), The sermon on the mount (cross-chapter range), NIV/ESV/NLT links, notes persistence, backup/restore, mobile scrolling, and offline access to a previously loaded passage. The external Bible service can be unavailable or rate-limited.

## Licensed translations
To integrate in-column NIV/ESV/NLT text, obtain authorized access from the relevant publisher or provider and implement a server-side proxy with credentials stored in server secrets; never put private keys in GitHub Pages JavaScript. Follow the provider's display, caching and export terms. See https://api.esv.org/ and https://scripture.api.bible/ for provider information.
