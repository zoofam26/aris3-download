# aris3-download

Public distribution hub for **Aris3**, an unofficial Android client for the
University of Dar es Salaam **ARIS 3** student portal
([aris3.udsm.ac.tz](https://aris3.udsm.ac.tz)).

This repository hosts:

* the **download page** (served via GitHub Pages → <https://zoofam26.github.io/aris3-download/>)
* `latest.json` — the version manifest the app's forced-update gate reads
* the **public releases** carrying the universal Android APK

> The app source lives in the private repository `zoofam26/aris3-app`.
> This public mirror exists so every client can reach the latest APK and
> manifest **anonymously**.

## For students

1. Open <https://zoofam26.github.io/aris3-download/>
2. Tap **Download APK** and allow the install (first time only)
3. Sign in with your normal ARIS 3 credentials — they never leave your device

## Release flow

Releases are cut by tagging `vX.Y.Z` on `aris3-app`; CI builds every platform,
publishes the private release, then mirrors the universal APK here and rewrites
`latest.json`. The landing page binds to the manifest, so it always offers the
newest verified build.
