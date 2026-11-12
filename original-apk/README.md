# Base APK contract

The repository tracks metadata only. The stock APK is stored as the single
asset of the prerelease named by `manifest.json`.

For the current input:

- TikTok: `47.7.3` (`2024707030`)
- tag: `base-tiktok-47.7.3-r1`
- asset: `TikTok-47.7.3-stock.apk`
- SHA-256: `9b35d4caed14ae54938eca1fa27fc89ce8307a9cf8350b80f66a9968fc3684e9`

Use the plain 47.7.3 APK from APKMirror (arm64-v8a + armeabi-v7a, nodpi), not
the `.apkm` bundle: the desktop patcher's bundle merge moves resource files
around, and HushFeed's Accent color, AMOLED dark theme and Custom launcher icon
patches refuse that result.

GitHub release immutability is enabled, and revision 1 is protected by it. If
the bytes ever need to change, increment `base_apk.revision`, create a new
`-rN` prerelease, and update the manifest. Never replace the asset behind an
existing tag.
