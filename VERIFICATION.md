# Source verification record — October 9, 2026

Full-source verification passed for [the current source release](https://github.com/pierceinc/parametric-cad-lgpl-sources/releases/tag/sources-2026-10-08-873c478f382a).
The [retained verification record](verification/full-source-2026-10-09.json)
contains archive hashes, rebuilt JS/WASM hashes, and browser test results.

| Check | Result |
| --- | --- |
| Installed package versions and generated JavaScript/WASM hashes | Match the retained source lock |
| Anonymous public downloads, source provenance, archive contents, and SHA256SUMS | Passed |
| PlaneGCS source rebuild | Passed with the archived sources, included headers, and pinned toolchain |
| OCCT full C++ source compilation | The archived Dockerfile compiled 258 standard bindings and all 5,387 selected C++ files locally. A file-hash audit confirmed the cached compilation inputs match this release; only documentation and a toolchain comment changed. |
| Final OCCT source-build link | Passed after increasing Docker from 8 to 12 GB; the cached compilation was reused |
| Matching rebuilt library pairs in the production browser worker | All four replacement assets loaded; radius edits changed extrusion width from 20 to 30 mm; STL export succeeded (389,636 bytes) |
| Solver and OCCT history tests with both rebuilt library pairs | All 22 checks passed |

The earlier 8 GB link attempts received SIGKILL. The October 9 run completed the
full-source check, including the final link and both replacement pairs. These
results use the archived source-build procedure; the OCCT source-build image
compiles its C++ objects from the archived sources.

Rebuilt files can differ from the shipped hashes. Compatible generated
JavaScript/WASM pairs must be used together. The checks provide build and
replacement evidence; they do not establish byte-for-byte reproducibility or
compatibility after changing the exported interface.

Licenses, source distribution, and the browser replacement method remain
subject to the distributor's release review. Verifying the deployed app's
source links remains a separate deployment check.
