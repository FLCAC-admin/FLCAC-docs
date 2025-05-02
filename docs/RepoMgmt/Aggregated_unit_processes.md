---
title: Aggregated Unit Processes
description: Guidance on developing aggregated unit processes as background data
abbreviations:
  FLCAC: Federal LCA Commons
---

In LCA modeling, it can be common for practitioners to build highly resolved and parameterized models.
These models may allow the generation of LCA results that are spatially explicity (i.e., regionalized) or that reflect specific scenario modeling, often through the use of global parameters.
However the use of parameters in LCA models can be cumbersome when they are intended as background or secondary data.
This document describes an approach for generating **aggregated unit processes** in openLCA for use as background data from complex models.
These unit processes are similar to {term}`system processes <system process>`, except they maintain transparent links to background data.

## Approach

1. Generate a product system of your model that is appropriately parameterized for your scenario.
2. Using the openLCA model graph, remove links to background data that are unparameterized. All processes that are impacted by the selection of a global parameter value must remain in the product system - these are the unit processes that will be aggregated.
3. Generate inventory results for this product system.
4. Save those results "As a system process" in openLCA. This will create a new process in openLCA that should have a number of input and output flows. Any technosphere flows that were unlinked in the step above will be maintained as technosphere flows without default providers.
5. For metadata purposes, this process can be indicated as a "Unit Process" in the [process type field](../MetadataGuidance.md#process-type-mandatory).
6. In this new aggregated unit process, apply default providers for any technosphere flows that remain.
7. Repeat this process as needed for other scenarios.

In the diagram below, processes A through E reflect core or novel modeling performed in an LCA model.
Processes A, B, C, and D are parameterized using a global parameter to reflect specific scenarios or regions.
Process E is not impacted by the global parameter.
Processes F and G represent background data (e.g., fuels, materials, or transport which are not core data), which may not be included in the final repository.

![text](../img/aggregated_up1.png)

To create the aggregated unit process, all links are removed to processes which will not be aggregated (and which are not impacted by the global parameter).
Results are run for the resulting product system and they are "Saved as System Process".

![text](../img/aggregated_up2.png)

## Limitations

- Aggregated unit processes will not maintain any uncertainty information from the original model.
- Metadata will need to be re-compiled for the aggregated unit process.
- Aggregated unit processes are not intended to reproduce reported results. For example, background data may be updated.

## Examples

- NETL Coal model
