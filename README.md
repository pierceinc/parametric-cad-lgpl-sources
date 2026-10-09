# parametric-cad library sources

This repository hosts versioned source downloads for the Open CASCADE and
PlaneGCS libraries distributed with parametric-cad. Pierce Inc. maintains these copies.

## Current downloads

Library versions: `replicad-opencascadejs 0.23.0` and `@salusoft89/planegcs 1.2.0`.

- [OCCT, bindings, and build inputs](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/download/sources-2026-10-08-873c478f382a/opencascade-replicad-0.23.0-complete-source.tar.gz)
- [PlaneGCS, bindings, and build inputs](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/download/sources-2026-10-08-873c478f382a/planegcs-1.2.0-complete-source.tar.gz)
- [Build and replacement instructions](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/download/sources-2026-10-08-873c478f382a/BUILDING-AND-REPLACING.md)
- [Source manifest](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/download/sources-2026-10-08-873c478f382a/manifest.json)
- [SHA-256 checksums](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/download/sources-2026-10-08-873c478f382a/SHA256SUMS)

Download the files into one directory, then run `sha256sum -c SHA256SUMS`.
The instructions explain how to rebuild the libraries and use matching generated
JavaScript/WASM pairs with the browser worker.

Each archive retains its libraries' licenses, copyright notices, source inputs,
patches, headers, binding generators, and build configuration. Refer to the
licenses inside each archive for its terms.

## Upstream projects

- [replicad](https://github.com/sgenoud/replicad)
- [OpenCascade.js](https://github.com/donalffons/opencascade.js)
- [Open CASCADE](https://github.com/Open-Cascade-SAS/OCCT)
- [PlaneGCS](https://github.com/Salusoft89/planegcs)

Exact commits, toolchain image digests, and shipped library hashes are recorded
in [source-lock.json](source-lock.json) and the downloadable manifest.

## Verification and retention

See [VERIFICATION.md](VERIFICATION.md) for the recorded technical checks.
Keep each release's files at its versioned URL while the corresponding app
release is distributed. Publish changed sources under a new version.

The parametric-cad application is maintained separately. This repository contains
library source downloads and their publication records.
