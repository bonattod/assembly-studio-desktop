# Assembly Studio Desktop 1.14.0

> **macOS update (17 November 2026):** the 1.14.0 Mac packages had a signing problem. Corrected 1.14.1 packages are available in [release 1.14.1](https://github.com/bonattod/assembly-studio-desktop/releases/tag/v1.14.1). For Apple Silicon/M1 installation and the Apple verification warning, see the [English guide](INSTALL-MACOS.md) or [guia em português](INSTALL-MACOS.pt-BR.md). Windows/Linux downloads remain at 1.14.0. The record below describes the original release.

First public desktop distribution of Assembly Studio, developed at LBCM / UFRGS for DNA assembly planning, oligonucleotide design and construct verification.

## Download

Choose the asset for your computer:

| System | Asset |
| --- | --- |
| Windows x64 | `Assembly-Studio-Desktop-1.14.0-win-x64.exe` |
| Debian / Ubuntu Linux x64 | `Assembly-Studio-Desktop-1.14.0-linux-amd64.deb` |
| Other compatible Linux x64 | `Assembly-Studio-Desktop-1.14.0-linux-x64.tar.gz` |
| macOS Apple Silicon | `Assembly-Studio-Desktop-1.14.0-mac-arm64.dmg` |
| macOS Intel | `Assembly-Studio-Desktop-1.14.0-mac-x64.dmg` |

The release also includes a Portuguese installation guide and SHA-256 checksums. The automatically generated **Source code** archives contain this distribution repository's documentation, not application source or installers.

## Included

- In vitro assembly (including Gibson and TPA), in vivo assembly/recombination and Golden Gate/Type IIS workspaces.
- Oligo assessment, combined synthesis exports, vector evaluation and PCR/restriction/sequencing verification tools.
- Bundled local scientific engines; no Python or Node.js installation required.
- Native menus and file dialogs, with JSON projects compatible with the web edition.
- The web edition remains available under its existing access permissions.

## Validation and known limitations

All 283 scientific/core tests and 10 desktop tests passed; desktop checks passed on all four CI platforms. Manual packaged-application verification was performed on Linux, including Gibson/TPA examples, project save/reopen and SnapGene export. Windows/macOS GUI and clean-machine installation testing remain outstanding.

These initial installers have no publisher signing certificate or Apple notarization. Operating-system or institutional policies may prevent installation. Do not disable system-wide security protections.

**Save projects explicitly: there is no autosave.** Updates are manual. Explicit NEB requests and external websites need internet. Computational validation does not establish experimental success.

See the repository README and VALIDATION.md for details. Feedback is welcome through Issues; use synthetic examples when sharing data publicly.

---

**Português:** os instaladores estão disponíveis publicamente. Escolha o arquivo do seu sistema, confira o SHA-256 e siga o guia `LEIA-ME-Assembly-Studio-Desktop.txt`. Os projetos são compatíveis com a versão web. A interface do programa está em inglês. Salve antes de fechar; não há salvamento automático.
