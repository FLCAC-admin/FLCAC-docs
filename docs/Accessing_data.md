---
title: Accessing FLCAC Data
description: Information on how to access and use data on the Federal LCA Commons
abbreviations:
  FLCAC: Federal LCA Commons
---

## Downloading data

Download whole {term}`repositories <repository>` or repository elements (e.g., {term}`processes <process>` and {term}`flows <flow>`) on the FLCAC as a {term}`JSON-LD` file type.
If prompted, select which version of openLCA you are working in; newer versions of openLCA are 2.0 and later.

:::{important}
Do not unzip the file that is downloaded from the FLCAC!
:::

In openLCA, right click on a pre-existing database or create a new, empty database. Select _import_, select _file_, and navigate to the downloaded JSON-LD file in your file explorer.

See the ['Importing and Combining Database' section of the openLCA manual](https://app.sli.do/event/gYHq4CGtMRhbo1JJmemfvc) for more information.

:::{iframe} https://www.youtube.com/embed/YLao5jC5b_0
Video 3: Importing the USLCI into openLCA
:::

## Connecting a Database Directly to the FLCAC Collaboration Server

The platform for the FLCAC is an openLCA collaboration server which is a server application that connects the openLCA desktop app and the FLCAC. The collaboration server allows users to work simutaneously on a database while tracking changes. Repository managers can prepare and publish data on the FLCAC via the collaboration server.

To connect to the FLCAC collaboration server, you must have login credentials. These credentials are provided to repository managers and designated data users and providers.

**Follow these steps to connect an openLCA database to the FLCAC collaboration server:**
- Navigate to the repository of interest on the collaboration server and copy the URL
- Create a new, empty database in openLCA
- Right click on the database, select 'Repository', select 'Connect'
- Paste the URL in the URL field (the following four fields will automatically populate)
- Enter your FLCAC collaboration server username
- Select 'Connect'
- Enter your FLCAC collaboration server Password
- Your database should now be connected to the FLCAC collaboration server. This connection is indicated by the url following the database name.

**Pushing and Pulling Data To and From the FLCAC Collaboration Server:**
- Right click on the database connected to the FLCAC collaboration server, select 'Repository'
- Functions:
  - Commit: Record of local changes to the repository
  - Push: Updates the collaboration server repository with local changes
  - Fetch: Record of changes that have been made
  - Merge: Combines changes if there are remote and local updates
  - Pull: Updates local repository with changes

**FLCAC Collaboration Server Features:**
- Repositories are sorted under Groups (e.g., US Forest Service, NREL, FLCAC)
- Repository level metadata fields and release version metadata fields
- Release feature
- Commit log 
- Change log 


## Connect a Database to a GitHub Repository
To work collaboratively or share openLCA databases, you may connect a local database to a GitHub repository. 

**Follow these steps to connect an openLCA database to a GitHub Repository:**
- Create a new GitHub repository
  - **This GitHub repository must be empty.** It cannot contain a readme file or any other files.
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