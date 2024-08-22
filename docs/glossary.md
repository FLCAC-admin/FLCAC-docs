---
title: Glossary
description: Glossary of terms and abbreviations used throughout the FLCAC
abbreviations:
    LCA: Life Cycle Assessment
    DOE: Department of Energy
    EPD: Environmental Product Declaration
    FEDEFL: Federal Elementary Flow List
    FLCAC: Federal LCA Commons
    ISO: International Organization for Standardization
---

:::{glossary}

collaboration server
: An openLCA specific server application, maintained by GreenDelta, that allows users to work collaboratively on LCA models, share data, and host public LCA repositories such as those available on [lcacommons.gov](https://www.lcacommons.gov/lca-collaboration/). For more information, see GreenDelta's Collaboration Server. 

context
: In the case of the FEDEFL (and often in LCA more broadly), context describes the origin or destination of an elementary flow. Context informs the directionality of an elementary flow. Resource flows are extracted from nature, while emissions are released to nature. [List of FEDEFL contexts](https://github.com/USEPA/Federal-LCA-Commons-Elementary-Flow-List/blob/master/wiki/resources/FEDEFLcontexts.xlsx). For more discussion of context see [EPA's FEDEFL Report](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=347251&Lab=NRMRL&simpleSearch=0&showCriteria=2&searchAll=elementary+flows&TIMSType=Published+Report&dateBeginPublishedPresented=07%2F31%2F2019)

cut-off flow
: a flow that is a placeholder or a dummy flow. These flows are used when no relevant flows in a database exists. It is not recommended to use these flows in your life cycle inventory if possible. In openLCA results, cut-off flows will appear in your inventory results, but will not contribute to impact category results.

<!-- [database](https://greendelta.github.io/openLCA2-manual/databases/) -->
<!-- : ... -->

[data package](https://datapackage.org/standard/data-package/)
: "A simple container format for describing a coherent collection of data in a single ‘package’. It provides the basis for convenient delivery, installation and management of datasets."

Disability-Adjusted Life Years (DALY)
: "One DALY represents the loss of the equivalent of one year of full health. DALYs for a disease or health condition are the sum of the years of life lost to due to premature mortality (YLLs) and the years lived with a disability (YLDs) due to prevalent cases of the disease or health condition in a population." from [World Health Organization](https://www.who.int/data/gho/indicator-metadata-registry/imr-details/158#:~:text=Definition%3A-,One%20DALY%20represents%20the%20loss%20of%20the%20equivalent%20of%20one,health%20condition%20in%20a%20population.)

elementary flow
: A material (resource), energy, or space that is exchanged with the biosphere. An elementary flow is characterized by a unique combination of {term}`flowable` and {term}`context` information and is assigned a {term}`UUID`.

endpoint indicator
: A category of LCIA indicator that expresses characterized impact in terms of damage caused to an area of concern such as the natural environment, human health or resource supply. An example of an endpoint indicator would be the human health impact of particulate matter formation potential expressed in {term}`Disability-Adjusted Life Years`.

Environmental Product Declaration
: A third-party verified report of the environmental impacts of a product. EPDs are developed according to ISO 14025 and the relevant 'product category rule' for that product type. For more information see the [FHWA EPD Tech Brief](https://www.fhwa.dot.gov/pavement/sustainability/hif21025.pdf)

FEDEFL
: see {term}`Federal Elementary Flow List`

[Federal Elementary Flow List](https://github.com/USEPA/fedelemflowlist)
: The Federal Elementary Flow List (FEDEFL) is a standardized list of {term}`elementary flow` names, developed by the U.S. Environmental Protection Agency, used in federal LCA work.

[Federal LCA Commons](https://lcacommons.gov/about-us)
: ...

[flow](https://greendelta.github.io/olca-schema/classes/Flow.html)
: ...

flowable
: A general term for the name of a material, energy or space that is exchanged with the biosphere. For more discussion of flowables see [EPA's FEDEFL Report](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=347251&Lab=NRMRL&simpleSearch=0&showCriteria=2&searchAll=elementary+flows&TIMSType=Published+Report&dateBeginPublishedPresented=07%2F31%2F2019)

functional unit
: The reference unit of a {term}`product system` within LCA. Results are run and compared on the {term}`functional unit`. [ISO 14040](https://www.iso.org/standard/37456.html)

[International Organization for Standardization](https://iso.org)
: An [independent, non-governmental body](www.iso.org/structure.html) with members from national standards boards that develops standard procedures for technical processes, such as life cycle assessment.

JSON-LD
: ...

Life Cycle Assessment
: [United Nations description of environmental LCA](https://lifecycleinitiative.org/starting-life-cycle-thinking/life-cycle-approaches/environmental-lca/)

library
: A type of data package limited to read-only access, intended to serve as a dependency of another data package. The library feature in openLCA 2.0 and later versions enables the use of databases together without the need to import them on top of one another. Processes and other elements that are part of a library database are not editable but can be utilized as part of processes or product systems in the main database.

midpoint indicator
: "A characterization method that provides indicators for comparison of environmental interventions at a level of cause-effect chain between emissions/resource consumption and the endpoint level." from the European Commission report [Indicators and targets for the reduction of the environmental impact of EU consumption: Overall environmental impact (resource) indicators](https://eplca.jrc.ec.europa.eu/uploads/JRC92824_qms_h08_lcind_deliverable3_final_20141113.pdf).  A common example of a midpoint indicator is global climate change potential where impacts are expressed as kg CO<sub>2 </sub>equivalents.

parquet
: ...

[process](https://greendelta.github.io/olca-schema/classes/Process.html)
: A set of related activities that convert inputs into output(s). A network of processes, the {term}`product system`, is used to define the life cycle of a product. Processes are characterized as {term}`unit process`es or {term}`system process`es. For more discussion of processes see [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)

Product Category Rule
: A collection of data source, scoping, and allocation rules for an {term}`Environmental Product Declaration`. "A set of specific rules, requirements and guidelines for developing Type Ill environmental declarations for one or more product categories." from[ISO 14025](https://www.iso.org/standard/38131.html). See also [EPA's Guidance for Product Category Rule Development](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=259406&Lab=NRMRL)

product flow
: These are all the flows that are not elementary or {term}`waste flow`s, and represent the materials or energy exchanged between processes within the {term}`product system`. [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/flows/index.html)

product system
: ...

provider
: A provider in openLCA is the upstream process that produces a flow. Providers can be chosen in the 'Inputs/Outputs' tab in openLCA under the 'Provider' column for product and waste flows.

[repository](https://greendelta.github.io/lca-collaboration-server-manual/chapter_3_4.html)
: A remote or local container in which data are stored under version control, from which a release of contained data can be published. The term repository is often applied to individual data releases (e.g. [USLCI](https://www.lcacommons.gov/lca-collaboration/National_Renewable_Energy_Laboratory/USLCI_Database_Public/datasets)) on the {term}`collaboration server` or individual GitHub sites (e.g. [FLCAC-Curation](https://github.com/FLCAC-admin/FLCAC-Curation).

resource flow
: A material or energy flow exiting the biosphere, which serves as an LCA process input.

system process
: "An aggregated life cycle result saved as a process." -from [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)

technosphere flow
: Intermediate product or service flows that serve as inputs to subsequent processes or comprise the functional unit of a {term}`product system`.

unit process
: "The  smallest (least aggregated) unit in a production system, for which input and output data are quantified." -from [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)

UUID
: Universally Unique Identifiers. Unrepeated alphanumeric code that points to specific database objects, typically within a JSON file. Within openLCA, UUIDs are assigned to processes, flows, {term}`product system`s, projects, parameters, impact categories and LCIA methods. Link to UUID search in the [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/introduction/index.html?search=UUID)

waste flow
: Waste flows are any substances or objects that the holder needs to dispose of, like by-products with no market value or those requiring more resources to recycle than their economic return. [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/flows/index.html)

:::
