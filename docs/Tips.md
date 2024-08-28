---
title: Tips and Tricks
description: openLCA resources for reference
---

## Running Calculations on USLCI in openLCA

Use **_'As Defined in Process'_** as the Default Allocation Method

Using _NONE_ or _CAUSAL_ as the default allocation method, as designated by data providers in many USLCI multi-output processes, can produce unexpected LCI and LCIA results.
The _PHYSICAL_ and _ECONOMIC_ default methods produce expected results.
As such, you must select **_AS DEFINED IN PROCESS_**; when running calculations in openLCA in order to produce the correct results.

For more information, please see [this double-counting thread on allocation](https://ask.openlca.org/2281/allocation-in-multifunctional-processes) and this [unit properties in allocation thread](https://github.com/GreenDelta/olca-app/issues/83).
