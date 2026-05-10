---
date_published: 2026-05-09
date_modified: 2026-05-09
canonical_url: https://github.com/IKE-Network/example-project/built-with.html
---

# Built With

Open-source software that `example-project` 4 depends on, links against, ships within, or invokes at runtime.

Three layers of attribution ship with each release:

- [Software Bill of Materials (CycloneDX, JSON)](bom.json)[1] — full transitive dependency graph with SPDX-normalized licenses and artifact hashes. Ingestible by Dependency-Track, Trivy, Snyk, GitHub’s dependency graph.
- [Licenses (SPDX)](licenses.html)[2] — human-readable SPDX-grouped view of declared dependencies, generated from `bom.json` (#335).
- This page — curated companion covering what mechanical reports can’t see (Maven Site skin, external services, fonts inside artifacts, frontend assets in rendered HTML).

## [#mechanical-inventory](#mechanical-inventory)Mechanical inventory

Direct dependencies of this module, grouped by SPDX expression. Generated from `bom.json` at build time.

| SPDX Expression | Components |
| --- | --- |
| `Apache-2.0` | 5 |
| `Apache-2.0 OR MIT License (DocBook XSL Stylesheets)` | 1 |
| `OFL-1.1` | 1 |
| **Total** | **7** |

For full per-component detail (group, artifact, version, hashes, transitive deps), see [bom.json](bom.json)[1] or [licenses.html](licenses.html)[2].

## [#related](#related)Related

- [site index](index.html)[3]
- [ike-issues#336](https://github.com/IKE-Network/ike-issues/issues/336)[4] — the issue that introduced this page (rename of the legacy "Third-Party Notices" to friendlier "Built With").
