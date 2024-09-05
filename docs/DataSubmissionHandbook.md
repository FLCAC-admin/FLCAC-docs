---
title: Data Provider Submission Handbook
description: Information and instructions for data providers submitting data to the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This is the Federal LCA Commons (FLCAC) Data Submission Handbook. It describes the data submission and documentation framework that all new data across the FLCAC repositories must adhere to. Resources are provided for data providers within this handbook.

- [Resources for data users are provided here](https://flcac-admin.github.io/FLCAC-docs/datauserhandbook).
- [Resources for repository owners are provided here](https://flcac-admin.github.io/FLCAC-docs/repositorymanagementhandbook).

# Introduction

The [FLCAC platform](https://www.lcacommons.gov/) provides users access to your data in LCA data formats and permits connectivity between your data and other LCA data resources.

The National Renewable Energy Lab (NREL) FLCAC Data Curators developed this comprehensive handbook to communicate the FLCAC’s streamlined, transparent, data provider-oriented submission and publication workflow. It additionally provides guidance for using the openLCA software within the context of preparing data for FLCAC submission.

The FLCAC data curation process is collaborative and iterative. Excluding technical review, the FLCAC Curators will review datasets to verify their compliance with the FLCAC Submission Handbook Guidelines, and coordinate with data providers to reconcile outstanding issues. Throughout this resource, additional opportunities for support from the FLCAC Data Curators during dataset preparation processes are clearly communicated.

The FLCAC consists of multiple, distinct LCI repositories covering a variety of topics, inventory collection methods, and dataset provider groups. One of the FLCAC repositories is the U.S. Life Cycle Inventory database (USLCI) which is managed by NREL and covers a wide breadth of LCI data from industry and . researchers. Federal agencies or their laboratories independently manage these repositories. A list of repositories and their management’s contact information can be found [here](https://flcac-admin.github.io/FLCAC-docs/flcac-repositories).

The FLCAC data handbook associated publication tools apply to all repositories on the FLCAC. This is a living document and will be updated as the FLCAC data submission process evolves. **This handbook applies to all new data submissions but is not enforced retroactively.**

The handbook is divided into two sections:

Section 1: Should I publish data on the FLCAC?

- Helps data providers decide if their data is a good fit for the FLCAC and provides an overview of the data submission process.

Section 2: How do I publish data on the FLCAC?

- Contains detailed guidance for publishing data on the FLCAC including data formatting, metadata approaches, and submission instructions.

If you have any questions, concerns, or recommendations, please contact us at: FederalLCACommons@erg.com.   



# Section 1: Should I publish data on the FLCAC?
This section provides an explanation of the benefits, expectations, and general process for publishing data on the Federal LCA Commons (FLCAC). This Submission Overview is intended to help interested parties understand the benefits of publishing their data on the FLCAC and set reasonable expectations for the publication documentation and standards.

## Benefits

- The FLCAC repositories offer data providers with the opportunity to share complete, representative, and well-documented LCI data to a public repository.
- The FLCAC provides public, interoperable repositories that can be used separately or together to form complete product systems.
- The FLCAC gives users across the value chain access to transparent and representative LCI data alongside guidance for its intended use.

## Expectations
- The dataset should have a comprehensive LCI
- LCI data should represent a novel or enhancing contribution to the FLCAC
- LCI data should be non-proprietary (i.e., no ecoinvent processes)
- Data providers accept that their data will be publicly available if submitted to the FLCAC

:::{note}
:class: dropdown 
USLCI has a [Data Use Disclaimer Agreement (“Agreement”)](LINK EVENTUALLY) and [Data Provider’s Content License Agreement (“Agreement”)](LINK EVENTUALLY).
:::
- Data should undergo a review before submission to the FLCAC.
- Data should principally represent the US/North American geographical region

:::{note}
:class: dropdown 
If data are outside of this geographic scope, inquire with the FLCAC Curators on their appropriateness of inclusion to the FLCAC
:::
- Data providers will strive to submit unit processes in place of system processes

:::{note}
:class: dropdown 
System processes will only be accepted when data aggregation [e.g., horizontal averaging, vertical aggregation; proprietary, ease-of-use](2) is required from the data provider. See metadata guidance for instructions on documenting aggregation method.
:::
- Multifunctional unit processes should include all co-products and any associated allocation factors or displaced products.

:::{note}
:class: dropdown 
The allocation approach should be justified and clearly described.
:::
- If multiple, gate-to-gate unit processes for a product system are submitted, the linking between them should be explicit.
- Flow data within a unit process must be based on measurements using a specified and standardized measurement method OR estimated using methods and data described in specified in a publicly available source.

## Placing Your Data in the Public Domain
To support increased access to and sharing of resources, as well as to promote novel and innovative uses of LCA data, NREL requires that all datasets submitted to the LCA Commons be placed in the public domain under the terms of the [Creative Commons Legal Code (CC0 1.0 Universal (CC0 1.0))]( https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-C.md). By placing your datasets in the public domain, according to the CC0 1.0 license, you are removing “all of [your] rights to the work worldwide under copyright law, including all related and neighboring rights, to the extent allowed by law.” 

For USLCI data submissions, please review the legal code of the CC0 1.0 Universal license before submitting your datasets, as well as the [Data Use Disclaimer Agreement]( https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-A.md) and Data Provider’s Content License Agreement]( https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/04-resources/04-App-B.md).

Data Formatting Overview
To facilitate compliance with ISO 14048:2002, the FLCAC uses the openLCA database schema and builds upon this schema with additional requirements to standardize data across FLCAC repositories. There are four steps of data formatting to align data with the openLCA and FLCAC schemas:
1.	Categorization of processes and flows using the North American Industry Classification System (NAICS)
2.	Elementary flow alignment with the Federal Elementary Flow List (FEDEFL)
3.	Technosphere flow alignment with FLCAC product, waste, or cut-off flows
4.	Metadata conformance with the openLCA schema and metadata guidance provided in this handbook (includes data quality measurements)

Detailed information about these steps is provided in Section 2.

To minimize data formatting efforts and ensure all metadata elements persist throughout submission, datasets submitted to the LCA Commons should be edited in openLCA or in a format that is compatible with the latest version of openLCA. Editing guidance is provided in Section 2 of this handbook. 

EcoSpold (v1 and v2) and International Reference Life Cycle Data (ILCD) submissions generated by SimaPro, GaBi, ecoEditor, the ILCD editor, or any other editor may not support the required format and metadata fields, so datasets will need to be edited according to the guidelines provided in Section 2.

## Section 2: How do I publish my data in the USLCI?