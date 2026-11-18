# Assembly Studio Desktop

**DNA assembly planning, oligonucleotide design and construct verification in a local desktop application.**

Developed by Diego Bonatto · LBCM · Universidade Federal do Rio Grande do Sul (UFRGS), Brazil.

[Download installers](https://github.com/bonattod/assembly-studio-desktop/releases/latest) · [Português](README.pt-BR.md) · [Validation](VALIDATION.md) · [Report an issue](https://github.com/bonattod/assembly-studio-desktop/issues)

## Downloads

Choose the package for your operating system and processor. The published Windows and Linux installers are version 1.14.0 and can be downloaded without requesting web access.

**Apple Silicon / M1:** use the corrected macOS 1.14.1 package and follow the [Mac installation guide](INSTALL-MACOS.md), including the “Apple could not verify…” instructions. The corrected installers are available in [release 1.14.1](https://github.com/bonattod/assembly-studio-desktop/releases/tag/v1.14.1). The 1.14.0 Mac packages remain archived in the old release and had a signing problem.

| Platform | Package |
| --- | --- |
| Windows, x64 | [Windows installer (.exe)](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-win-x64.exe) |
| Debian / Ubuntu Linux, x64 | [Debian package (.deb)](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-linux-amd64.deb) |
| Other compatible Linux distributions, x64 | [Linux archive (.tar.gz)](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.0/Assembly-Studio-Desktop-1.14.0-linux-x64.tar.gz) |
| macOS, Apple Silicon / M1 | [Apple Silicon / M1 DMG (1.14.1)](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-arm64.dmg) |
| macOS, Intel | [Intel DMG (1.14.1)](https://github.com/bonattod/assembly-studio-desktop/releases/download/v1.14.1/Assembly-Studio-Desktop-1.14.1-mac-x64.dmg) |

[SHA-256: Windows/Linux 1.14.0](SHA256SUMS-Assembly-Studio-Desktop-1.14.0.txt) · [SHA-256: macOS 1.14.1](SHA256SUMS-Assembly-Studio-Desktop-1.14.1.txt) · [Installation guide in Portuguese](LEIA-ME-Assembly-Studio-Desktop.txt)

The automatically generated **Source code** archives on the release page contain this distribution repository's documentation, not the application source or an installer. Download a platform-specific package from the table above.

## What the application does

- Plans **in vitro assembly**, including Gibson/homology workflows and TPA Designer.
- Supports **in vivo assembly and recombination**, including assisted plasmid editing.
- Provides **Golden Gate / Type IIS** assembly profiles and data-assisted junction planning.
- Helps design and assess oligos, with checks on both DNA strands and method-aware identifiers.
- Combines selected assembly workflows, consolidates identical oligo sequences and exports synthesis lists.
- Includes vector assessment, PCR/restriction verification, sequencing-based verification planning, combinatorial assembly and functional annotation transfer.
- Imports and exports supported FASTA, GenBank, SnapGene and project formats; synthesis tables support tab-delimited ordering workflows.

The interface is in English. This is a planning and analysis tool: computational predictions do not establish experimental yield, ligation fidelity or the proportion of correct clones.

## Install and start

**Windows:** run the `.exe` installer, choose the destination and open **Assembly Studio Desktop** from the Start menu or desktop shortcut.

**Debian / Ubuntu:** open the `.deb` with the system package installer, or run this command from the download directory:

```sh
sudo apt install ./Assembly-Studio-Desktop-1.14.0-linux-amd64.deb
```

**Other compatible Linux distributions:** extract the `.tar.gz` and run `./assembly-studio-desktop` from the extracted directory. Keep its files together. System graphical libraries are required. Run as a normal user; do not disable Chromium's sandbox to work around compatibility problems.

**macOS Apple Silicon / M1:** follow the [dedicated installation guide](INSTALL-MACOS.md) ([Português](INSTALL-MACOS.pt-BR.md)). It identifies the ARM64 installer, gives its checksum and explains the per-app **Open Anyway** procedure. For an Intel Mac, select the 1.14.1 `mac-x64` package and its corresponding checksum instead.

The macOS 1.14.1 package uses an ad-hoc signature; it has no Apple Developer ID signature or notarization. Native macOS startup checks passed, but first-launch approval on a clean end-user Mac remains unverified. The Windows installer also lacks a publisher signing certificate. See [validation and limitations](VALIDATION.md).

## Projects and offline operation

- End users do **not** need to install Python or Node.js. Local engines and required scientific assets are included.
- Open projects with **Open project** or `Ctrl+O` (`Cmd+O` on macOS).
- Save with **Save project** or `Ctrl+S` (`Cmd+S` on macOS). Integrated projects use `.assembly.json` and are compatible with the web edition.
- **Save before closing: there is no automatic project saving.**
- Local calculations and exports run on the computer. Explicit NEB requests and links to external websites require an internet connection.
- Updates are manual: install a newer package and reopen your saved project. There is no automatic updater or cloud project synchronization.

The [hosted web edition](https://assembly-studio-lbcm.diegobonatto.chatgpt.site) remains available under its existing access rules. Public desktop downloads do not change web access permissions.

## Verify a download

Download the checksum file from the same release. On Linux, run:

```sh
sha256sum -c SHA256SUMS-Assembly-Studio-Desktop-1.14.0.txt --ignore-missing
```

On macOS, compute a downloaded file's hash using `shasum -a 256 <filename>`. On Windows PowerShell, use `Get-FileHash <filename> -Algorithm SHA256`. Compare all 64 hexadecimal characters with the corresponding line in the checksum file. A matching checksum confirms byte integrity; it does not replace publisher code signing.

## Feedback and citation

Use [Issues](https://github.com/bonattod/assembly-studio-desktop/issues) to report a problem or suggest a feature. Include the application version, operating system and steps to reproduce. Share a minimal synthetic example when possible; issues and attachments in this repository are public.

Suggested citation: **Bonatto, D. (2026). Assembly Studio Desktop (Version 1.14.1) [Computer software]. LBCM, UFRGS. https://github.com/bonattod/assembly-studio-desktop**

Machine-readable citation metadata is provided in [CITATION.cff](CITATION.cff). Cite the original scientific methods relevant to your analysis as well; this software does not replace those references.

## Repository scope

The original Assembly Studio code and documentation are licensed under the [MIT License](LICENSE). Third-party components retain their own terms; see [license scope and notices](THIRD_PARTY_NOTICES.md).

This public repository distributes installers and documentation. The development repository remains private; adding the MIT license does not itself make the source code publicly available.

Contact: [diego.bonatto@ufrgs.br](mailto:diego.bonatto@ufrgs.br).
