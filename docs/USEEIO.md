---
title: Linking to USEEIO Background Data
description: Background, steps and resources to help users link to USEEIO processes
---

The USEEIO repository (repo) on the Federal LCA Commons (FLCAC) has a broad range of product flows that can be useful for filling gaps in LCI data. USEEIO reference flows are expressed in United States Dollars (USD). Using USEEIO flows will typically require a conversion from more common physical units (mass, volume, energy) to USD. 

## Pros of using USEEIO
* The full scope of the U.S. economy is reflected in the database. 
* LCIs in the USEEIO can be more comprehensive than a typical unit process based LCI approach given that supporting activities such as management, technical services, and real estate are included in the model scope by default.

## Cons of using USEEIO
* Price data can vary significantly from year to year and between sellers, introducing uncertainty in generated conversion factors.
* The entire economy is reflected in 411 commodity flows (in USEEIO v2), which may necessitate selecting a more aggregated commodity.

In a repo such as the USLCI, bridge processes are used to map source flows to target flows in the USEEIO. Use of a bridge process allows for a transparent conversion between physical units and USD. Bridge processes also allow us to maintain the source flow name, which can provide valuable context to other LCA practitioners especially in cases where the target USEEIO flow is not a perfect match for the source flow. 

Two tiers of flow correspondence may be required to link technosphere flows in the original OpenLCA database and USEEIO flows. It is recommended that both tiers of flow correspondence are documented in Excel prior to implementation in openLCA. The linked mapping template can be used. Once the flow correspondence is completed (in Excel) it will be necessary to import all necessary target flows into your working database as a flow needs to be present before it can be mapped to or used in a bridge process. 

The following guidance will help you to develop flow correspondence, map flows, and develop bridge processes and appropriate conversion factors to connect USLCI or other FLCAC resource to background data in the USEEIO.

