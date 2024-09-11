---
title: Tips and Tricks
description: openLCA resources for reference
abbreviations:
  FLCAC: Federal LCA Commons
  LCIA: Life Cycle Impact Assessment Method
  NAICS: North American Industry Classification System
  EPD: Environmental Product Declaration
---
## Organizing a Database
- Processes and flows in FLCAC repositories are categorized by NAICS 2 and four digit NAICS codes. See [this section](https://flcac-admin.github.io/FLCAC-docs/datasubmissionhandbook#naics-categorization) for more information on Categorization.
- The [Commons Core Database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) contains an empty NAICS folder structure and the data quality matrices. This database can be combined with pre-existing or new openLCA databases to make organization easier.
- Drag and drop processes and flows into different folders in openLCA.
- New folders and subfolders can be created by right clicking on an existing folder and selecting "Add new child category".

## Import/Export LCI Data from Excel/openLCA
- It is possible to copy/paste to and from excel and a process inventory (i.e., the 'Inputs/Outputs tab of a process)
- Review [this section](https://greendelta.github.io/openLCA2-manual/cheat/import_export.html) of the openLCA manual

## Developing EPD Results in openLCA with FLCAC Data
- The openLCA EPD feature allows users to combine results representing different modules into an EPD structure.
- To use this feature, import relevant FLCAC repositories and a compatible LCIA method. Develop [module/stage processes](https://greendelta.github.io/openLCA2-manual/epds/create_processes_for_target_products.html) for the desired product (i.e., A1, A2, etc.). [Create product systems for each stage](https://greendelta.github.io/openLCA2-manual/epds/create_product_systems_from_processess.html), [run LCIA results](https://greendelta.github.io/openLCA2-manual/epds/calculate_impact_assessment.html), and then [save the results](https://greendelta.github.io/openLCA2-manual/epds/save_results.html). Lastly, [create a new EPD](https://greendelta.github.io/openLCA2-manual/epds/creating_epd_olca.html) and [add the module results](https://greendelta.github.io/openLCA2-manual/epds/adding_results_3rd_sources.html)

## Connect a Database to a GitHub Repository
To work collaboratively or share openLCA databases, you may connect a local database to a GitHub repository. 

**Follow these steps to connect an openLCA database to a GitHub Repository:**
- Create a new GitHub repository
:::{important}
This GitHub repository must be empty. It cannot contain a readme file or any other files.
:::
- Generate a GitHub Classic Token (Settings --> Developer Settings)
- Set the expiration (no expiration is recommended)
- Check the box to allow full control of private repos
- Save the token (it cannot be regenerated)
- Right click on the openLCA database that you would like to connect
- Select 'Repository', select 'Connect'
- Enter the following fields: 
  - URL = GitHub repository url
  - Username = GitHub username
- Your database should now be connected to your GitHub repository. This connection is indicated by the url following the database name.
- Password for pushing/pulling = token

**Pushing and Pulling Data To and From the a GitHub Repository**
- Right click on the database connected to a GitHub repository, select 'Repository'
- Functions:
  - Commit: Record of local changes to the repository
  - Push: Updates the collaboration server repository with local changes
  - Fetch: Record of changes that have been made
  - Merge: Combines changes if there are remote and local updates
  - Pull: Updates local repository with changes
