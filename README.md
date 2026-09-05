# Minimal Calendar — GitHub APK Build

A mobile-friendly offline calendar packaged as an Android APK with Capacitor.

## Build APK on GitHub

1. Upload the complete project to a GitHub repository.
2. Use the `main` or `master` branch.
3. Open **Actions** → **Build Android APK**.
4. Click **Run workflow** if it has not started automatically.
5. Open the completed workflow run.
6. Under **Artifacts**, download `minimal-calendar-debug-apk`.
7. Extract the artifact and install `app-debug.apk` on Android.

### Important
This workflow does **not** use npm dependency caching because there is no committed `package-lock.json`. GitHub's `setup-node` npm cache requires a lockfile; disabling that cache fixes the `Dependencies lock file is not found` error.

## Project structure

- `www/index.html` — calendar app
- `www/manifest.json` — PWA metadata
- `www/sw.js` — offline cache
- `capacitor.config.json` — Android wrapper configuration
- `.github/workflows/build-apk.yml` — automatic GitHub APK build
- `package.json` — Capacitor dependencies
