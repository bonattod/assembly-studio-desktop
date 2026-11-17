# Assembly Studio Desktop 1.14.1 — macOS packaging update

This patch addresses the macOS packaging problem reported when opening version 1.14.0 on Apple Silicon. It updates the desktop shell to 1.14.1 and retains scientific core 1.14.0.

## Download selection

**Publication status, checked on 17 November 2026:** installer upload to GitHub Releases is pending. These notes document the prepared macOS update, not a completed public release. See the [installation and availability guide](INSTALL-MACOS.md) ([Português](INSTALL-MACOS.pt-BR.md)).

- Apple Silicon (M1, M2 and later): `Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg`.
- Intel Macs: `Assembly-Studio-Desktop-1.14.1-mac-x64.dmg`.
- Windows and Linux: continue using their existing 1.14.0 installers.

## What changed

- Ad-hoc signing is now explicitly applied to the macOS application and its helpers.
- Hardened runtime and the required Electron entitlements are configured.
- Packaging checks verify the DMG, verify the mounted and copied application signatures, and launch the copied application.
- The assembly and primer-design algorithms are unchanged by this packaging patch.

## Verification

Both installers passed their respective native macOS jobs. The application launch check verified renderer isolation, a WebAssembly operation, a 2,334-bp synthetic construct with six primers, and an unchanged project JSON round trip.

- ARM64: source commit `040576b8fea843f84b2d17dd307b2adc9770b34c`, workflow run `43895111174`, job `133396423778`.
- Intel x64: source commit `41b92aed2ff56ca73f95487cd580f205feb65451`, workflow run `43896425601`, job `133401265395`.
- The later source commit adjusts the CI verification script to use software rendering on the Intel hosted runner. The ARM64 test passed without that flag.
- These checks do not establish approval by Gatekeeper on a fresh end-user Mac.

## Installation and signing status

These builds use **ad-hoc signatures** and have **no Apple Developer ID signature or notarization**. The “Apple could not verify…” warning can therefore still appear after the packaging correction.

Follow the [Apple Silicon/M1 installation guide](INSTALL-MACOS.md) ([Português](INSTALL-MACOS.pt-BR.md)) for checksum verification, copying the application to Applications, the per-app **Open Anyway / Abrir Mesmo Assim** procedure and troubleshooting. Intel users must choose the x64 DMG and its corresponding checksum.

The guide links to Apple's official instructions and lists the details needed for a support report.

## Integrity

The accompanying `SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt` lists the two DMG checksums.
