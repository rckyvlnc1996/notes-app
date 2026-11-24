# Notes

A simple notes app. Write, time-stamp and delete notes; they're saved on the device.

Built with [Capacitor](https://capacitorjs.com/) — the app is plain HTML/CSS/JS in `www/`, wrapped into a native Android APK.

## How it's built

There is no need to build anything on your phone. When you push to the `main`
branch on GitHub, the workflow in `.github/workflows/build.yml` runs on
GitHub's servers and produces an installable APK.

### Getting the APK

1. Push this repo to GitHub.
2. Open the repo's **Actions** tab and wait for the build to finish (a few minutes).
3. Open the finished run and download **notes-app-debug-apk** under "Artifacts".
4. Unzip it, copy `app-debug.apk` to your phone, and tap to install
   (you'll need to allow "install from unknown sources" once).

This is a **debug** APK — perfect for installing on your own phone. A signed
**release** APK (needed for the Play Store) is a later step.

## Project layout

- `www/index.html` — the whole app (UI + logic).
- `capacitor.config.json` — app name and ID.
- `package.json` — Capacitor dependencies.
- `.github/workflows/build.yml` — the cloud build.
