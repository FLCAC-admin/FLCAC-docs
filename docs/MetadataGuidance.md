---
title: Metadata Guidance
description: Detailed information on metadata fields for data on the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This document provides detailed information on metadata fields for data on the FLCAC. Each field in this document corresponds to a field in openLCA.

As FLCAC interagency coordination increases, the new standard for data formats and documentation is being advanced. To move toward interoperability and transparency, FLCAC harmonization of digital data access and preservation will increase collaboration potential and the reviewability of the LCA data exchange process. These efforts will significantly reduce not only data acquisition costs but also computer- and human-based misinterpretation errors, and thus, data misuse. As such, and to be more aligned with international protocols for all newly developed data, **the current FLCAC standard is to strive for 100% metadata completion**.

The sections in this document correspond to the tabs[^exclusions] and sections within the openLCA software.

- [General Information](#general-information)
- [Inputs/Outputs](#input-output)
- [Documentation](#documentation)
- [Allocation](#allocation)

:::{important}
Each field has a description and example(s) recommended by the Data Curator for completing the metadata for processes submitted to the FLCAC. Some of these fields are mandatory, a few are automatically populated, and some are optional - this is noted next to the field name.
:::

:::{note}
It is preferred that data providers fill in their metadata directly in openLCA, but if needed an excel template can be provided to fill out metadata.
:::

[^exclusions]: Three openLCA process tabs are not included in this guidance 'Parameters', 'Social aspects', and 'Direct impacts', data providers do not need to provide any information on these tabs. Please discuss the use of parameters with the Data Curator if your data submission includes parameters.

# General Information
![alt text](img/general_info.png)
## **Name** (_Mandatory_)

- Process names are based on the [ILCD naming conventions, Section 3.2](https://eplca.jrc.ec.europa.eu/uploads/MANPROJ-PR-ILCD-Handbook-Nomenclature-and-other-conventions-first-edition-ISBN-fin-v1.0-E.pdf)
- Process name should reflect the product or service it represents
- The product reference output (i.e., quantitative reference flow) is given the same name as the process name sans temporal or geographic references (i.e., those may be indicated by the provider process and/or in the quantitative reference flow metadata so that one quantitative reference flow may have several provider processes)

The naming conventions are as follows: 

**Base name[^mandatory]; treatment received[^mandatory], production route(s)[^mandatory], standard(s) fulfilled[^mandatory]; production or consumption type[^optional], location type[^optional]; quantitative flow properties**

[^mandatory]: Mandatory field
[^optional]: Mandatory field if relevant to the process. If not, it can be ignored.

For consistent nomenclature, use the following guidelines:
  - separate components with a semi-colon 
    - separate elements within a component with a comma
  - abbreviations and brackets should be avoided
  - chemical element symbols should be avoided (except in quantitative flow properties)
  - limit names to 220 characters

**Example(s)**
With 3 components: 
- _Clinker; average mineral mix; at kiln; 1415 kg/m3_
- _Transport; long-haul truck, diesel powered; trip length > 200 mi_
- _Corn stover production; average, US, 2022; 15.5% moisture_

With 2 components: 
- _Scanner manufacture; Kodak Alaris i940 desktop manufacturing process_

## **Category** _(Automatic)_

The category/subcategories schema follows North American Industry Classification System (NAICS). See the [Categorization section](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#naics-categorization) of the Data Submission Handbook for instructions on how to categorize flows and processes.

This field is automatically populated based on the folder that your process is located in.

**Example(s)**
- _22: Utilities/2211: Electric Power Generation, Transmission and Distribution_ 

- _31-33: Manufacturing/3253: Pesticide, Fertilizer, and Other Agricultural Chemical Manufacturing_

## **Description** _(Mandatory)_

A legible overview of the process description, i.e., technical scope, functional unit, system boundaries, and any other information needed for unambiguous data interpretation and application.

**Functional Unit**: Measure of the function of the studied system quantified to provides a reference to which the inputs and outputs can be related.

**Technical Scope**: Cradle-to-gate, cradle-to-grave, gate-to-gate, gate-to-grave.

**System boundaries**: Overview of included and excluded processes, i.e., boundaries between the technosphere and nature; geographic and temporal scope; boundaries between this and other technosphere systems. Detailed information on system boundaries can be provided in the [Sampling procedure](#sampling-procedure-mandatory) field.

:::{note}
Examples of included processes are: raw material acquisition; manufacturing/processing/refining; distribution/transport; production and use of fuels, electricity, and heat; use and maintenance of products; disposal of process waste and products; recovery of used products via reuse, recycling, and energy recovery; ancillary materials manufacturing; manufacture, installation, maintenance, and decommissioning of capital equipment; additional operations, such as lighting, heating, service personnel.
:::

**Other Relevant Information**: Include relevant modeling information regarding the inclusion of avoided products, co-products, cut-off flows, proxies, etc.


**Example(s)**
- _This gate-to-gate unit process is for the net production of one kilowatt-hour of electricity supply from a coal-fired plant with co-generation of steam in Four Corners Area, United States. The studied system includes all processes, from washed coal delivery through to power generation, including treatment of cooling water, of a combined heat and power plant with conventional steam cycle within a circulating fluidized bed.The fuel is 100% washed bituminous coal extracted from Rocky Mountain regional mines located within 500 km of the plant. Data are from one coal-powered base load plant so no aggregation was performed but is representative of typical coal-based power facility in that region._

- _The functional unit for this model is one kilogram of aniline. This aniline dataset includes nitrobenzene production and has been aggregated with incoming nitric acid LCI data. The technical scope includes the gate-to-gate production of nitric acid, nitrobenzene, and aniline. The system boundary includes incoming transport, manufacturing, and disposal of process wastes. The aniline dataset represented in this model includes data for nitric acid to conceal the confidential data of a provider company. Steam/heat is produced as a coproduct during this process, so system expansion is used for this recovered energy, which is shown as natural gas as an avoided product. Aniline is formed by the hydrogenation of nitrobenzene in the presence of a copper-chromium or copper-silica catalyst. The aniline producers who provided data for this module verified that the characteristics of their plants are representative of a majority of North American aniline production. The captured aniline production amount is approximately 71 percent of the aniline production in the U.S. in 2015._

## **Version** _(Automatic)_

Per ILCD, the data set version is formatted as follows: the first two digits indicate major updates, the second two digits refer to minor revisions and error corrections; the final three digits are used for automatic and internal version counting during dataset development.

 Unless discussed in advance with the Data Curator, the value will be generated automatically by openLCA
 
 **Example(s)**
 
 _01.00.000_|

## **Last change** _(Automatic)_

The date and time when the dataset was last saved.

**Example(s)**

_2018-04-01T17:38:55-0600_

## **UUID** _(Automatic)_

32-digit Universally Unique Identifier (UUID) for the dataset.[^UUID]

[^UUID]: Every element in an openLCA database has a UUID. UUIDs cannot be set, they are assigned by openLCA. [More details on UUID from the openLCA manual.](https://greendelta.github.io/olca-schema/classes/RefEntity.html?highlight=uuid#id)

**Example(s)**

_961fad56-bde2-4fbe-8895-5be03461729b_

## **Infrastructure** _(Mandatory)_

This is a box field in openLCA, checking the box indicates that the process includes infrastructure requirements in its inventory. Leave this box unchecked if infrastructure requirements are not included in the process.

**Example(s)**

![alt text](img/infra_unchecked.png)

![alt text](img/infra_checked.png)

## **Time** _(Mandatory)_

**Start Date**

Start date for the time period that the process data represents. The date format is MM/DD/YYYY.

**Example(s)**

_01/01/2017_

**End Date**

End date for the time period that the process data represents. The date format is MM/DD/YYYY.

**Example(s)**

_12/31/2017_

:::{important}
The Start and End Date fields should not represent publication dates, they should represent the time period for which the process data is representative of. 
:::
:::{note}
The time span is often the same as the foreground data collection period. If data has been gathered from secondary sources, reference those sources to find primary data collection dates and report the earliest and latest dates and discuss these methods in the description field below.
:::

**Description**

Provide information regarding the temporal characteristics and period that the process data represents. Information can also be provided pertaining to secondary data source time periods.

Examples can include explanation of the valid time period, any temporal aggregation, data collection period, seasonal/annual variations, and carbon provenance. 

:::{note}
The valid time span is often identical to the time of the data collection, unless projections or other forecasts have been applied. Limitations on the validity in valid time span can include future technology shifts, planned measurement improvements, or specific seasons.
:::

**Example(s)**

- _This unit process is representative of operations from 2014-2015. Water consumption varied seasonally but was averaged over an annual period._
- _This unit process is representative of aniline production from 2015-2016. Secondary data supporting the modeling are from 1990 and were adapted to represent updated nitric acid production. Companies providing primary data were given the option to collect data from the year preceding or following 2015 if either year would reflect more typical production conditions. One company provided data for the year 2015, and one company provided data for the year 2016. After reviewing individual company data in comparison to the average, each manufacturer verified data from 2015-2016 was representative of an average year for aniline production at their company._ 

## **Geography** _(Mandatory)_
**Location**

The geographic area to which the unit process data were collected or refer. If multiple locations were used, indicate the highest geographic location (e.g., if data for several states across the US were collected then enter 'US'). Describe the locations in the geography ‘Description’ field

**Example(s)**
- _US-CO_
- _RNA_ 

**Description**

Description of the process' geographic representativeness and any geographic aggregation methods as well as name(s) and production volume(s) or capacity of specific included site(s), where applicable. 

:::{note}
Any geographical information on where the process, inputs and/or outputs occur is useful for end-users in considering region-specific aspects such as average temperature, wind speeds, and precipitation levels, etc. that affect e.g., landfill decomposition, fate and transport of emissions, etc.
:::

**Example(s)**
- _This process is representative of production in the state of Colorado. Production data were aggregated across five sites ranging from eastern to western Colorado._
- _This unit process is representative of average aniline production in North America. Production data were collected from 2 leading producers in the United States and aggregated using horizontal averaging. The energy and emissions data for nitric acid production is from a primary European source from 1990 and was adapted to North American conditions._

## **Technology** _(Mandatory)_

A short (i.e., 1-3 paragraphs), general description of the process intended technical scope, representativeness, and applicability of the process. Include the following information (if applicable):

- Process design including sub-processes, unit operations, and/or other activities (anthropogenic or natural) included in the process
- Material selection and quality
- Operational conditions and representativeness
- A description of any waste and/or transport modeling


**Example(s)**
- _This process represents the production of "Calcium carbonate, ground, 20 microns, at plant" using average technologies for the United States from 2015-2016._ 

  _The process includes three sub-processes: Quarry Operations; Transport and Plant Processing. Quarry Operations includes the following unit operations: mechanical extraction; primary crushing; screening; and intermediate storage of calcium carbonate rock (marble, limestone, or chalk). Transport includes the transport of materials from Quarry Operations to Plant Processing via barge, train, or truck. Plant processing which includes jaw crushing, washing, impact crushing, ball milling to particle size, and then classifying. Material selection and quality represent industry averages from the contiguous United States. Operational conditions represent industry averages from the contiguous United States.Fate and transport modeling was not considered for this process._
- _The overall production technology is similar among all aniline plants that submitted data for this analysis. Aniline is formed by the hydrogenation of nitrobenzene in the presence of a copper-chromium or copper-silica catalyst. For hydrogenation of nitrobenzene, preheated hydrogen and nitrobenzene are fed into an evaporator, and aniline is formed by vapor phase catalytic reduction. The aniline is dehydrated to remove the water produced during the reaction. Pure aniline (99.95 wt. %) is obtained after a purification step in which the dehydrated aniline goes through a distillation process._

## **Data Quality**
### **Process Schema** _(Mandatory)_
#### Matrix
Use the US EPA - Process Pedigree Matrix, this matrix comes preloaded in many FLCAC repositories. This matrix can also be found in the [Commons Core Database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) which can be imported as a skeleton structure into any openLCA database.

#### Data Quality Entry
Once you have selected the US EPA - Process Pedigree Matrix, select '(not specified)' next to the 'Data quality entry' field and select the appropriate data quality scores for the 'Process Review' and 'Process Completeness' fields.

Please reference [EPA's Guidance on Data Quality Assessment for Life Cycle Inventory Data](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=321834) for information about the development of this matrix and guidance on how to complete it.

**Example(s)**

![alt text](img/process_DQ.png)

### **Flow Schema** _(Optional)_
:::{important}
While it is highly recommended to commplete flow level data quality for data submissions, it is currently not mandatory.
:::
#### Matrix
Use the US EPA - Flow Pedigree Matrix, this matrix comes preloaded in many FLCAC repositories. This matrix can also be found in the [Commons Core Database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) which can be imported as a skeleton structure into any openLCA database.

#### Data Quality Entry
Select the US EPA - FLow Pedigree Matrix on the 'General Information' tab and enter data quality scores for each exchange in the inventory on the 'Inputs/Outputs' tab.

Please reference [EPA's Guidance on Data Quality Assessment for Life Cycle Inventory Data](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=321834) for information about the development of this matrix and guidance on how to complete it.

Detail any assumptions used to assign these scores in the [Data treatment](#data-treatment) field.

**Example(s)**
- Select the matrix on the 'General Information' tab: 

![alt text](img/flow_DQ.png)

- Select data quality entries on the 'Inputs/Outputs' tab under the 'Data quality entry' column:

![alt text](img/flow_DQ_entry.png)

### **Social Schema** _(Optional)_
Currently, the FLCAC does not require social schema so no social schema data quality matrix is required.

# Input/Output

![alt text](img/inputs_outputs_tab.png)

## **Flow** (_Mandatory_)
Elementary Flows: Should only be from the [FEDEFL](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/elementary_flow_list/datasets) Read more about elementary flow alignment on the FLCAC [here](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#elementary-flow-alignment).

**Example(s)**
![alt text](img/elementary_flow_names.png)

:::{tip}
To ensure that elementary flows included in a process are FEDEFL flows, open up the flow information by doubleclicking a flow and check the description field. The description will include a statement such as this "From FedElemFlowList_1.0.1. Flow Class: Chemicals. Not a preferred flow." if it is a FEDEFL flow.
:::

Technosphere Flows: Should be newly created flows based on the [ILCD naming convention](#name-mandatory). Read about technosphere flow alignment on the FLCAC [here](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#technosphere-flow-alignment).

**Example(s)**
![alt text](img/tech_flow_names.png)

Quantitative Reference Flow: The quantitative reference flow is the designated output of a process. The quantitative reference flow is bolded and can be in the inputs or outputs section depending on the process type. A process must have a quantitative reference flow to be created.

**Example(s)**
![alt text](img/quant_ref.png)

## **Category** (_Automatic_)
Category is determined based on the folder that the flow is contained within. The FLCAC uses NAICS Categories to organize flows and processes, read about FLCAC Categorization [here](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#naics-categorization).

**Example(s)**
![alt text](img/elementary_flow_cats.png)
![alt text](img/tech_flow_cats.png)

:::{tip}
- Drag and drop flows and processes into different folders to change the flow category. 
- Create a new folder by right clicking an existing folder and selecting "Add a new child category". 
- The [Federal LCA Commons Core Database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) contains the skeleton NAICS structure, this can be imported into an existing openLCA database.
:::

## **Amount** (_Mandatory_)
Flow quantity

**Example(s)**
![alt text](img/elementary_flow_amt.png)

## **Unit** (_Mandatory_)
Flow unit; the openLCA software includes a set of unit groups and units. These units must be used to ensure proper data importation. 

:::{note}
If the pre-existing units in a database are not appropriate for one or more of your dataset flows, let the Data Curator know and they will assist in adding a unit to the list.
:::

**Example(s)**
![alt text](img/elementary_flow_unit.png)

## **Costs/Revenues** (_Optional_)
This field is provided for documenting life cycle costing (LCC) data. The currency and costs may be provided for each flow; the costs per unit are automatically generated based on this information and flow amount.

This field is not required and should be left blank if no life cycle costing data is available.

:::{note}
Most LCI data on the FLCAC does not include life cycle costing data.
:::

**Example(s)**
![alt text](img/tech_flow_costs.png)

## **Uncertainty** (_Optional_)
Describe flow's data uncertainty. The distribution type, mean, and standard deviation may be provided.

This information is not required, but if provided it increases the process' usefulness.

**Example(s)**
![alt text](img/tech_flow_unc.png)

## **Inputs: Avoided Waste** (_Optional_)
If there is a scrap or waste flow that is utilized in your process, the flow may be listed as an input to your dataset and marked as an avoided waste.

**Example(s)**

N/A

## **Outputs: Avoided product** (_Optional_)
Used to indicate allocation has been avoided in a multi-functional process. This box should only be checked for the by-product flow(s). For example, if a process produces steam and offsets natural gas, then natural gas would be entered as an output flow and the avoided product box would be checked. 

:::{important}
The provider should always be chosen if a flow is an avoided product.
:::

**Example(s)**
![alt text](img/avoided_prod.png)

## **Provider** (_Mandatory_)
For every non-cutoff technosphere flow, a provider must be selected. A provider connects the flow to an upstream process producing that flow. Every non-cutoff technosphere should have at least one provider option.

Read more about openLCA provider linkages in the openLCA manual [here](https://greendelta.github.io/openLCA2-manual/processes/process_tab_content.html).

:::{note}
Only non-cutoff technosphere flows have an upstream provider. Cutoff flows and elementary flows do not have providers as they are not being produced by a process.
:::

**Example(s)**
![alt text](img/tech_flows_provider.png)

## **Data quality entry** (_Optional_)
[See the flow data quality section](#flow-schema-optional).

This information is not required, but if provided it increases the usefulness of a process.

## **Location** (_Optional_)
Flow level location is an optional field but is useful to include if flow level exchange locations are known (i.e., where a flow was produced/originated from) and if they differ from the process location. 

:::{important}
To better support regionalized impact assessment, USLCI and FLCAC repositories will no longer allow locations on flow objects, but instead will utilize locations on exchanges and/or processes
:::

**Example(s)**
![alt text](img/tech_flow_locs.png)

:::{note}
In the example above, the location has not been entered for the first two technosphere flows. The reason for this is that the flow exchange location does not vary from the process location (US and RNA) in these instances, so a flow exchange location is not needed.
:::

## **Description** (_Optional_)
This field is required where applicable. Briefly describe the flow's relationship to the process and assumptions used to obtain the quantitative reference or data quality.

Types of information to include in the flow description field:

- Conversion factors
- Proxy/surrogate informatio (e.g., this flow is a proxy for the original flow "Natural gas combustion, RoW" from the ecoinvent database v2.1)
- Aggregation methods (e.g., two natural gas flows existed in the original study, these have been combined into one value)
- Stage of the LCI that a flow relates to (e.g., transportation from plant to warehouse)
- Other details about how the flow was transformed from the original study
- Pertinent information related to a specific flow that would impact the use of the data

**Example(s)**

![alt text](img/flow_descrip.png)

# Documentation
## LCI Method

### **Process type** (_Mandatory_)
Indication of whether the data represent a unit or system process.

<!-- :::{note}
[From the openLCA manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=quantitative#processes):

Unit process: A unit process is the smallest (least aggregated) unit in a production system, for which input and output data are quantified. It can contain any flow type.

System process: A system process is an aggregated life cycle result saved as a process.
::: -->

**Example(s)**

- {term}`_Unit process_`
- {term}`_System process_`

### **LCI method** (_Mandatory_)
Indicate whether the LCI method was attributional, consequential, input/output, hybrid, etc. Can include caveats regarding inclusion of the process in a product system.

**Example(s)**

- _Attributional process. Represents gate-to-gate data, use and end-of-life is dependent on how the product is used._
- _Consequential process_

### **Modeling constants** (_Mandatory_)
State the primary assumptions used to create this process. Detail how the process differs from the original source.

**Example(s)**

_This process was adapted from a Smith, 2016 process for wood pellet manufacturing for pellets of a specific energy value in Europe. The process weight factors were adapted for the energy density of a typical US biomass fuel._

## Data source information

### **Data completeness** (_Mandatory_)
This field is comprised of three elements:

1. Treatement of Missing Environmental Data:
List and describe accounting methods for missing environmental data (e.g., cut-off rules) and/or intentional environmental data omissions.

2. Treatment of Missing Technosphere Data:
List and describe accounting methods for missing technosphere data and/or intentional technosphere data omissions.

3. Mass Balance:
Either quantify and describe the mass imbalance ((mass of material outputs - mass of material inputs)/mass of material outputs) or state, "The mass balance for this process was not calculated."

**Example(s)**

_Elementary flows are cut-off at less than 1% based on environmental relevance. Technosphere flows are cut-off at less than 1% based on environmental relevance. The mass imbalance for this unit process is -17.87 kg (-0.72%)._

### **Data selection** (_Mandatory_)
Detail how data was selected for this process. If data was excluded, explain why.

**Example(s)**

- _Data was collected from 5 primary producers, one producer's data was not used because it was not representative of standard production practices._
- _Source 1 disaggregated waste inputs and listed heating values and emission factors for the incineration. Whereas, Source 2 had only heating values for waste flow inputs. Therefore, Source 2 waste heating values were excluded from the averages._

### **Data treatment** (_Mandatory_)
This field consists of two sections:

1. Detailed description of the methods and assumptions used to transform primary and secondary data into flow quantities through recalculating, reformatting, aggregation, or proxy data. 

:::{important}
The data documentor shall ensure that all data related to the relevant process in the unformatted document that are of environmental importance are adequately transferred and that no bias is generated. Justification and documentation shall be made regarding information that has been neglected or modified. 
:::

:::{note} Aggregation Types

Horizontal averaging combines data from processes serving the same function, e.g., via a production volume-weighted average.

Vertical averaging sums several interconnected processes to protect identification of the contribution of individual steps or entities, a.k.a., “gate-to-gate aggregation”.
:::

2. Describe any assumptions that were used when assigning [data quality](#data-quality) scores.

**Example(s)**

_A horizontally weighted average was calculated from the primary data collected from 4 producers. To indicate known emissions while protecting the confidentiality of individual company responses, some emissions are reported only by the order of magnitude of the average. Flow level data quality scores assume that the reference year is 2024._

### **Sampling procedure** (_Mandatory_)
This field is comprised of three elements:

1. System Boundary Conditions: A description of what is included and excluded from the system boundaries.

2. Data collection: A description of how data were collected for this process.

3. A description of if and how uncertainty was calculated for this process. If uncertainty was not calculated, this should be explicitly stated.

**Example(s)**

- _The system boundary is gate-to-gate and includes incoming transportation, direct emissions, material and energy use, as well as process waste management. The following are excluded from the system boundary: miscellaneous materials and additives, capital equipment, facilities and infrastructure, and support personnel requirements. Data were collected directly from 4 aniline manufacturers. Uncertainty was not calculated._
- _The system boundary includes: 1) the transport of raw materials to multiple manufacturing facilities where various subcomponents are produced; 2) the manufacture of subcomponents; 3) the transport of subcomponents to a different manufacturing plant for final assembly; 4) the assembly of subcomponents into a complete scanner; and 5) the transport of generated waste from the manufacturing facilities to a municipal solid waste landfill. The following processes and life cycle phases fall outside the system boundary: 1) packaging of the completed scanner; 2) all transport downstream of the assembly plant gate; 3) sale of product; 4) product use phase; and 5) end-of-life phase (including recycling)._

  _For material inputs, data collection was based on scanner specifications provided by the manufacturer. Other inputs (e.g. energy; waste transport and disposal) were calculated on the basis of quantity of input per kg of scanner produced._

  _Uncertainty was estimated based on engineering judgment. Material inputs had less uncertainty because they were based off of precise engineering specifications. Other inputs (e.g. energy; waste transport and disposal) had more uncertainty._

### **Data collection period** (_Optional_)
Include any additional information regarding data collection time period that was not covered in the [Time](#time-mandatory) field.

**Example(s)**

_All primary data were collected from 2015 to 2016. Secondary data were collected from 2005-2016 (NREL 2016; Wernet et al. 2016)._

### **Use advice**
Detail information that a data user needs to be aware of when using this process.

**Example(s)**

- _This process does not contain use or end-of-life stage because these vary based on the intended use of a product._
- _Cut-off flows were used for waste products which causes toxicity results to be underestimated by 20%._

<!-- ## Reviews

### **Review type**

**Example(s)**

### **Review report**

**Example(s)**

### **Review details**

**Example(s)**

### **Reviewers**

**Example(s)**

### **Review methods**

**Example(s)**

### **Quality assessment**

**Example(s)**

## **Compliance declarations**

**Example(s)**

## **Completeness**

**Example(s)**
-->
## **Sources**
Reference to the publication or entity from which data or methodology were obtained. 

Source title should use: “Author (YEAR) Abbreviated Title” format such that these information display in the openLCA navigation panel.

:::{tip}
To add a new source:
1. Open the 'Background data' folder in the openLCA navigation pane of database
2. Right click the 'Sources' folder and select 'New source'
3. Enter the metadata:
    - Name: "Author (YEAR) Abbreviated Title"
    - Description: Details about the source (if needed)
    - URL (if available)
    - Text reference: Full source title
    - Year
:::

**Example(s)**
![alt text](img/source.png)

<!-- ## Administrative Information

### **Project**

**Example(s)**

### **Intended Application**

**Example(s)**

### **Data set owner**

**Example(s)**

### **Data generator**

**Example(s)**

### **Data documentor**

**Example(s)**

### **Publication**

**Example(s)**

### **Creation date** _(Automatic)_

**Example(s)**

### **Copyright**

**Example(s)**

### **Access and use restrictions**

**Example(s)**
-->
# Allocation
## Physical
## Economic
## Causal
