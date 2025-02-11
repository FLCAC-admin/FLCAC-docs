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

Questions:
:::{dropdown} What is the scope of the U.S. Electricity Baseline?
The Electricity baseline accounts for LCI data by region for electricity generation at various points along the supply chain.
Users can select from electricity processes of four types:

- Electricity - <FUEL> - <Region>: LCI per MWh of electricity produced in this region for the selected fuel type.
- Electricity; at grid; generation mix - <Region>: LCI per MWh of electricity generated in this region across all fuel types.
- Electricity; at grid; consumption mix - <Region>: LCI per MWh of electricity consumed in this region, accounting for net trade from other regions.
- Electricity; at user; consumption mix - <Region>: LCI per MWh of electricity consumed in this region, accounting for losses from transmission and distribution.

The generation of electricity by fuel type accounts for the upstream supply of those fuels (e.g. natural gas, coal, nuclear, petroleum fuels).
:::

:::{dropdown} What is the source of the data for the generation emissions?
To be added
:::


:::{dropdown} What is the source of the data for upstream fuel supply LCI?
LCI data for fuel supply chains are included in the model as follows:

- GAS: Emissions from natural gas extraction and processing are sourced from XXX.
- OIL: Emissions from crude oil extraction, processing, and distribution of petroleum fuels are sourced from XXX.
- COAL: Emissions from the mining, processing, and transportation of coal are sourced from XXX.
- NUCLEAR: Emissions from the mining and processing of uranium for nuclear power plants are sourced from XXX.

:::

:::{dropdown} Is infrastructure included in the inventory?
For GAS, OIL, and COAL sources, LCI for power plant construction **ARE** included.
These data are calculated using USEPA's USEEIO model based on estimated power plant construction costs.

For SOLAR, SOLARTHERM.....

LCI from construction **ARE NOT** not currently included for HYDRO, NUCLEAR, .

Electricity transmission and distribution infrastructure is outside of the scope.
:::

:::{dropdown} Are transmission losses accounted for in the calculations?
Yes. Processes that are labeled as "at user" account for the transmission loss in that region, typically of around 5%.

:::

:::{dropdown} How do I determine which region to use?
A lookup of the appropriate balancing authority can be found at https://www.energy.gov/femp/balancing-authority-lookup-tool. 

:::

:::{dropdown} What impact categories/methods are intended to be used with the Electricity baseline?
To be added

:::

:::{dropdown} How do I access other years or older versions of the database?
Prior released versions on the FLCAC can be accessed using the repository dropdown.

NETL maintains additional data vintages in JSON-ld beyond the one hosted on the FLCAC.
These can be found at XXX.

:::

- What do the acronyms stand for? (OTHF and OSFL) -- other fuel and other fossil
- What does the 'Heat' flow mean? Heat from what?
- What does the 'Water, reclaimed' flow mean?
- Do cutoff flows exist? How are they indicated? -- yes, they exist, two are in the third party flows folder, others just exist in the flows' folders.
- How are errors in the database resolved?
- What's the difference between FERC and Balancing Authority regions?
- Can I make my own US average grid mix?
- Lots of questions about water, but hopefully these will be resolved soon!
