# Install on Apple Silicon / M1

[Português](INSTALL-MACOS.pt-BR.md) · [Main page](README.md) · [Release notes](RELEASE-NOTES-1.14.1.md)

## Package and availability

For a MacBook Air M1 or another Apple Silicon Mac, use **`Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg`**. The `mac-x64` package is for Intel Macs.

The corrected macOS installers are published in [release 1.14.1](https://github.com/bonattod/assembly-studio-desktop/releases/tag/v1.14.1). The older 1.14.0 macOS packages had a signing problem; this guide is for **1.14.1**. Windows and Linux remain on 1.14.0.

Download the [Apple Silicon / M1 installer](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg) or, for an Intel Mac, the [Intel installer](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-x64.dmg). The automatically generated “Source code” ZIP is not an installer. For support, contact [diego.bonatto@ufrgs.br](mailto:diego.bonatto@ufrgs.br).

## Check and install the M1 package

1. Save any open projects as JSON, keep your saved project files, and close the old application.
2. Verify the downloaded DMG against the [1.14.1 checksums](SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt). In Terminal, from the directory containing the download, run:

   ```sh
   shasum -a 256 Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg
   ```

   Expected SHA-256:

   ```text
   e508e3e3bab922617935fb90788acd0e0546c3c4fd3197eb5aadfcf78844157f
   ```

   A match identifies the checked installer bytes; it is not a malware scan or Apple certification. If the hash differs, obtain a fresh copy before installing.
3. Open the DMG and copy **Assembly Studio Desktop** to **Applications**, replacing the previous application if prompted.
4. Open **Assembly Studio Desktop** from **Applications**.

## “Apple could not verify…” warning

You may see the following message:

> Apple could not verify “Assembly Studio Desktop” is free of malware that may harm your Mac or compromise your privacy.

Version 1.14.1 uses **ad-hoc signing** and has **no Apple Developer ID signature or Apple notarization**. This packaging correction does not remove that limitation. The warning alone does not establish that malware was detected.

After an opening attempt, proceed only if you trust the source and the checksum matches:

1. Open **System Settings → Privacy & Security** and scroll to **Security**.
2. Find **Assembly Studio Desktop** and select **Open Anyway**.
3. Confirm **Open** and authenticate on your Mac if prompted.

This creates an exception for the application. Keep Gatekeeper enabled. See [Apple’s official instructions](https://support.apple.com/en-us/102445).

## If it still does not open

If **Open Anyway** is missing, or the message says the application is **damaged** or **will damage your computer**, stop and report the exact message instead of applying the above procedure indiscriminately. Include the macOS version from **Apple menu → About This Mac**, processor, DMG filename and SHA-256 result. Do not post passwords or personal project data.

Report the issue through [GitHub Issues](https://github.com/bonattod/assembly-studio-desktop/issues) or the maintainer’s email above.

Native Apple Silicon checks covered DMG integrity, application signatures, startup and a synthetic assembly/project round trip. First-launch Gatekeeper approval on a clean end-user Mac remains unverified; see [validation details](VALIDATION.md).