# 1. Mapping to FLCAC flows
The first tier of flow correspondence is required if a technosphere flow is not currently available within the FLCAC (i.e., from another flow list). This correspondence will associate the original source flow and a product or CUTOFF flow in the USLCI or another repo on the FLCAC. This is an important housekeeping step as it will prevent the inclusion of duplicate flow names and UUIDs referring to a single product. If a bridge process will be created for a CUTOFF flow, the flow should be relocated to the appropriate NAICS folder. Once the flow correspondence is complete, the first tier of flow mapping should be carried out in OpenLCA: [Flow Mapping Instructions](https://flcac-admin.github.io/FLCAC-docs/flowmappinginstructions#mapping-a-dataset-within-openlca).

# 2. Bridging to USEEIO flows
The second tier of flow correspondence links the intermediate flow to a USEEIO flow via a [bridge process](https://flcac-admin.github.io/FLCAC-docs/bridge-processes). 
* When creating a bridge process, the target flow (with a matching UUID) from step 1 is set as the quantitative reference. 
* The bridge process name should be structured as follows:
    * ‘Name of material or process’ Bridge; ‘source repo’ to ‘target repo’
    * e.g. Citric Acid Bridge; USLCI to USEEIO
* The process description should include additional context on the material/process being bridged and information on the suggested provider(s) if relevant. 
* If the target USEEIO process is not a perfect match for the source flow, please add a ‘Proxy’ label to the developed bridge process. 
* The target flow in USEEIO is added to the new bridge process as an input. Target flows from USEEIO (with a matching UUID) will need to be exported from the most recent version of USEEIO available on the FLCAC. Do not manually recreate these flows based on name as the UUIDs will not match and will lead to duplicate flows. 
* To complete the bridge process, an exchange value needs to be developed to convert from physical units of the quantitative reference to USD in 2012 producer prices. Details on conversion factor development can be found in the section: {ref}`conv_heading`. 

:::{important}
To export flows, right click on an open copy of the target database, click ‘Export’, select ‘JSON-LD’, and use the folder tree to select the identified target flows. When identifying target flows in USLCI or USEEIO, it is important that you take note of the Target Flow Context as this information will be necessary when exporting flows from the target repos to be imported into your working database. A name-based search is not currently supported in the export feature, which is why it is necessary to know the Target Flow Context. Do NOT click the box to “Export default providers of product inputs and waste outputs” as this will lead to inclusion of unnecessary content in your working database. Only select flows that you intend to map to for less clutter.
:::

:::{admonition} Mapping example
A source database has a flow named ‘citric acid | citric acid production’. An exact name match for this flow is not present in the USLCI but a CUTOFF flow named ‘Citric Acid, at plant’ is available. Rather than including multiple citric acid flows in USLCI, the citric acid flow in the source database is first mapped to the USLCI CUTOFF flow. The CUTOFF flow is then moved to the appropriate NAICS folder and a bridge process is developed with ‘Citric Acid, at plant’ as the reference flow making a transparent connection to the selected USEEIO flow, named ‘Other basic organic chemicals’. 

In this example the bridge process is serving two functions. It will allow transparent documentation of the conversion between kilograms and USD. Second it will communicate to LCA practitioners that the broad category ‘Other basic organic chemicals’ is being used as a proxy for citric acid. If this flow ends up being an important contributor to life cycle impact assessment (LCIA) results, a more specific data source or sensitivity assessment is likely appropriate.
:::

(conv_heading)=
# Developing Conversion Factors to USD
Dollar values in USEEIO v2 are expressed in 2012 producer prices. However, cost data is not often readily available in producer prices. Equation {eq}`eq_1` can be used to convert purchaser price data to producer price data in the target year (2012 for USEEIO v2). Use of bulk, wholesale price data is a good source of purchaser price data that can be reliably converted to producer prices using sector specific matrix values. USEEIO includes available conversion factors to support the conversion of price types and dollar years. Rho matrix values reflect NAICS sector specific consumer price index (CPI) price year ratios that are used to convert current dollars to the model year (2012) of USEEIO version 2.0. Phi matrix values, reflecting producer-to-purchaser price ratios for the appropriate NAICS sector, are used to convert purchaser price data to producer prices to reflect the basis of USEEIO version 2.0. The necessary Rho and Phi matrix values can be found in recent versions of USEEIO models published by EPA, such as this one: [USEEIOv2.5-kinglet-22.xlsx](https://catalog.data.gov/dataset/useeio-v2-5-models/resource/ef9ad858-5d52-4f32-b408-8fb541ca56ae).

```{math}
:label: eq_1
\text{2012 Producer Price} = \text{Purchaser Price} × \frac{Rho_y}{Rho_{2012}} × Phi_{2012}
```

Purchaser price - United States Dollars per physical unit of the reference flow based on year y.<br>
Rho<sub>y</sub> – The CPI price year (Rho) matrix ratio for year y. Where year y corresponds to your price data.<br>
Rho<sub>2012</sub> – The CPI price year (Rho) matrix ratio for the 2012 model year used in USEEIO v2.<br>
Phi<sub>2012</sub> - The producer-to-purchaser price (Phi) matrix ratio for the 2012 model year.<br>


Conversion factors to U.S. Dollars are developed based on recent cost data in source flow units and should match the context of that flow. For example, if the source flow is 1 kg of citric acid as a 40% solution, the price data should reflect a 40% solution.  

It is recommended that the assumed NAICS sector code and associated Rho and Phi values be documented in the ‘data treatment’ metadata field. Please also document any necessary details of the conversion from physical units to USD and include sources, as appropriate. 
Example of documentation to be included in the ‘data treatment’ field for conversion of 1 m<sup>3</sup> building hall construction to construction of ‘other nonresidential structures’ in USEEIO:

:::{admonition} Example documentation text
Conversion to USD assumes purchaser price of $238 per ft<sup>2</sup>. One cubic meter of building volume is converted to square meters of floor area assuming the Average height of US industrial building = 36 feet or 10.97 meters.  1 cubic meter of building volume is approximately 1 square foot of floor area. Purchaser prices are in 2024 dollars. The 2023 Rho matrix values (most recent available), which reflect CPI price year ratios, for the appropriate NAICS sector are used to convert current 2024 dollars to the model year (2012) of USEEIO version 2.0. Phi matrix values, which reflect producer-to-purchaser price ratios, for the appropriate NAICS sector are used to convert purchaser price data to producer prices to reflect the basis of USEEIO version 2.0.

2012 Producer Price = 2024 purchaser price * (2023 Rho/2012 Rho) * 2012 Phi

Utilized ratios - NAICS code: 333120/US, 2023 Rho: 0.741, 2012 Rho: 1.076, 2012 Phi: 0.813
:::
