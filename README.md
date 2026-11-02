# Super Easy Icon Changer

**A simple, standalone HTML icon and shortcut utility by QuoteCraft Studio.**

Choose an icon from your computer or phone, explore ready-made designs, generate a custom gradient icon, and export a Windows web shortcut with its matching icon.

**[Open the live app](https://quotecraftstudio.ca/IconChanger.html)** · **[View the QuoteCraft Studio app collection](https://quotecraftstudio.ca/apps.html)**

## Highlights

- **Drag and drop:** Import APKs, Internet shortcuts (`.url`), Windows shortcuts (`.lnk`), compatible desktop shortcut files, or an image.
- **Find your icons:** Pick individual icon files or select a folder on a supported device. Filter the selected images by filename and preview them in a gallery.
- **Create an icon:** Choose a preset style, generate a gradient icon, or customize the icon appearance.
- **Keep the link:** Read HTTP(S) links from `.url` files and preserve the destination when exporting a replacement shortcut.
- **Export for Windows:** Download a ZIP containing the web shortcut (`.url`) and the matching Windows icon (`.ico`), or export an `.ico` alone.
- **Inspect APKs:** Read package identifiers from supported APK manifests when available, without inventing launch URLs.

Files selected for icon browsing are handled in your browser. This project does not require an account or upload your icon library to a server.


## Privacy, terms and responsibility

Visitors opening the browser edition on **QuoteCraftStudio.ca** see an unchecked acknowledgement before using the app. They can read the [Privacy Notice](https://quotecraftstudio.ca/privacy.html#privacy) and [App Terms & Responsibility Notice](https://quotecraftstudio.ca/terms.html), or choose **Not now** to return to the collection. The notice asks visitors to take responsibility for their own actions, device permissions and files to the extent the law permits; it does **not** remove non-waivable legal rights. No account, signature, or server-side acceptance record is collected by this notice.

The standalone HTML includes the same notice and links; reading the linked online notices requires an internet connection.

## Quick start

**Use it online:** Visit [Icon Changer](https://quotecraftstudio.ca/IconChanger.html).

**Run the standalone HTML locally:** Download `index.html` and open it in a modern browser. Internet access is needed for the page's Tailwind CSS and Font Awesome CDN assets; application file handling runs in the browser.

1. Drop in a shortcut or image, or paste a valid web destination.
2. Choose a preset icon, create one, or select **Choose Icon Files** / **Search a Folder** to use your own images.
3. Click **Open / Test Launch** for a valid HTTP(S) link.
4. Choose **Save Shortcut** for a ZIP with both `.url` and `.ico`, or **Save Icon Only** for an `.ico` file.
5. On Windows, extract the shortcut and icon together into the same folder.

## File compatibility

| Input | Supported behavior |
| --- | --- |
| PNG, JPG/JPEG, WebP, SVG, GIF, ICO | Select and preview as icons; export an ICO from a renderable image |
| `.url` | Read and preserve valid HTTP(S) destinations |
| `.lnk` | Inspect recognizable local shortcut paths, where available |
| APK | Inspect a supported package manifest; cannot install, run or recolor an Android app |
| `.desktop`, `.webloc` | Inspect supported web links |
| EXE / local app | Use an exported icon in the operating system's shortcut settings; browser cannot execute the app |

## Platform limitations

- **Device search requires selection:** A browser cannot silently scan a PC or phone. Choose a file or grant access to a folder using the file picker. Folder selection depends on browser and device support.
- **Windows desktop programs:** A webpage cannot directly edit an installed program's icon or launch an arbitrary local executable. Export the `.ico` and use Windows shortcut **Properties → Change Icon**.
- **Android installed apps:** A webpage cannot change installed app icons or launch arbitrary APKs. Use your Android launcher's icon customization features with exported images where supported.
- **Shortcut ZIP files:** The exported `.url` and `.ico` are designed to be kept together after extraction.

## Repository structure

```text
QuoteCraft-Icon-Changer/
├── index.html              # Standalone application (matches the published web version)
├── README.md               # Project overview and user instructions
├── CHANGELOG.md            # Version history
└── tests/
    └── TESTING.md          # Verified browser tests and remaining platform checks
```

## Quality checks

The tested edition was checked for `.url` handling, Windows shortcut ZIP contents, `.ico` export, icon-file and folder selection, filename search, malformed APK handling, user-input escaping, and JavaScript errors. See [testing notes](tests/TESTING.md).

## Support

QuoteCraft Studio · [quotecraftstudio.ca](https://quotecraftstudio.ca) · [support@quotecraftstudio.ca](mailto:support@quotecraftstudio.ca)

© 2026 QuoteCraft Studio. No open-source license is supplied with this repository.
