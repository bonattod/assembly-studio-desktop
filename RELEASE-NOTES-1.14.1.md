# Assembly Studio Desktop 1.14.1 — macOS packaging update

This patch addresses the macOS packaging problem reported when opening version 1.14.0 on Apple Silicon. It updates the desktop shell to 1.14.1 and retains scientific core 1.14.0.

## Download selection

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

Close the previous application, open the matching DMG, and copy Assembly Studio Desktop to Applications. Open the copy in Applications.

These builds use **ad-hoc signatures**. They are **not Apple Developer ID signed or notarized**. macOS may therefore require a per-app “Open Anyway” confirmation in System Settings > Privacy & Security after an opening attempt. Only approve a download whose source and checksum you have verified. Do not disable Gatekeeper system-wide.

Apple's guidance: https://support.apple.com/en-us/102445

If opening still fails, report the exact error message, macOS version, chip architecture, and installer filename.

## Integrity

The accompanying `SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt` lists the two DMG checksums.
