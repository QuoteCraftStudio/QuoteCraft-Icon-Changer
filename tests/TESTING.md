# Testing and verification

Original feature tests (v1.0.0): SHA-256 `4021d024c014d223afabcd1747e66f8dadaabf0a20b9728b6e2eb8643a4ad9ed`.

Current published and repository version (v1.0.1): SHA-256 `c87e48f01034f27b0f1fab943c93a747c5483b4002d2440b955c117159fda99e`.

## Automated browser checks — passed

Tested with headless Chromium / Playwright (external CSS/icon CDNs blocked for deterministic JavaScript checks).

- Application initializes and displays preset icon options.
- `.url` input preserves the full HTTP(S) destination including query strings.
- Generated shortcut ZIP opens without errors and contains a `.url` and a 256×256 `.ico`.
- Exported URL has a relative `IconFile` pointing to the included `.ico`.
- Selected local PNG is previewed, searchable and exported as the correct icon artwork.
- A user-selected directory contributes compatible icon images to the gallery.
- Invalid APK data does not generate a fabricated URL, and invalid launches are blocked.
- Custom icon text is treated as literal text rather than HTML.
- No JavaScript page errors were observed in these checks.

## Website deployment check — passed

The live QuoteCraft Studio `IconChanger.html` and `apps.html` returned HTTP 200 and matched their expected SHA-256 digests in the previous deployment verification. The standalone app's deployed SHA-256 matches the `index.html` in this repository.

## Manual platform checks — not yet completed

- Opening the downloaded `.url` and seeing its icon on a real Windows desktop.
- Browser folder-selection behavior across different Android devices and browser versions.
- Behavior of a wide selection of real APK and `.lnk` formats.

These results describe the tests performed, not a claim of full platform or APK compatibility.

## Consent-notice regression test — 2026-11-02

Local Chromium browser check passed for the Icon Changer consent notice: the checkbox initially remains unchecked, **I agree — open app** is disabled until checked, Privacy and Terms links display correctly, and the original 15 icon choices remain available after acceptance. The notice collects no account or server-side acceptance record.

The apps collection consent popup for APK download links was checked in a browser fixture for checkbox state and cancellation, without changing download targets. On-device APK launches and individual installed Android apps have not been modified by this HTML-only update.
