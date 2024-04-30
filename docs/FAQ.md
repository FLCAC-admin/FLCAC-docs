# Frequently Asked Questions
## Data Submission
<details>
 <summary><b>How do I submit data to the Federal LCA Commons (FLCAC)?</b></summary>

Submission processes vary for each repository, so it is recommended to reach out to the repository managers/owners to submit data or inquire about the specific data submission process. The USLCI submission process is currently recommended as the default FLCAC submission process. The submission handbook may be found [here](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/00-sub-handbook-landing.md) and a YouTube training video that covers this process is located [here](https://www.youtube.com/watch?v=jecyDLHu6OQ). The current FLCAC-Curation repository also includes various resources for preparing your data for the FLCAC. 

Here is a brief overview of the data preparation process: 
- Map elementary flows to FEDEFL
- Map technosphere flows to those that exist in the FLCAC repositories, or create new processes that produce the desired flows. Cut-off flows can also be created if needed, but these are not recommended.
- Import the data into openLCA, this can be done before or after the mapping process.
- Align the processes and flows with the NAICS folder structure.
- Complete the metadata for each process as described in the [USLCI metadata gudance tables](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#metadata-guidance-tables).
- Export the processes intended for submission and submit them to the repository owner/manager.
  - If you are the repository owner/manager then you will integrate the new processes into the existing database and push it to the collaboration server.

</details>

<details>
 <summary><b>How do I align my elementary flows with the Federal Elementary Flow List?</b></summary>

All data on the Federal LCA Commons must use elementary flows that conform to the [Federal Elementary Flow List](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=347251).
For instructions on mapping your flows, see [here](https://github.com/USEPA/fedelemflowlist/wiki/Getting-Started-with-FEDEFL#mapping-a-dataset)
</details>

<details>
 <summary><b>How do I align my technosphere flows the FLCAC?</b></summary>

Work in progress
</details>

<details>
 <summary><b>How do I align my dataset with the NAICS folder structure?</b></summary>

All data on the Federal LCA Commons must use the North American Industry Classification System (NAICS) folder structure [NAICS - Census Bureau](https://www.census.gov/naics/).
To align new or existing processes and flows with NAICS, import the [Commons Core database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) to add the NAICS folder structure to your openLCA database and then organize flows and processes into the relevant folders. Use the NAICS Census Bureau link above to determine the appropriate 4 digit NAICS code. 
</details>

<details>
 <summary><b>I have specific questions about data submission to the FLCAC, who do I reach out to?</b></summary>

Work in progress
</details>

## Using and Accessing Data
<details>
 <summary><b>How do I find impact assessment methods?</b></summary>

Impact assessment methods aligned with the Federal Elementary Flow List (FEDEFL) and Federal LCA Commons data are available in two forms:
- [LCIA Methods without flows](https://www.lcacommons.gov/lcia-methods-without-flows): These JSON-LD files do not contain the flow objects, only the characterization factors. They can be downloaded and imported into any openLCA database. The no flows versions of methods must be imported on top of a database that contains flows, otherwise the methods will not appear in the database.
- LCIA Methods repositories: Repositories are available for TRACI2.1 and ReCiPe which contain the methods and all relevant flow objects. These repositories are useful for reviewing all characterization factors for flows in the FEDEFL
</details>

<details>
 <summary><b>Why are the impact assessment methods that I imported into openLCA not showing up in my database?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What review process does data on the FLCAC undergo?</b></summary>

Work in progress
</details>

<details>
 <summary><b>How do I see what data exists on the FLCAC?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What is the FLCAC collaboration server?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What is a cut-off flow?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What is a library?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What is a provider?</b></summary>

Work in progress
</details>

<details>
 <summary><b>How do I use data from the FLCAC in openLCA?</b></summary>

Work in progress
</details>

<details>
 <summary><b>How do I use data from the FLCAC in other software?</b></summary>

Work in progress
</details>
