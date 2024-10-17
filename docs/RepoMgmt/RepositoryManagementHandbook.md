---
title: Repository Management Handbook
description: Information and instructions for FLCAC repository managers 
abbreviations:
  FLCAC: Federal LCA Commons
  LCA: Life Cycle Assessment
  LCI: Life Cycle Inventory
---

This is the Federal LCA Commons (FLCAC) Repository Management Handbook. It describes the repository management processes that repositories should strive to adhere to. Resources are provided for Repository Managers within this handbook.

<!-- - [Resources for data users are provided here](https://flcac-admin.github.io/FLCAC-docs/datauserhandbook). -->
- [Resources for data providers are provided here](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook).

# Data Submission
The data submission/curation process for each FLCAC repository can be decided upon by individual Repository Managers. The FLCAC Data Curator recommends following the guidance set forth in the [FLCAC Submission Handbook](datasubmissionhandbook). The [Data Formatting Section](datasubmissionhandbook#data-formatting) of this handbook must be followed for all new data submissions across the FLCAC. This includes the following:

1.	Categorization of processes and flows using the North American Industry Classification System (NAICS)
2.	Technosphere flow alignment with FLCAC product, waste, or cut-off flows
3.  Elementary flow alignment with the Federal Elementary Flow List (FEDEFL)
4.	Run LCIA results with new FEDEFL/FLCAC aligned model and compare to the original LCIA results
5.  Metadata conformance with the openLCA schema and the [FLCAC Metadata Guidance](metadataguidance) (includes data quality measurements)

:::{note}
These data formatting standards are not enforced retroactively.
:::

The FLCAC Data Curator will review all new data submissions for compliance with the data formatting steps above. 

Outside of the data formatting review, the Repository Manager can dictate the level of involvement of the FLCAC Data Curator throughout the data submission process. If desired, the FLCAC Data curator can help facilitate the entire data submission process with data providers for FLCAC Repository Managers. See the [Data Submission Steps](datasubmissiontoolkit#data-submission-steps) that the FLCAC Data Curator follows.

For new data submissions, the data provider should complete the [Data Provider Questionnaire](datasubmissiontoolkit#data-provider-questionnaire) and send this form to the Repository Manager and the FLCAC Data Curator.

:::{note}
Upcoming repository updates that are able to be publicly shared are listed on the [FLCAC Repositories](FLCAC_Repositories.md) page.
:::

# FLCAC Collaboration Server
The platform for the FLCAC is an openLCA collaboration server which is a server application that connects the openLCA desktop app and the FLCAC. The collaboration server allows users to work simutaneously on a database while tracking changes. Repository managers can prepare and publish data on the FLCAC via the collaboration server.
The collaboration server relies on basic Git commands.
For more details refer to the [Collaboration Server manual](https://greendelta.github.io/lca-collaboration-server-manual/chapter_3.html).

To connect to the FLCAC collaboration server, you must have login credentials. These credentials are provided to repository managers and designated data users and providers.

## Accessing a Repository on the FLCAC Collaboration Server

- Navigate to the repository of interest on the collaboration server and copy the URL, e.g., `https://www.lcacommons.gov/lca-collaboration/National_Renewable_Energy_Laboratory/USLCI_Database_Public`
- With all databases closed, select 'Import', select 'From Git...'. (Or right-click in the navigation pane and select 'Import from Git...')
- Paste the URL in the URL field (the following four fields will automatically populate)
- Enter your FLCAC collaboration server username and password
- Select ‘Connect’
- A list of commits will be displayed, select 'OK'
- Your database should now be connected to the FLCAC collaboration server. This connection is indicated by the url following the database name.

## Pushing and Pulling Data to and from the FLCAC Collaboration Server

Right click on the database connected to the FLCAC collaboration server, select ‘Repository’.
The following options are available:

- Commit: Record one or more changes to objects within the local repository
- Push: Submit one or more commits to the collaboration server repository
- Fetch: Retrieves changes that have been made in the remote collaboration server repository
- Pull: Updates local repository with changes
- Merge: Combines changes if there are both remote and local updates

:::{tip} FLCAC Collaboration Server Features
- Repositories are sorted under Groups (e.g., US Forest Service, NREL, FLCAC)
- Repository level metadata fields and release version metadata fields
- Release and versioning feature
- FLCAC and repository level commit log
- Repository level compare feature
:::
<!-- - # Repository-Level Metadata Guidance-->
