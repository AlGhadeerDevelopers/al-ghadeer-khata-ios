# Al Ghadeer Khata Pro — iOS Dual-Track Deployment Guide (iPhone & iPad)

**App Name:** Al Ghadeer Khata Pro  
**Bundle Identifier (`appId`):** `com.alghadeer.khatapro`  
**Official Support Email:** `info.alghadeer@yahoo.com`

## Track A — Instant iOS Progressive Web App (No MacBook or App Store Fee Required)

Because `www/index.html`, `www/manifest.json`, and `www/sw.js` are pre-configured with Apple's standalone WebKit engine and offline Service Worker caching, you can host the `www/` folder for free on **GitHub Pages**, **Netlify**, or **Vercel** and install it on any iPhone or iPad in 10 seconds:

1. Upload the files inside `www/` (`index.html`, `manifest.json`, `sw.js`, `icon (2)_2.jpg`) to any HTTPS host (such as GitHub Pages).
2. Open the link in **Safari** on any iPhone or iPad.
3. The built-in **"Install Al Ghadeer Khata Pro on iOS"** banner automatically appears at the bottom of the screen.
4. Tap **Share (`⬆️`) -> Add to Home Screen (`➕`) -> Add**.
5. The app launches full-screen from the iPhone Home Screen with your official Al Ghadeer icon, `0 PKR` persistent vault (backed by `localStorage` + `IndexedDB` + `navigator.storage.persist()`), and works **100% offline**.

## Track B — Native iOS `.ipa` Compilation in the Cloud via GitHub Actions (`macos-latest`)

Just like your Android `.apk` build, you can compile the native iOS `.ipa` package directly from your Windows PC using GitHub's cloud Mac servers (`macos-latest`):

1. Create a new repository on GitHub (for example, `al-ghadeer-khata-ios`).
2. Upload the contents of `Al_Ghadeer_Khata_Pro_iOS_Suite.zip` (`package.json`, `capacitor.config.json`, `www/`, `ios-template/`) to the repository.
3. Create `.github/workflows/build-ios.yml` on GitHub using the workflow file included in `.github/workflows/build-ios.yml`.
4. Open the **Actions** tab on GitHub, wait ~4 minutes for the `macos-latest` Xcode runner to finish, and download **`Al-Ghadeer-Khata-Pro-iOS-IPA`** (`Al-Ghadeer-Khata-Pro-iOS.ipa`).
5. You can sideload the `.ipa` onto any iPhone/iPad using **Sideloadly** or **AltStore** from Windows, or sign it with an Apple Developer Certificate for TestFlight / App Store distribution.
