---
title: Process Metadata Guidance
description: Detailed information on metadata fields for data on the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This document provides detailed information on metadata fields for data on the FLCAC. Each field in this document corresponds to a field in openLCA.

As FLCAC interagency coordination increases, the new standard for data formats and documentation is being advanced. To move toward interoperability and transparency, FLCAC harmonization of digital data access and preservation will increase collaboration potential and the reviewability of the LCA data exchange process. These efforts will significantly reduce not only data acquisition costs but also computer- and human-based misinterpretation errors, and thus, data misuse. As such, and to be more aligned with international protocols for all newly developed data, **the current FLCAC standard is to strive for 100% metadata completion**.

The sections in this document correspond to the tabs and sections within the openLCA software.

:::{important}
Each field has a description and example(s) recommended by the Data Curator for completing the metadata for processes submitted to the FLCAC. Some of these fields are mandatory, a few are automatically populated, and some are optional - this is noted next to the field name.
:::

:::{note}
It is preferred that data providers fill in their metadata directly in openLCA, but if needed an excel template can be provided to fill out metadata.
:::

# General Information
![alt text](image-4.png)
## **Name** (_Mandatory_)
### Description
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

### Example(s)
With 3 components: 
- _Clinker; average mineral mix; at kiln; 1415 kg/m3_
- _Transport; long-haul truck, diesel powered; trip length > 200 mi_
- _Corn stover production; average, US, 2022; 15.5% moisture_

With 2 components: 
- _Scanner manufacture; Kodak Alaris i940 desktop manufacturing process_

## **Category** _(Automatic)_
### Description
The category/subcategories schema follows North American Industry Classification System (NAICS). See the [Categorization section](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#naics-categorization) of the Data Submission Handbook for instructions on how to categorize flows and processes.

This field is automatically populated based on the folder that your process is located in.

### Example(s)
- _22: Utilities/2211: Electric Power Generation, Transmission and Distribution_ 

- _31-33: Manufacturing/3253: Pesticide, Fertilizer, and Other Agricultural Chemical Manufacturing_

## **Description** _(Mandatory)_
### Description
A legible overview of the process description, i.e., technical scope, functional unit, system boundaries, and any other information needed for unambiguous data interpretation and application.

**Functional Unit**: Measure of the function of the studied system quantified to provides a reference to which the inputs and outputs can be related.

**Technical Scope**: Cradle-to-gate, cradle-to-grave, gate-to-gate, gate-to-grave.

**System boundaries**: Included and excluded processes, i.e., boundaries between the technosphere and nature; geographic and temporal scope; boundaries between this and other technosphere systems.

:::{note}
Examples of included processes are: raw material acquisition; manufacturing/processing/refining; distribution/transport; production and use of fuels, electricity, and heat; use and maintenance of products; disposal of process waste and products; recovery of used products via reuse, recycling, and energy recovery; ancillary materials manufacturing; manufacture, installation, maintenance, and decommissioning of capital equipment; additional operations, such as lighting, heating, service personnel.
:::

**Other Relevant Information**: Include relevant modeling information regarding the inclusion of avoided products, co-products, cut-off flows, proxies, etc.


### Example(s)
- _This gate-to-gate unit process is for the net production of one kilowatt-hour of electricity supply from a coal-fired plant with co-generation of steam in Four Corners Area, United States. The studied system includes all processes, from washed coal delivery through to power generation, including treatment of cooling water, of a combined heat and power plant with conventional steam cycle within a circulating fluidized bed.The fuel is 100% washed bituminous coal extracted from Rocky Mountain regional mines located within 500 km of the plant. Data are from one coal-powered base load plant so no aggregation was performed but is representative of typical coal-based power facility in that region._

- _The functional unit for this model is one kilogram of aniline. This aniline dataset includes nitrobenzene production and has been aggregated with incoming nitric acid LCI data. The technical scope includes the gate-to-gate production of nitric acid, nitrobenzene, and aniline. The system boundary includes incoming transport, manufacturing, and disposal of process wastes. The aniline dataset represented in this model includes data for nitric acid to conceal the confidential data of a provider company. Steam/heat is produced as a coproduct during this process, so system expansion is used for this recovered energy, which is shown as natural gas as an avoided product. Aniline is formed by the hydrogenation of nitrobenzene in the presence of a copper-chromium or copper-silica catalyst. The aniline producers who provided data for this module verified that the characteristics of their plants are representative of a majority of North American aniline production. The captured aniline production amount is approximately 71 percent of the aniline production in the U.S. in 2015._

## **Version** _(Automatic)_
### Description
Per ILCD, the data set version is formatted as follows: the first two digits indicate major updates, the second two digits refer to minor revisions and error corrections; the final three digits are used for automatic and internal version counting during dataset development.

 Unless discussed in advance with the Data Curator, the value will be generated automatically by openLCA
 
 ### Example(s)
 _01.00.000_|

## **Last change** _(Automatic)_
### Description
The date and time when the dataset was last saved.

### Example(s)
_2018-04-01T17:38:55-0600_

## **UUID** _(Automatic)_
### Description
32-digit Universally Unique Identifier (UUID) for the dataset. Every element in an openLCA database has a UUID. UUIDs cannot be set, they are assigned by openLCA.

### Example(s)
_961fad56-bde2-4fbe-8895-5be03461729b_

## **Infrastructure** _(Mandatory)_
### Description
This is a box field in openLCA, checking the box indicates that the process includes infrastructure requirements in its inventory. Leave this box unchecked if infrastructure requirements are not included in the process.

### Example(s)
![alt text](image-2.png)

![alt text](image-3.png)

## **Time** _Mandatory_

### **Start Date** 
#### Description
Start date for the time period that the process data represents. The date format is MM/DD/YYYY.

#### Example(s)
_01/01/2017_

### **End Date**
#### Description
End date for the time period that the process data represents. The date format is MM/DD/YYYY.
#### Example(s)
_12/31/2017_

:::{important}
The Start and End Date fields should not represent publication dates, they should represent the time period for which the process data is representative of. 
:::
:::{note}
The time span is often the same as the foreground data collection period. If data has been gathered from secondary sources, reference those sources to find primary data collection dates and report the earliest and latest dates and discuss these methods in the description field below.
:::

### **Description**
#### Description
Provide information regarding the temporal characteristics and period that the process data represents. Information can also be provided pertaining to secondary data source time periods.

Examples can include explanation of the valid time period, any temporal aggregation, data collection period, seasonal/annual variations, and carbon provenance. 

:::{note}
The valid time span is often identical to the time of the data collection, unless projections or other forecasts have been applied. Limitations on the validity in valid time span can include future technology shifts, planned measurement improvements, or specific seasons.
:::

#### Example(s)
- _This unit process is representative of operations from 2014-2015. Water consumption varied seasonally but was averaged over an annual period._
- _This unit process is representative of aniline production from 2015-2016. Secondary data supporting the modeling are from 1990 and were adapted to represent updated nitric acid production. Companies providing primary data were given the option to collect data from the year preceding or following 2015 if either year would reflect more typical production conditions. One company provided data for the year 2015, and one company provided data for the year 2016. After reviewing individual company data in comparison to the average, each manufacturer verified data from 2015-2016 was representative of an average year for aniline production at their company._ 

## Data Quality Assessment


# Input/Output Flows

## Input Flows


## Output Flows

# Documentation

# Allocation

# Parameters

## Global Parameters

## Process Parameters