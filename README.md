# GK Movies Android App

Native Android WebView application for GK Movies.

## App details

- App name: GK Movies
- Package: `com.gkmovies.app`
- Website: `https://gkmovies.com.ng/`
- Version: `1.2.1` (`versionCode 5`)
- Target SDK: Android 36
- Minimum SDK: Android 7.0 / API 24
- Download notifications: enabled

## Included features

- Native WebView without Chrome branding
- Fullscreen HTML5 video support
- Secure movie downloads using logged-in WebView cookies
- File upload support
- Swipe to refresh and offline cache
- Camera-cutout and system-bar safe layout
- GK Movies green, white and gold launcher and splash branding
- Movie-title downloads with Android progress and completion notifications
- Persistent login until the user explicitly logs out
- Firebase push notifications in the foreground and background
- Automatic subscription to topic `gk_movies_all`
- Notification taps open the supplied GK Movies link inside the app

## GitHub Actions signing secrets

Add these GK Movies signing repository secrets:

- `GK_KEYSTORE_BASE64`
- `GK_KEYSTORE_PASSWORD`
- `GK_KEY_PASSWORD`
- `GK_GOOGLE_SERVICES_JSON_BASE64` (optional fallback; Firebase configuration is included)

The expected key alias is `gk_movies`. The workflow produces APK and Play Store AAB artifacts.

The included Firebase Android configuration is registered to
`com.gkmovies.app`. Every active installation subscribes to topic
`gk_movies_all`. Send broadcast notifications to that topic to address all
registered devices at once.

## Important

The project uses `https://gkmovies.com.ng/`. Upload `assetlinks.json` to `https://gkmovies.com.ng/.well-known/assetlinks.json` before publishing.
