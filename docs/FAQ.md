# Frequently Asked Questions

<details>
 <summary><b>How do I align my dataset with the Federal Elementary Flow List?</b></summary>

All data on the Federal LCA Commons must use elementary flows that conform to the [Federal Elementary Flow List](https://cfpub.epa.gov/si/si_public_record_report.cfm?Lab=NRMRL&dirEntryId=347251).
For instructions on mapping your flows, see [here](https://github.com/USEPA/fedelemflowlist/wiki/Getting-Started-with-FEDEFL#mapping-a-dataset)
</details>

<details>
 <summary><b>How do I find Impact Assessment Methods?</b></summary>

Impact assessment methods aligned with the Federal Elementary Flow List (FEDEFL) and Federal LCA Commons data are available in two forms:
- [LCIA Methods without flows](https://www.lcacommons.gov/lcia-methods-without-flows): These JSON-LD files do not contain the flow objects, only the characterization factors. They can be downloaded and imported into any openLCA database. The no flows versions of methods must be imported on top of a database that contains flows, otherwise the methods will not appear in the database.
- LCIA Methods repositories: Repositories are available for TRACI2.1 and ReCiPe which contain the methods and all relevant flow objects. These repositories are useful for reviewing all characterization factors for flows in the FEDEFL
</details>

<details>
 <summary><b>How do I align my dataset with the NAICS folder structure?</b></summary>

All data on the Federal LCA Commons must use the North American Industry Classification System (NAICS) folder structure [NAICS - Census Bureau](https://www.census.gov/naics/).
To align new or existing processes and flows with NAICS, import the [Commons Core database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) to add the NAICS folder structure to your openLCA database and then organize flows and processes into the relevant folders. Use the NAICS Census Bureau link above to determine the appropriate 4 digit NAICS code. 
</details>
