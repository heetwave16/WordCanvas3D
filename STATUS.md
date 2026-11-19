# Project Status

## Active Task: Rename App to ToKens, Custom Color Theme & Top-Right GitHub Bar Removal

### Overview
1. Update the application name from `WordCanvas3D` to `ToKens`.
2. Apply the user-specified custom color palette across UI scopes:
   - **Midnight Violet**: `#210124`
   - **Dark Teal**: `#0B3C49`
   - **Scarlet Rush**: `#DF2A36`
   - **Beige**: `#E6EED6`
   - **Silver**: `#B3B6B7`
3. Remove the floating GitHub bar in the top-right corner of the navbar.
4. Run locally and deploy to Vercel production.

### Affected Files
- `STATUS.md`
- `Frontend/lib/site.js`
- `Frontend/messages/en.json`
- `Frontend/messages/zh.json`
- `Frontend/messages/ja.json`
- `Frontend/messages/es.json`
- `Frontend/components/Navbar.jsx`
- `Frontend/components/NotFound.jsx`
- `Frontend/components/landing/Interactive.jsx`
- `Frontend/styles/globals.css`
- `Frontend/components/landing/landing.module.css`
- `README.md`

### Completed Changes
1. **App Renaming**:
   - `Frontend/lib/site.js`: `SITE_NAME` updated to `ToKens`.
   - `Frontend/messages/{en,zh,ja,es}.json`: Updated app titles, pitch descriptions, drawer descriptions, copyright notices, and share strings across all supported languages.
   - `Frontend/components/NotFound.jsx`: Page title updated to `ToKens`.
   - `Frontend/components/landing/Interactive.jsx`: Web share fallback title updated to `ToKens`.
   - `README.md`: Header and documentation updated to reflect `ToKens`.

2. **Custom Color Palette**:
   - `Frontend/styles/globals.css`: Updated theme tokens (`:root` and `.dark`) with Midnight Violet, Dark Teal, Scarlet Rush, Beige, and Silver; updated `.loader-hl` and custom scrollbars.
   - `Frontend/components/landing/landing.module.css`: Ambient hero glow using Midnight Violet & Dark Teal; serif shimmer gradient across the 5-color palette; explore CTA button with Scarlet Rush/Dark Teal gradient; orbit particles, kickers, and terminal highlights aligned.
   - `Frontend/components/Navbar.jsx`: Brand logo updated to "To" + gradient "Kens" (`from-[#DF2A36] via-[#B3B6B7] to-[#0B3C49]`), active tabs styled with Scarlet Rush and Dark Teal glow, focus rings updated to Scarlet Rush.

3. **Top-Right GitHub Bar Removal**:
   - `Frontend/components/Navbar.jsx`:
     - Removed the external floating corner cluster (`fixed top-3 right-4 z-50 ...`).
     - Removed GitHub repository link (`GithubMark`, `REPO_URL`) and author avatar link (`PROFILE_URL`).
     - Kept and neatly integrated `LanguageMenu` directly inside the primary navigation bar.

4. **Local Execution & Vercel Production Deployment**:
   - Local dev server: Running at `http://localhost:3000`.
   - Vercel production deployment: Deployed to `https://tokens-app-six.vercel.app` (`https://tokens-app-heetwave16.vercel.app`).

### Verification & Test Results
- `node Frontend/scripts/check-messages.mjs zh ja es`: 441 entries validated per locale (0 missing keys, 0 tag mismatches).
- Production build: `next build --webpack` completed successfully (157 static pages compiled without errors).
- Vercel Deployment check: `readyState: "READY"`, aliases verified and responding live.

### Current Status
- Status: **DEPLOYED & RUNNING**
