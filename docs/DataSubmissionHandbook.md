---
title: Data Provider Submission Handbook
description: Information and instructions for data providers submitting data to the FLCAC
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This is the Federal LCA Commons (FLCAC) Data Submission Handbook. It describes the data submission and documentation framework that all new data across the FLCAC repositories must adhere to. Resources are provided for data providers within this handbook.

- Resources for data users are provided here (LINK EVENTUALLY).
- Resources for repository owners are provided here (LINK EVENTUALLY).

# Introduction

The [FLCAC platform](https://www.lcacommons.gov/) provides users access to your data in LCA data formats and permits connectivity between your data and other LCA data resources.

The National Renewable Energy Lab (NREL) FLCAC Data Curators developed this comprehensive handbook to communicate the FLCAC’s streamlined, transparent, data provider-oriented submission and publication workflow. It additionally provides guidance for using the openLCA software within the context of preparing data for FLCAC submission.

The FLCAC data curation process is collaborative and iterative. Excluding technical review, the FLCAC Curators will review datasets to verify their compliance with the FLCAC Submission Handbook Guidelines, and coordinate with data providers to reconcile outstanding issues. Throughout this resource, additional opportunities for support from the FLCAC Data Curators during dataset preparation processes are clearly communicated.

The FLCAC consists of multiple, distinct LCI repositories covering a variety of topics, inventory collection methods, and dataset provider groups. One of the FLCAC repositories is the U.S. Life Cycle Inventory database (USLCI) which is managed by NREL and covers a wide breadth of LCI data from industry and . researchers. Federal agencies or their laboratories independently manage these repositories. A list of repositories and their management’s contact information can be found [here](https://flcac-admin.github.io/FLCAC-docs/flcac-repositories).

The FLCAC data handbook associated publication tools apply to all repositories on the FLCAC. This is a living document and will be updated as the FLCAC data submission process evolves. **This handbook applies to all new data submissions but is not enforced retroactively.**

The handbook is divided into two sections:

Section 1: _Should I publish data on the FLCAC?_

- Helps data providers decide if their data is a good fit for the FLCAC and provides an overview of the data submission process.

Section 2: _How do I publish data on the FLCAC?_

- Contains detailed guidance for publishing data on the FLCAC including data formatting, metadata approaches, and submission instructions.

If you have any questions, concerns, or recommendations, please contact us at: FederalLCACommons@erg.com.   



# Section 1: _Should I publish data on the FLCAC?_
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
