---
title: Commons Merged
description: Compilation of merged data packages for use on the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCIA: Life Cycle Impact Assessment
  LCI: Life Cycle Inventory
---

_Commons Merged_ is a merged database built from multiple data packages—i.e., data objects in a repository, as released with a version identifier) on the Federal LCA Commons. 
The database is assembled by the LCA Data Package Manager ([`LDPM`](https://github.com/FLCAC-admin/commons_merged/tree/main/ldpm)), which follows the original authors’ instructions for connecting processes via `exchange.defaultProvider` pointers across data packages. 

## Why Commons Merged?
Previously, when a user wanted to integrate an FLCAC data package into their local openLCA database, they had to individually download and import each package then manually link objects across them.
This prior workflow emerged as a work-around to an openLCA Collaboration Server limitation: it cannot preserve UUID pointers ([`Ref`](https://greendelta.github.io/olca-schema/classes/Ref.html)s) across packages (e.g., a process from package _X_ intends to consume the output reference flow of another process from package _Y_).

Instead, _Commons Merged_ offers users a single download with cross-package links already established, wherein all [`exchange.amount`](https://greendelta.github.io/olca-schema/classes/Exchange.html#amount) and [`.unit`](https://greendelta.github.io/olca-schema/classes/Exchange.html#unit) values are carefully preserved during the linking procedure. Furthermore the build routine (and linking subroutine) is deterministic: a unique [`manifest.toml`](https://github.com/FLCAC-admin/commons_merged/blob/main/ldpm/config/manifest.toml) input will yield a consistent, reproducible output[^1].

[^1]: Just like software package managers, wildcard specifiers like "*" (i.e., to use a depedency's latest version) must replaced by fixed version numbers to produce a consistent "frozen" build; otherwise the build will steadily change as new versions are released.

:::{important}
No changes are made to [`exchange.amount`](https://greendelta.github.io/olca-schema/classes/Exchange.html#amount) or [`.unit`](https://greendelta.github.io/olca-schema/classes/Exchange.html#unit) from the original sources.
:::

## Details
Within _Commons Merged_, individual processes are labeled with [`process.tags`](https://greendelta.github.io/olca-schema/classes/Process.html#tags) to denote their parent data package.
Cross-package connections are based on two sets of instructions: (1) the "defaultProvider.@id" JSON component of an `exchange.description` (example [here](https://www.lcacommons.gov/lca-collaboration/National_Renewable_Energy_Laboratory/USLCI_Database_Public/dataset/PROCESS/331207ab-8a06-400e-bace-9657a3e10732)) value embedded on each bridge process input, and (2) supplemental links established via the `LDPM`'s [`provider_links.yaml`](https://github.com/FLCAC-admin/commons_merged/blob/main/ldpm/config/provider_links.yaml) configuration file.
Despite their central role in supporting the pre-_Commons Merged_ workflow, [bridge processes](BridgeProcessesForUsers.md) have been preserved as containers for explicit declarations of cross-package connections (i.e., much like how `import` statements work in Python).

Furthermore, aside from serving as a tool to repeatedly mint _Commons Merged_ and _Commons Merged Hybrid_, the `LDPM` can also be used to build custom LCA databases using any desired combination of data packages and release versions available on the FLCAC.

:::{caution} Disclaimer
_Commons Merged_ includes a mixture of industry-supplied data and data from federal agencies and has not undergone additional review, nor does it constitute or imply an endorsement by the agencies of the Federal LCA Commons.
:::

## Releases

The pair of _Commons Merged_ builds made available on the FLCAC are listed below with their respective dependencies.
For the most up-to-date information, please refer to each database's description as hosted on the Commons.

<!-- ToDo: render latest manifest TOMLs directly from FLCAC-admin/commons_merged repo -->
1. **Commons Merged, _alpha_**

- USLCI: v1.2026-09.0
- US Electricity Baseline: v1.2026-06.1
- Forest and Forestry Products: v1.2026-09.1
- TRACI 2.2: v1.2025-04.0
- IPCC_GWP: v1.2026-09.0
- FEDEFL_Inv: v1.2024-12.0

2. **Commons Merged Hybrid (with USEEIO), _alpha_**

- USEEIO v2.0: v1.2022-06.0
- USLCI: v1.2026-09.0
- US Electricity Baseline: v1.2026-06.1
- Forest and Forestry Products: v1.2026-09.1
- TRACI 2.2: v1.2025-04.0
- IPCC_GWP: v1.2026-09.0
- FEDEFL_Inv: v1.2024-12.0

