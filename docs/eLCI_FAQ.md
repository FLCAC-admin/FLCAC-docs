---
title: Electricity Baseline Frequently Asked Questions
description: Frequently asked questions for the U.S. Electricity Baseline on the Federal LCA Commons
abbreviations:
    LCA: Life Cycle Assessment
    LCI: Life Cycle Inventory
    LCIA: Life Cycle Impact Assessment
    FLCAC: Federal LCA Commons
    USLCI: U.S. Life Cycle Inventory
    repo: repository
---

:::{dropdown} What is the scope of the U.S. Electricity Baseline?
The Electricity baseline accounts for LCI data by region for electricity generation at various points along the supply chain.
Users can select from electricity processes of multiple types:

- Electricity - FUEL - REGION: LCI per MWh of electricity produced in this region for the selected fuel type.
- Electricity; at grid; generation mix - REGION: LCI per MWh of electricity generated in this region across all fuel types.
- Electricity; at grid; consumption mix - REGION: LCI per MWh of electricity consumed in this region, accounting for net trade with other regions.
- Electricity; at user; consumption mix - REGION: LCI per MWh of electricity consumed in this region, accounting for losses from transmission and distribution.

As of June 2026 (v1.2026-06.0), the electricity baseline also includes residual mixes.
These processes remove generation from sources associated with Renewable Energy Credits (e.g., the quantity of solar in the generation or consumption mix will be lower):

- Electricity; at grid; _residual_ generation mix - REGION
- Electricity; at grid; _residual_ consumption mix - REGION
- Electricity; at user; _residual_ consumption mix - REGION


The generation of electricity by fuel type accounts for the upstream supply of those fuels (e.g. natural gas, coal, nuclear, petroleum fuels).
:::


:::{dropdown} What is a residual mix and how is it calculated?

In a residual mix, the electricity from renewable sources which is claimed via other mechanisms (e.g., Renewable Energy Credits) is removed from the available mix.

The data used to estimate the residual mix is from  E. O'Shaughnessy, S. Jena, and D. Salyer. 2024. Status and Trends in the Voluntary Market (2023 Data). Golden, CO: NLR. https://doi.org/10.2172/2584242 and [associated workbook](https://www.nlr.gov/docs/libraries/analysis/nrel-green-power-data-v2023.xlsx?sfvrsn=5775598f_2).
:::


:::{dropdown} When to use the residual electricity mix?

If your product system includes a unit process representing a faciility that does not purchase renewable energy credits (REC) or have a power purchase agreement (PPA), a residual mix should be chosen as the Exchange.defaultProvider for consumed electricity input(s) on that process.
:::

:::{dropdown} What is the difference in results between the residual and normal consumption mixes?

Most impact categories have higher impact category results in the residual mix due to fewer renewable sources. View the difference in US avg and FERC region results [here](https://github.com/FLCAC-admin/FLCAC-docs/tree/main/docs/results/elci_diffs.md).
:::

<!--
:::{dropdown} What is the source of the data for the generation emissions?
To be added
:::
-->

:::{dropdown} What is the source of the data for upstream fuel supply LCI?
LCI data for fuel supply chains are included in the model as follows:

- GAS: Emissions from natural gas extraction and processing are sourced from [Life Cycle Analysis of Natural Gas Extraction and Power Generation](https://netl.doe.gov/energy-analysis/details?id=3198).
- OIL: Emissions from crude oil extraction, processing, and distribution of petroleum fuels are sourced from updated modeling based on that described in [Updating the U.S. Life Cycle GHG Petroleum Baseline to 2014 with Projections to 2040 Using Open-Source Engineering-Based Models](http://dx.doi.org/10.1021/acs.est.6b02819).
- COAL: Emissions from the mining, processing, and transportation of coal are sourced from [Cradle-to-Gate Life Cycle Analysis Baseline for United States Coal Mining and Delivery](https://doi.org/10.2172/2370100).
- NUCLEAR: Emissions from the mining and processing of uranium for nuclear power plants are sourced from [Role of Alternative Energy Sources: Nuclear Technology Assessment](https://netl.doe.gov/energy-analysis/details?id=620).

Additional details for each are included in the process metadata and the associated reports.

:::

:::{dropdown} Is infrastructure included in the inventory?
For GAS, OIL, and COAL sources, LCI for power plant construction **ARE** included.
These data are calculated using USEPA's USEEIO model based on estimated power plant construction costs.
Similarly, emissions for plant construction for SOLAR PV, SOLAR THERMAL, and WIND are calculated from publicly available reports and datasets.
Plant constructiion for GEOTHERMAL is included in the utility inventory, and not tracked in a separate unit process.
LCI from infrastructure for all other sources **ARE NOT** included at this time.

Electricity transmission and distribution infrastructure is outside of the scope.
:::

:::{dropdown} Are transmission losses accounted for in the calculations?
Yes. Processes that are labeled as "at user" account for the transmission loss in that region, typically of around 5%.

:::

:::{dropdown} How do I determine which region to use?
A lookup of the appropriate balancing authority can be found at https://www.energy.gov/femp/balancing-authority-lookup-tool. Federal Energy Regulatory Commission (FERC) and US average regions are also available. Balancing authorities are aggregated into FERC regions which are aggregated into a US average.

:::

:::{dropdown} What impact categories/methods are intended to be used with the Electricity baseline?
The Electricity baseline is aligned with the {term}`Federal Elementary Flow List`.
As such, all [FEDEFL compatible methods](LCIAmethods.md) can be used, including inventory methods for water and energy resources.

:::

:::{dropdown} How do I access other years or older versions of the database?
Prior released versions on the FLCAC can be accessed using the repository dropdown.

NETL maintains additional data vintages in JSON-ld beyond the one hosted on the FLCAC, linked here for your convenience.
Note that there may be minor differences between published JSON-ld files and data that are published on the FLCAC.
- 2020: https://edx.netl.doe.gov/dataset/electricity-baseline-2020
- 2021: https://edx.netl.doe.gov/dataset/electricity-baseline-2021
- 2022: https://edx.netl.doe.gov/dataset/electricity-baseline-2022

:::

<!--
- What do the acronyms stand for? (OTHF and OSFL) -- other fuel and other fossil
- What does the 'Heat' flow mean? Heat from what?
- What does the 'Water, reclaimed' flow mean?
- Do cutoff flows exist? How are they indicated? -- yes, they exist, two are in the third party flows folder, others just exist in the flows' folders.
- How are errors in the database resolved?
- What's the difference between FERC and Balancing Authority regions?
- Can I make my own US average grid mix?
- Lots of questions about water, but hopefully these will be resolved soon!

-->
