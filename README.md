# Alberta Prime Blinds — Camera + PDF Fix (v3 source project)

**Not an APK.** To build a new installable APK, upload the contents of this ZIP (NOT the ZIP itself) to an Android SDK environment or GitHub Actions.

## Fixed in source
- Android WebChromeClient file chooser opens Camera or Gallery from image upload buttons.
- Android FileProvider URI supplies a writable camera destination.
- Print and Save PDF are separate buttons on the quotation page.
- A standalone printable Android WebView renders just the quotation and its logo/watermark, then opens the native Android print UI.
- Save PDF: In the Android print UI, choose **Save as PDF** and tap the save/PDF icon; select a device folder. This approach uses native Android printing rather than attempting to download a blob from inside an offline WebView.
- Product, control price, measurements, quotation storage and JSON backup retained.

## Building with GitHub Actions
1. Extract the ZIP to a folder. Keep `app/...`, `build.gradle.kts`, and `.github/workflows/build-apk.yml` in the repository root.
2. On GitHub, upload the extracted project tree to `cesar050520/alberta-prime-blinds` as files (not just a ZIP file).
3. On the repository **Actions** tab, run **Build and publish Alberta Prime APK**. Download the generated APK from Actions Artifacts or Releases.

**Do NOT uninstall your existing app until you have exported a JSON backup.** A new signing key may require uninstalling the older APK, erasing its private app storage. This project is not a tested binary and a successful Android device test is still required.
