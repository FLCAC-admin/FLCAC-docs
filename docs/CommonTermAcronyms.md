# Terms and Acronyms Common to the Federal LCA Commons
The list of terms and acronyms is alphabetical according to 'Full Name'. Not all terms have an associated abbreviation or acronym. Single quotes are used to denote defined terms when deemed helpful.  

|Acronym or Abbreviation| Full Name| Definition or Descriptive Link
|----|----|----
|-|context|In the case of the FEDEFL (and often in LCA more broadly), context describes the origin or destination of an elementary flow. Context informs the directionality of an elementary flow. Resource flows are extracted from nature, while emissions are released to nature. [List of FEDEFL contexts](https://github.com/USEPA/Federal-LCA-Commons-Elementary-Flow-List/blob/master/wiki/resources/FEDEFLcontexts.xlsx). For more discussion of context see [EPA's FEDEFL Report](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=347251&Lab=NRMRL&simpleSearch=0&showCriteria=2&searchAll=elementary+flows&TIMSType=Published+Report&dateBeginPublishedPresented=07%2F31%2F2019)
|database|project database|In the context of the FLCAC, the term project database is used to refer to a collection of background and foreground LCA processes, flows, product systems. LCIA methods and other data objects as developed by an LCA practitioner(s). A project database is often composed of one or more 'repositories' and novel foreground LCI models that are typically the basis of 'product systems' under study. The goal of the FLCAC is to provide background data and a community of practice to inform consistency in developing project databases. 
|-|elementary flow|  A material (resource), energy or space that is exchanged with the biosphere. An elementary flow is characterized by a unique combination of 'flowable' and 'context' information and is assigned a 'UUID'.
|endpoint|endpoint indicator|
|EPD|Environmental Product Declaration|
|FEDEFL|Federal Elementary Flow List|Standardized list of elementary flow names, developed by the U.S. Environmental Protection Agency, used in federal LCA work. [FEDEFL GitHub](https://github.com/USEPA/fedelemflowlist)
|FLCAC|Federal LCA Commons| [LCA Commons About Us Page](https://www.lcacommons.gov/about-us)
|-|flowable|A general term for the name of a material, energy or space that is exchanged with the biosphere. For more discussion of flowables see [EPA's FEDEFL Report](https://cfpub.epa.gov/si/si_public_record_report.cfm?dirEntryId=347251&Lab=NRMRL&simpleSearch=0&showCriteria=2&searchAll=elementary+flows&TIMSType=Published+Report&dateBeginPublishedPresented=07%2F31%2F2019)
|-|functional unit| The reference unit of a 'product system' within LCA. Results are run and compared on the functional unit. [ISO 14040](https://www.iso.org/standard/37456.html)
|ISO|International Organization for Standardization|An [independent, non-governmental body](https://www.iso.org/structure.html) with members from national standards boards that develops standard procedures for technical processes, such as life cycle assessment. 
|LCA|Life Cycle Assessment| [United Nations description of environmental LCA](https://www.lifecycleinitiative.org/starting-life-cycle-thinking/life-cycle-approaches/environmental-lca/)
|midpoint|midpoint indicator|
|-|library| A type of data package limited to read-only access, intended to serve as a dependency of another data package. The library feature in openLCA 2.0 and later versions enables the use of databases together without the need to import them on top of one another. Processes and other elements that are part of a library database are not editable but can be utilized as part of processes or product systems in the main database.
|-|process| A set of related activities that convert inputs into output(s). A network of processes, the 'product system', is used to define the life cycle of a product. Processes are characterized as 'unit processes' or system processes'. For more discussion of processes see [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)
|repo|repository|
|resource|resource flow| 
|-|system process|"An aggregated life cycle result saved as a process." -from [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)
|-|technosphere flow|Intermediate product or service flows that serve as inputs to subsequent processes or comprise the functional unit of a product system. 
|-|unit process|"The  smallest (least aggregated) unit in a production system, for which input and output data are quantified." -from [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/processes/index.html?highlight=process#processes)
|UUID|Universally Unique Identifiers|Unrepeated alphanumeric code that points to specific database objects, typically within a JSON file. Within openLCA, UUIDs are assigned to processes, flows, product systems, projects, parameters, impact categories and LCIA methods. Link to UUID search in the [openLCA 2 manual](https://greendelta.github.io/openLCA2-manual/introduction/index.html?search=UUID)









