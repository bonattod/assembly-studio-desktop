# License scope and third-party notices

The MIT license in LICENSE applies to the original Assembly Studio code and documentation, including the first-party portions of Assembly Studio Desktop 1.14.0. This licensing notice also accompanies the previously published 1.14.0 installers. Those binaries have not been rebuilt or replaced, and their published SHA-256 hashes remain unchanged.

The original installers predate this licensing update. Their embedded package metadata may still say `UNLICENSED`; this repository's explicit MIT grant applies to the original Assembly Studio code. Subsequent builds include LICENSE and this notice and use MIT package metadata.

## Components covered by their own terms

The MIT grant does not replace the existing copyrights, licenses or notices of bundled third-party components. Retain those notices when redistributing the application.

- **Electron and Chromium:** the desktop runtime carries its own LICENSE and LICENSES.chromium.html notices and other applicable notices.
- **Pyodide:** runtime notices are supplied as LICENSE-pyodide in the bundled runtime.
- **Python:** LICENSE-python contains the Python runtime notices.
- **Biopython and NumPy:** the runtime licenses directory contains the corresponding LICENSE/COPYING files and component-specific notices.
- Other dependencies and separately attributed resources retain the licenses and attribution that accompany them.

In the development repository, scientific runtime notices are under `dist/gibson/gibson/runtime/314.0.7/` and its `licenses/` directory. The desktop application packages those assets under `web/gibson/gibson/runtime/314.0.7/`.

Scientific articles, method names, product names and third-party logos are not relicensed by the application's MIT file. References to methods identify their scientific sources and do not imply endorsement.

## Source availability

The public `assembly-studio-desktop` repository currently distributes installers and documentation. The development repository remains private. Adding an open-source license does not by itself publish the application's source code, and this repository does not claim that the source is publicly available.

Contact: [diego.bonatto@ufrgs.br](mailto:diego.bonatto@ufrgs.br).
