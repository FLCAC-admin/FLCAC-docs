# Life Cycle Impact Assessment (LCIA) Methods

A number of LCIA methods have been created for use with the Federal Elementary Flow List (FEDEFL) and the Federal LCA Commons (FLCAC).
The [LCIA Formatter](https://github.com/USEPA/LCIAformatter) is the primary tool for creating these methods.

> LCIA formatter, or lciafmt, is a Python tool for standardizing the format and flows of life cycle impact assessment (LCIA) data.
> The tool acquires LCIA data transparently from its original source, cleans the data, shapes them into a standard format using the LCIAmethod format, and optionally applies flow mappings as defined in the FEDEFL.

An article describing the [LCIA Formatter was published in the Journal of Open Source Software (JOSS)](https://doi.org/10.21105/joss.03392)

## Available Methods

:::{table}
:name: available_lcia_methods
|LCIA Data|Provider|Link|
|---|---|---|
|TRACI 2.1|US Environmental Protection Agency|[Tool for Reduction and Assessment of Chemicals and Other Environmental Impacts](https://www.epa.gov/chemical-research/tool-reduction-and-assessment-chemicals-and-other-environmental-impacts-traci)|
|ReCiPe 2016 Midpoint|National Institute for Public Health and the Environment (The Netherlands)|[LCIA: the ReCiPe Model](https://www.rivm.nl/en/life-cycle-assessment-lca/recipe)|
|ReCiPe 2016 Endpoint|National Institute for Public Health and the Environment (The Netherlands)|[LCIA: the ReCiPe Model](https://www.rivm.nl/en/life-cycle-assessment-lca/recipe)|
|ImpactWorld+ Midpoint|International Reference Center for Life Cycle of Products, Services and Systems (CIRAIG)|[ImpactWorld+](http://www.impactworldplus.org/en/team.php)|
|ImpactWorld+ Endpoint|International Reference Center for Life Cycle of Products, Services and Systems (CIRAIG)|[ImpactWorld+](http://www.impactworldplus.org/en/team.php)|
|IPCC GWP|Intergovernmental Panel on Climate Change (IPCC)| |
|FEDEFL Inventory Methods|US Environmental Protection Agency|[FEDEFL Inventory Methods](https://github.com/USEPA/LCIAformatter/wiki/Inventory-Methods)|
|ISO21930-LCIA-US|[US Environmental Protection Agency](https://www.epa.gov/greenerproducts/data-quality-improvements)|[Characterization Factors for Construction Material EPD Indicators](https://github.com/USEPA/LCIAformatter/blob/master/lciafmt/data/ISO21930-LCIA-US.yaml)|

:::

## Accessing LCIA Methods
LCIA methods aligned with the FEDEFL are available in two forms.
Both are updated simultaneously, and results will be the same regardless of which version is used.
- [LCIA Methods without flows](https://www.lcacommons.gov/lcia-methods-without-flows):
These JSON-LD files do not contain the flows, only the characterization factors.
They can be downloaded and imported into any openLCA database.
The "No flows" versions of methods must be imported _into_ a database that contains the relevant flows already, otherwise the methods will not calculate correctly.
Updating a local database with new data which contains new elementary flows (e.g., importing a new process from a repository on the FLCAC) may result in new, uncharacterized flows in the database.
In these cases, the "No flows" methods should be **re-imported** to ensure that all elementary flows are characterized.
Using the "No flows" version of an LCIA method allows the practitioner to limit the number of elementary flows in their project database, simplifying LCIA flow checks.

- LCIA Methods repositories: [Repositories](https://www.lcacommons.gov/lca-collaboration/) are available which contain the methods and all relevant flow objects.
These repositories are useful for reviewing all characterization factors for flows in the FEDEFL.
They can be downloaded and imported into a user's local database.
However doing so will also import _all_ FEDEFL flows characterized by the method, often resulting in over 100,000 flow objects.

If you require the LCIA data in a different format, please reach out to the Data Curators at FederalLCACommons@erg.com

## Issues and Bugs
If you identify an error or have questions about specific methods, please use the [Issues](https://github.com/USEPA/LCIAformatter/issues) or [Discussions](https://github.com/USEPA/LCIAformatter/discussions) feature of the LCIA Formatter to report them.
If you have questions regarding accessing or using the methods in openLCA, please use the [Issues](https://github.com/FLCAC-admin/FLCAC-docs/issues) or [Discussions](https://github.com/FLCAC-admin/FLCAC-docs/discussions) feature of the FLCAC Curation repository.
