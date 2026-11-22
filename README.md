# Buddy Portfolio Analyst website (GitHub Pages)

Ready-to-publish static site: plain HTML + CSS, no build step. **Nothing has been pushed or published.**
Prepared Nov 19, 2026 for app version 0.84 (build 85).

## What changed
No local clone of a GitHub Pages repo was found on this Mac (no `CNAME`, no `*.github.io` / `buddyportfolio` git remote).
The earlier 4-file draft in `AppStore/website/` (index / privacy / terms / style.css) is superseded by this folder; it was left untouched.

| File | What it is |
|---|---|
| `index.html` | New landing page: what the app is, features up to 0.84 (portfolio + Today, Stock Analysis with grades and indicators, Market Health, Portfolio City, Goals, Trophies, IPOs, Crypto, Live Activities, widgets, Siri / Shortcuts, Apple Watch, Mac, haptics, holidays, on-device Apple Intelligence), plans and prices, App Store badge placeholder (no link). |
| `support.html` | New. Contact, manage / cancel / restore / refund a subscription, FAQ and troubleshooting from `Docs/USER-GUIDE.md`. |
| `privacy.html` | Rewritten from `AppStore/PRIVACY-POLICY.md` (Nov 19 draft): adds notes, goals, morning brief, feedback & diagnostics; one extra section "This website" (GitHub Pages, no cookies/analytics). |
| `terms.html` | Apple's Standard EULA link + "For information only. Not investment, tax or legal advice." + the earlier terms (subscriptions, data, AI, no warranty). |
| `style.css` | Colours from `MyApp/Design/Theme.swift` (Light / Dark palettes, Coral accent), darkened where needed for 4.5:1 contrast. Follows the system light / dark setting. |
| `img/` | App icon (`icon-256.png`, `apple-touch-icon.png`, `favicon-64.png`, resized from `AppStore/Icon/final/icon-ios.png`) and screenshots `img/screens/01-home.jpg` … `06-lock-screen.jpg` (660 × 1434, from the Nov 20, 2026 iPhone 6.9" App Store set in `AppStore/Screenshots/2026-11/iPhone-6.9/`). |
| `_config.yml` | Tells GitHub Pages not to publish this README. |

Wording follows the app's rule (describe, never direct; no promises of returns). Prices: Plus $2.99/mo or $23.99/yr, Pro $5.99/mo or $47.99/yr, free week on yearly plans (from `BuddyPortfolio.storekit` / `APP-STORE-LISTING.md`). Plan contents from `PaywallSheet.swift` and the Guide's Plans table.

## Before publishing (owner)
1. **Screenshots:** done Nov 20, 2026 (real 660 px JPGs replaced the SVG placeholders). When the App Store screenshots change, re-export with `sips -s format jpeg -z 1434 660` and keep the `alt` text accurate.
2. **App Store badge:** once the app is live, replace the "Coming soon" box in `index.html` with Apple's official badge (developer.apple.com/app-store/marketing/guidelines) linking to the app's App Store page.
3. **Privacy policy:** effective date is set to Nov 19, 2026. If you name the market-data provider (TODO D3 / P1) or change anything, update both `privacy.html` and `AppStore/PRIVACY-POLICY.md` and the date. Lawyer review is still on the checklist.
4. **Support email:** the site uses `akhoale@gmail.com` (as the old site, the privacy policy and the review notes did). The app's **Send feedback** button uses `akhoale@gmail.com` (`FeedbackAndDiagnostics.swift`). Pick one and make them match.

## How to publish (GitHub Pages)
1. github.com, signed in as **akhoale** → **+ → New repository** → name **`buddyportfolio`**, **Public** → Create.
2. **Add file → Upload files** → drag in everything inside this `Website/` folder (including `img/` and `_config.yml`) → **Commit changes**.
   (Or from Terminal: `cd Website && git init && git add . && git commit -m "Website" && git branch -M main && git remote add origin https://github.com/akhoale/buddyportfolio.git && git push -u origin main`.)
3. **Settings → Pages** → Source **Deploy from a branch**, Branch **main**, folder **/ (root)** → Save.
4. After a minute, open each page on your iPhone to check it loads.

## URLs (must match everywhere)
| Where | URL |
|---|---|
| App Store Connect → Support URL | `https://akhoale.github.io/buddyportfolio/support.html` |
| App Store Connect → Marketing URL | `https://akhoale.github.io/buddyportfolio/` |
| App Store Connect → Privacy Policy URL | `https://akhoale.github.io/buddyportfolio/privacy.html` |
| App description → Terms of Use | `https://akhoale.github.io/buddyportfolio/terms.html` (keep App Store Connect's License Agreement on Apple's standard EULA) |
| App → `LegalLinks.privacy` (`MyApp/App/Legal.swift`) | `https://akhoale.github.io/buddyportfolio/privacy.html` — already this value; if the repo name or domain changes, change it there too |
| App → `LegalLinks.terms` | Apple's standard EULA (unchanged) |

The **Privacy Policy URL in App Store Connect and `LegalLinks.privacy` in the app must be the same address**, and the page must be live before you submit. If you ever use a custom domain (a `CNAME` file), every URL above changes, including `LegalLinks.privacy` in the app.
