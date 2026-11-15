# Validation and limitations — 1.14.0

This release packages the Assembly Studio 1.14.0 scientific core in a desktop application. The original installers are redistributed unchanged; the SHA-256 file identifies their exact bytes.

## Automated validation

- **283 scientific/core tests** passed locally and in the Linux CI job.
- **10 desktop tests** passed locally and in all four CI targets: Linux x64, Windows x64, macOS Apple Silicon and macOS Intel.
- Desktop tests cover bounded file reads, allowed origins, external links, download names, traversal/symlink containment, prepared-bundle integrity and project compatibility.
- Scientific engine/module files in the prepared bundle match the web source. Desktop adapters add native menus/dialogs and local resource handling.
- All four platform jobs completed successfully. Build success is distinct from manual GUI or clean-machine installation testing.

## Manual packaged-application checks

Manual GUI verification was performed on **Linux**, using the packaged executable without disabling its sandbox:

1. Generated the bundled synthetic Gibson example using the local scientific engine.
2. Saved a project through the native dialog, checked it using the web project reader, restarted the application and reopened the project.
3. Generated the synthetic TPA example: 3,000 bp, three fragments, 12 assembly primers and six PCR reactions.
4. Exported native SnapGene and independently checked its packet structure: 3,000 bp and 18 primer records, including verification oligos.

The Linux package metadata was inspected. This was not a clean-machine installation test. Windows and macOS packages were built on corresponding CI operating systems; their GUI and installation behavior have not been manually validated in this release workflow.

## Operational limits

- No publisher code-signing certificate or Apple notarization. Institutional or operating-system policies may block installation.
- No automatic project saving, updater or cloud synchronization. Save JSON projects explicitly and keep backups before updating.
- Explicit NEB requests and external links require internet. A live NEB request was not part of desktop verification.
- The public desktop distribution has no dependency on the hosted website's email allowlist.
- Computational checks and protocol planning do not demonstrate wet-lab success, yield or the proportion of correct clones.

Report reproducible problems in this repository's Issues, preferably with synthetic examples and the operating-system/application versions.
