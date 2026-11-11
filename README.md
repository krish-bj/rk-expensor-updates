# RK Expensor Updates

This public repository hosts update metadata for the RK Expensor Android app.

## Update channel

- Manifest: `version.json`
- APK files: publish as assets on GitHub Releases (do not commit APK binaries to this repository).

## Publishing a release

1. Build a signed release APK using the same Android application ID and signing key as the installed app.
2. Increase `versionCode` for every release.
3. Create a GitHub Release and attach the APK asset.
4. Update `version.json` with the new version, versionCode, release notes, exact release asset URL, and SHA-256 checksum.
5. Set `mandatory` to `true` only when the update must be installed before continuing.

The app verifies the APK checksum before opening Android's package installer. Android may require the user to allow installs from RK Expensor; installation is always confirmed by Android.
