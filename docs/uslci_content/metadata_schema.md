---
title: FLCAC Metadata Schema
description: ...
abbreviations:
    LCA: Life Cycle Assessment
    DOE: Department of Energy
    EPD: Environmental Product Declaration
    FEDEFL: Federal Elementary Flow List
    FLCAC: Federal LCA Commons
    ISO: International Organization for Standardization
---

:::{glossary}

## Process

term
: description
: example(s)

(M) Name<sup>[**[1]**](#fn1)</sup>
: Process name based on the [ILCD naming conventions](https://github.com/uslci-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-D.md#rule-12-general-flow-and-process-naming-rules);
Process name should reflect the product or service it represents; 
the product reference output (i.e., quantitative reference flow) is given the same name as the process name sans temporal or geographic references (i.e., those may be indicated by the provider process and/or in the quantitative reference flow metadata so that one quantitative reference flow may have several provider processes);
the naming conventions are as follows: 
<br><br>**Base name; treatment received, production route(s), standard(s) fulfilled; production or consumption type, location type; quantitative flow properties**<br><br>
The base name is a general descriptive name of the process using technical language.
The technical name should be given as it is used in the respective industry or toward their customers.
The standards include qualitative information about the process in technical terms (see Rules 12-17 [Appendix D: ILCD Nomenclature Rules](../04-resources/04-App-D.md) or the full [ILCD Handbook](http://eplca.jrc.ec.europa.eu/uploads/MANPROJ-PR-ILCD-Handbook-Nomenclature-and-other-conventions-first-edition-ISBN-fin-v1.0-E.pdf) for a list of potential descriptive terms). 
The quantitative process properties further specify information on process in technical quantitative term(s).<br><br>
Base name and treatment/routes/standards are mandatory
production/location type is mandatory if relevant to the process (if not, it can be ignored);
the location type of availability (LCAC) is designated only if the process is not a mix; if the process is a production or consumption mix, the mix type is indicated; finally, any essential quantitative properties of the product or process should be included.<br><br>
For consistent nomenclature, use the following guidelines:
  - separate components with a semi-colon
  - separate elements within a component with a comma
  - abbreviations and brackets should be avoided
  - chemical element symbols should be avoided (except in quantitative flow properties)
  - limit names to 220 characters

**Example with 3 components**<br>_Clinker; average mineral mix, at kiln, 1415 kg/m3_&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br><br>**Example with 3 components**<br>_Transport; long-haul truck, diesel powered; trip length > 200 mi_<br><br>**Example with 2 components**<br>_Scanner manufacture; Kodak Alaris i940 desktop manufacturing process_<br><br>
**Example with 3 components & output**<br>_Corn stover production; average, US, 2022; 15.5% moisture_<br>with quantitative reference flow:<br>_Corn stover production, 15.5% moisture_<br>

term
: description
: example(s)

## Allocation
<!-- from ./docs/uslci_content/allocation.md -->

term
: description
: example(s)

## Repository
<!-- from ./docs/uslci_content/admin-info.md -->

## Global Parameter
<!-- from ./docs/uslci_content/global-parameters.md -->

## Exchange Parameter
<!-- from ./docs/uslci_content/process-parameters.md -->

## Input Flows
<!-- from ./docs/uslci_content/inputs.md -->

## Output Flows
<!-- from ./docs/uslci_content/outputs.md -->

## Data Quality Assessment
<!-- from ./docs/uslci_content/modeling-and-validation.md -->

## Parameter
<!-- from ./docs/uslci_content/global-parameters.md -->

:::
