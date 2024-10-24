---
title: Data Submission Toolkit
description: An overview of the data submission process and relevant resources
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This document provides an overview of the data submission process and relevant resources.
Please refer to the [Data Submission Handbook](DataSubmissionHandbook.md) for detailed information regarding the submission process.
The [Frequently Asked Questions page](FAQ.md) includes more information about many of these topics.

## Data Submission Steps

1. Become familiar with the [Federal LCA Commons platform](https://www.lcacommons.gov/)
2. Contact the FLCAC data curators to set up an initial meeting to discuss your datasets intended for submission to the FLCAC
    - Prior to this meeting fill out the [data submission questionnaire](#data-provider-questionnaire) and submit it to the data curators at FederalLCACommons@erg.com
    - During this meeting we will discuss the specific steps needed to prepare your data for submission and assign roles
3. [Download the openLCA software](#openlca) and install it on your computer
4. Prepare and format your unit processes/product system as discussed in the initial curation meeting ([overview of the data formatting steps](#data-formatting-steps))
5. Export ONLY your prepared datasets as a zipped JSON-LD file & submit to the data curators or add the datasets to a repository directly through the collaboration server
6. Reconcile issues identified by the data curators during the review process & check results
7. Approve the final version
8. FLCAC data curators will publish your datasets on the FLCAC

## Data Formatting Steps

- Import your data into openLCA (import steps depend on original data source)
- Download and import the latest version of the repository that you will be submitting data to into your database
- [Flow map technosphere flows to existing FLCAC flows](DataSubmissionHandbook.md#technosphere-flow-alignment)
- [Flow map elementary flows to FEDEFL flows](DataSubmissionHandbook.md#elementary-flow-alignment)
- Download and import the [Federal LCA Commons Core database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) into your local database
- Move your processes and flows into the correct NAICS folders, you can search for the relevant folders on the [Census Bureau website here](https://www.census.gov/naics/)
- Delete the old, unused folders that were brought in with your original database
- [Run results](FAQ.md#openlca) and compare values to the original model
- Complete the metadata fields according to the [metadata guidelines](MetadataGuidance.md)
- Send your draft database to the FLCAC curators for review

:::{important} Notes on data submissions and maintenance of data

- The FLCAC data curators provide QA/QC checks on data submissions to ensure that they adhere to FLCAC standards.
- The FLCAC data curators **do not** review the originating LCA from which LCI data are generated.
- Background datasets in a {term}`product system` may be updated over time (e.g., the electricity grid will be updated to represent the most recent year of data available, if an incoming chemical production process is updated and linked to your product system this will be updated). As a result, **static LCIA results are not maintained over time.**
- The FLCAC data curators will make corrections to your data if errors arise. The curators will reach out to original dataset owners to notify them of changes.
:::

## Data Provider Questionnaire
Can be accessed [here](Data%20Provider%20Questionnaire.docx) in Microsoft Word format
| **Question**                                                                                                                                                                             | **Response** |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| **Describe the number and scope of the intended unit processes for submission.**                                                                                                     |              |
| **Describe the underlying source of the data. (Please share links or pdfs as appropriate)**                                                                                          |              |
| **What flow list is used for the elementary flows (e.g., ILCD, openLCA, SimaPro, etc)?**                                                                                             |              |
| **What impact assessment categories and/or inventory categories is the data representative of (e.g., global warming potential, eutrophication potential, water consumption, etc.)?** |              |
| **What format is the data currently in (e.g., SimaPro, excel, openLCA, etc.)?**                                                                                                      |              |
| **Will this data be submitted to part of an existing repository or will a new repository be needed?**                                                                                |              |
| **Are there any anticipated cross-repository dependencies (e.g., new processes will require data from the electricity baseline)?**                                                   |              |
| **What is the anticipated timing of submission and timing of curation support?**                                                                                                     |              |
| **Can we share publicly that you are working towards publishing this dataset on the FLCAC?**                                                                                         |              |
| **Is this effort in collaboration with or in support of a governmental agency? If so, will that agency require a review process for data submitted to the FLCAC?**                   |              |
| **Point of contact for submission** **(name and email).**                                                                                                                            |              |
| **Please provide any other details about level of curation support needed.**                                                                                                         |              |

## Technical Assistance Resources for Data Providers
### openLCA
:::{include} Reference/olca_resources.md
:::

### Submission Guidance

- [FLCAC Submission Handbook](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook): Submission handbook for USLCI and other FLCAC repositories. Section 2: How do I publish my data in USLCI? Provides technical details of the publishing process.
- [Metadata Guidance Tables](https://flcac-admin.github.io/FLCAC-docs/metadataguidance): These tables provide information on metadata that should be included in each openLCA field with examples.

:::{note}
It is preferred that data providers fill in their metadata directly in openLCA, but if needed an excel template can be provided to fill out metadata.
:::

- [YouTube Quick Help Series](https://www.youtube.com/playlist?list=PLmIn8Hncs7bFUOyXZNGXwG4LtdoTfLz6Q): Includes videos on how to work with repositories on the Federal LCA Commons, using USLCI as an example.

#### Video: USLCI Data Submission 📺 🔉
:::{iframe} https://www.youtube.com/embed/IlPlYet8llY
:width: 100%
Overview of the data submission process with an example dataset. Includes guidance on importing/exporting, aligning the folder structure with NAICS, flow mapping, completing metadata, and more.
:::
