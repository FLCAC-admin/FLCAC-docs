---
title: FLCAC Merged
description: Compilation of merged data packages for use on the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCIA: Life Cycle Impact Assessment
  LCI: Life Cycle Inventory
---

FLCAC Merged is a merged data package that compiles versions of existing data packages (or repositories) on the Federal LCA Commons and combines them as intended by the original authors.
Where appropriate, this data package fills in default providers and aligns technosphere flows across source data packages.

## Why FLCAC Merged?
FLCAC Merged prevents users from needing to download multiple data packages individually and manually connecting data across them.
It also includes LCIA methods.
The openLCA Collaboration Server does not allow for making explicit connections across data packages (i.e., a process from Repository X intends to use as an input a process from Repository Y).
While [bridge processes](BridgeProcessesForUsers.md) have been used to highlight those connections, users still must download individual repositories and explicitly add default providers in openLCA or risk an incorrect linkage during product system creation.

:::{important}
No changes are made to exchange values from the original sources.
:::

## Details
Within FLCAC Merged, individual processes are labeled with Tags based on their source data package.
Documentation of the connections made across each data package is available within the [flcac-merged] data package manager python package [here](https://github.com/FLCAC-admin/flcac_merged/blob/main/ldpm/config/provider_links.yaml).
[flcac-merged](https://github.com/FLCAC-admin/flcac_merged) can also be used to develop custom merged data packages.

:::{caution} Disclaimer
FLCAC Merged includes a mixture of industry-supplied data and data from federal agencies and has not undergone additional review, nor does it constitute or imply an endorsement by the agencies of the Federal LCA Commons.
:::

## Releases

Versions of FLCAC merged which are available on the FLCAC are listed below with their compiled data packages.
For the most up to date information, see the description of each data package on the Commons.

1. **FLCAC Merged (beta)**

- USLCI: v1.2026-06.1
- US Electricity Baseline: v1.2026-06.0
- Forest and Forestry Products: v1.2026-04.2
- TRACI 2.2: v1.2025-04.0
- IPCC: v1.2024-12.0
- FEDEFL_INV: v1.2024-12.0


2. **FLCAC Merged with USEEIO (beta)**

- USLCI: v1.2026-06.1
- US Electricity Baseline: v1.2026-06.0
- Forest and Forestry Products: v1.2026-04.2
- USEEIO v2.0: v1.2022-06.0
- TRACI 2.2: v1.2025-04.0
- IPCC: v1.2024-12.0
- FEDEFL_INV: v1.2024-12.0

