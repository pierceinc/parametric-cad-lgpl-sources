# Source verification record — October 8, 2026

These records concern the libraries in the current release manifest. This publication updates the project name in the guide and a toolchain comment. Library C++ sources, bindings, and compiler flags are unchanged from the previously checked archives.

| Check | Result |
| --- | --- |
| Installed package versions and generated JavaScript/WASM hashes | Match the retained source lock |
| Source provenance, archive contents, and SHA256SUMS | Checked before publication |
| PlaneGCS source rebuild | Passed with the archived sources and pinned toolchain |
| OCCT custom rebuild using the pinned builder's precompiled OCCT objects | Passed |
| Matching rebuilt library pairs in the production browser worker | Passed: solve/edit a radius dimension, extrude, check changed dimensions, export STL |
| Solver and OCCT history tests with both rebuilt library pairs | 22 checks passed |
| OCCT full C++ source compilation | The archived Dockerfile compiled 258 standard bindings and all 5,387 selected C++ files locally using the same C++ inputs before this documentation update |
| Linking OCCT after the full C++ source build | Pending: linker received SIGKILL in the shared 8 GB Docker VM, including on a retry with lower process-memory overhead |

The full-source link remains unverified. The successful custom rebuild uses
precompiled OCCT objects and is a separate result. Rebuilt files can have
different hashes from the shipped files; compatible JavaScript/WASM pairs must
be used together.

Licenses, source distribution, and the browser replacement method remain
subject to the distributor's release review.
