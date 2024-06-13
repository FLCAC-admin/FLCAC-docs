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
- Complete the metadata for each process as described in the [USLCI metadata guidance tables](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#metadata-guidance-tables).
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

Technosphere flows (i.e., product or waste flows) that come from another database (e.g., ecoinvent, Agri-footprint, GaBi, etc.) must be mapped to technosphere flows that exist within the FLCAC repositories or new processes should be created that produce these flows. Cut-off flows may be created if neither of the previous options are possible. 

To map technosphere flows, you may either create a new process within openLCA and manually add the desired technosphere flows to your life cycle inventory (LCI) or you may use [openLCA's flow mapping function](https://www.openlca.org/flow-mapping-feature/) which allows you to apply mappings to your whole database.

</details>

<details>
 <summary><b>How do I align my dataset with the NAICS folder structure?</b></summary>

All data on the Federal LCA Commons must use the North American Industry Classification System (NAICS) folder structure [NAICS - Census Bureau](https://www.census.gov/naics/).
To align new or existing processes and flows with NAICS, import the [Commons Core database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) to add the NAICS folder structure to your openLCA database and then organize flows and processes into the relevant folders. Use the NAICS Census Bureau link above to determine the appropriate 4 digit NAICS code. 
</details>

<details>
 <summary><b>I have specific questions about data submission to the FLCAC, who do I reach out to?</b></summary>

Please submit questions to the FLCAC data curators via the [Issues page](https://github.com/FLCAC-admin/FLCAC-Curation/issues) or email us at FederalLCACommons@erg.com.
</details>

## Using and Accessing Data

### Federal LCA Commons (FLCAC)
<details>
 <summary><b>What is the Federal LCA Commons?</b></summary>
 
Official definition of the Federal LCA Commons (FLCAC) can be found on the [About Us](https://www.lcacommons.gov/about-us) page of the lcacommons.gov website.

The FLCAC is a collaborative project across several agencies of the U.S. federal government intended to make life cycle inventory (LCI) data available across agencies and to the general public. The FLCAC also looks to establish community resources and best practices for using and conducting life cycle assessments (LCA). 

- List of LCI and LCIA [repositories available on the FLCAC](https://www.lcacommons.gov/lca-collaboration/)
- Homepage for [FLCAC resources](https://github.com/FLCAC-admin/FLCAC-Curation)

</details>

<details>
 <summary><b>What is the FLCAC collaboration server?</b></summary>

Work in progress
</details>

### Data Review and Data Quality
<details>
 <summary><b>What review process does data on the FLCAC undergo?</b></summary>

Data posted to the FLCAC is subjected to the review process as described in process-level metadata. The FLCAC Data Curators do not perform an additional critical review of submitted data or check for ISO compliance. 

Currently, metadata fields are not consistently filled out within USLCI or all federal LCA or LCIA repositories on the FLCAC. Data users will need to assess the available metadata to ensure that utilized LCI datasets meet the data quality standards associated with their project scope. 

The FLCAC Data Curator is engaged in an ongoing task to assess data quality on the FLCAC and retroactively assign data quality scores that will help practitioners assess the sufficiency of a given dataset for their project.

Moving forward the FLCAC Data Curator will also work to ensure that metadata is consistently filled out for all new data submissions. At this time, there is no plan to retroactively update process metadata (aside from data quality scores) for data previously submitted to the FLCAC.

</details>

### Finding Data
<details>
 <summary><b>How do I see what data exists on the FLCAC?</b></summary>

Data on the FLCAC can be accessed via the [FLCAC website](https://lcacommons.gov), select "Browse repositories" on the landing page, select the repository of interest, and browse the elements included in that repository by opening folders. 

You can also search for processes across all repositories via the search function in the top right, filters are available to refine your search to specific repositories and elements of repositories. Data on the FLCAC can also be explored within openLCA by downloading the data from the FLCAC and importing them into an openLCA database. You can look through the elements in the navigation pane or the search function.
</details>

<details>
 <summary><b>How do I find impact assessment methods?</b></summary>

Impact assessment methods aligned with the Federal Elementary Flow List (FEDEFL) and Federal LCA Commons data are available in two forms:
- [LCIA Methods without flows](https://www.lcacommons.gov/lcia-methods-without-flows): These JSON-LD files do not contain the flow objects, only the characterization factors. They can be downloaded and imported into any openLCA database. The no flows versions of methods must be imported on top of a database that contains flows, otherwise the methods will not appear in the database.
- LCIA Methods repositories: Repositories are available for TRACI2.1 and ReCiPe which contain the methods and all relevant flow objects. These repositories are useful for reviewing all characterization factors for flows in the FEDEFL
</details>

### Life Cycle Impact Assessment (LCIA)

<details>

 <summary><b>What LCIA methods are currently harmonized for use with LCI data on the FLCAC?</b></summary>
The LCIA methods listed in the following table are currently available on the FLCAC and have been harmonized to align with the federal elementary flow list using the [LCIAformatter](https://github.com/USEPA/LCIAformatter)
<br></br>
TRACI version 2.2 is currently being harmonized for compatibility with FLCAC data. 
<br></br>

|LCIA Data|Provider|Link|
|---|---|---|
|TRACI 2.1|US Environmental Protection Agency|[Tool for Reduction and Assessment of Chemicals and Other Environmental Impacts](https://www.epa.gov/chemical-research/tool-reduction-and-assessment-chemicals-and-other-environmental-impacts-traci)|
|ReCiPe 2016 Midpoint|National Institute for Public Health and the Environment (The Netherlands)|[LCIA: the ReCiPe Model](https://www.rivm.nl/en/life-cycle-assessment-lca/recipe)|
|ReCiPe 2016 Endpoint|National Institute for Public Health and the Environment (The Netherlands)|[LCIA: the ReCiPe Model](https://www.rivm.nl/en/life-cycle-assessment-lca/recipe)|
|ImpactWorld+ Midpoint*|International Reference Center for Life Cycle of Products, Services and Systems (CIRAIG)|[ImpactWorld+](http://www.impactworldplus.org/en/team.php)|
|ImpactWorld+ Endpoint*|International Reference Center for Life Cycle of Products, Services and Systems (CIRAIG)|[ImpactWorld+](http://www.impactworldplus.org/en/team.php)|
|IPCC GWP|Intergovernmental Panel on Climate Change (IPCC)| |
|FEDEFL Inventory Methods|US Environmental Protection Agency|[FEDEFL Inventory Methods](https://github.com/USEPA/LCIAformatter/wiki/Inventory-Methods)|

Additional LCIA methods such as CML, Ecopoint, eco-indicator, EDIP2003, EPS, IMAGE 3, LIME, LUCAS, MEEup, ILCD and NAMEA are not currently available in a harmonized format. Flow mapping would be required to use these impact assessment methods with FLCAC data. <br></br>
 
</details>
<details>
 <summary><b>How do I get impact assessment results (e.g., climate change, eutrophication potential, etc.) for data on the FLCAC?</b></summary>

Work in progress
</details>

<details>
 <summary><b>Why are the impact assessment methods that I imported into openLCA not showing up in my database?</b></summary>

Work in progress
</details>

### LCA Software (OpenLCA is listed separately)

<details>
 <summary><b>How do I use data from the FLCAC in other software?</b></summary>

Work in progress
</details>

### OpenLCA

<details>
 <summary><b>How do I use data from the FLCAC in openLCA?</b></summary>

Download whole repositories or repository elements on the FLCAC as a JSON-LD file type (if prompted, select which version of openLCA you are working in, newer versions of openLCA are 2.0 and later). Then, open openLCA and create a new empty database and import the JSON-ld file into your database. **Link future video here.
</details>

<details>
 <summary><b>What is a library?</b></summary>

Work in progress
</details>

<details>
 <summary><b>What is a provider?</b></summary>

In openLCA, both elementary and technosphere flows exist independent of the processes inventories that use them. This means that multiple processes can produce, and therefore reference, a shared technosphere flow. Then, when the inputs of another process uses this technosphere flow, users can select which upstream (background) process dataset they want to assign as the 'provider' of that input. 

</details>



### LCA Terminology

<details>
 <summary><b>What is a cut-off flow?</b></summary>

A cut-off flow is a flow that is a placeholder or a dummy flow. These flows are used when no relevant flows in a database exists. It is not recommended to use these flows in your life cycle inventory if possible. In openLCA results, cut-off flows will appear in your inventory results, but will not contribute to impact category results.
</details>





