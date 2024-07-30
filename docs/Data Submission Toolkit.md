# Data Submission Toolkit
This document provides an overview of the data submission process and relevant resources. Please refer to the [Data Submission Handbook](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/00-sub-handbook-landing.md) for detailed information regarding the submission process. The [Frequently Asked Questions page](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/FAQ.md) includes more information about many of these topics.

Table of Contents:
- [Data Submission Steps](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#data-submission-steps)
- [Data Preparation Steps](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#data-preparation-steps)
- [Notes on Data Submissions and Maintenance of Data](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#notes-on-data-submissions-and-maintenance-of-data)
- [Data Provider Questionnaire](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#data-provider-questionnaire)
- [Technical Assistance Resources for Data Providers](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#technical-assistance-resources-for-data-providers)

## Data Submission Steps
1.	Become familiar with the [Federal LCA Commons platform](https://www.lcacommons.gov/)
2.	Contact the FLCAC data curators to set up an initial meeting to discuss your datasets intended for submission to the FLCAC
    - Prior to this meeting fill out the [data submission questionnaire](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Submission%20Toolkit.md#data-provider-questionnaire) and submit it to the data curators at FederalLCACommons@erg.com 
    - During this meeting we will discuss the specific steps needed to prepare your data for submission and assign roles 
3.	Download the openLCA software and install it on your computer
4.	Prepare your unit processes/product system as discussed in the initial curation meeting ([overview of the data preparation steps](https://github.com/FLCAC-admin/FLCAC-Curation/edit/main/docs/Data%20Submission%20Overview%20and%20Resources.md#data-preparation-steps))
5.	Export ONLY your prepared datasets as a zipped JSON-LD file & submit to the data curators or add the datasets to a repository directly through the collaboration server
6.	Reconcile issues identified by the data curators during the review process & check results
7.	Approve the final version
8.	FLCAC data curators will publish your datasets on the FLCAC

## Data Preparation Steps
-	Import your data into openLCA (import steps depend on original data source)
-	Download and import the latest version of the repository that you will be submitting data to into your database
-	[Flow map elementary flows to FEDEFL flows](https://github.com/FLCAC-admin/FLCAC-Curation/edit/main/docs/FAQ.md#data-submission)
-	[Flow map technosphere flows to existing FLCAC flows](https://github.com/FLCAC-admin/FLCAC-Curation/edit/main/docs/FAQ.md#data-submission)
-	Download and import the [Federal LCA Commons Core database](https://www.lcacommons.gov/lca-collaboration/Federal_LCA_Commons/Fed_Commons_core_database/datasets) into your local database
-	Move your processes and flows into the correct NAICS folders, you can search for the relevant folders on the [Census Bureau website here](https://www.census.gov/naics/)
-	Delete the old, unused folders that were brought in with your original database
-	[Run results](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/FAQ.md#openlca) and compare values to the original model 
-	Complete the metadata fields according to the [metadata guidelines](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#metadata-guidance-tables)
-	Send your draft database to the FLCAC curators for review

## Notes on Data Submissions and Maintenance of Data
-	The FLCAC data curators provide QA/QC checks on data submissions to ensure that they adhere to FLCAC standards.
-	The FLCAC data curators do not review the originating LCA from which LCI data are generated.
-	Static LCIA results are not maintained over time. Background datasets in a product system may be updated over time (e.g., the electricity grid will be updated to represent the most recent year of data available, if an incoming chemical production process is updated and linked to your product system this will be updated).
-	The FLCAC data curators will make corrections to your data if errors arise. The curators will reach out to original dataset owners to notify them of changes.

## Data Provider Questionnaire
Can be accessed [here](https://github.com/FLCAC-admin/FLCAC-Curation/blob/main/docs/Data%20Provider%20Questionnaire.docx) in Microsoft Word format 
| **Question**                                                                                                                                                                             | **Response** |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------ |
| **Describe the number and scope of the intended unit processes for submission.**                                                                                                     |              |
| **Describe the underlying source of the data. (Please share links or pdfs as appropriate)**                                                                                          |              |
| **What flow list is used for the elementary flows (e.g., ILCD, openLCA, SimaPro, etc)?**                                                                                             |              |
| **What impact assessment categories and/or inventory categories is the data representative of (e.g., global warming potential, eutrophication potential, water consumption, etc.)?** |              |
| **What format is the data currently in (e.g., SimaPro, excel, openLCA, etc.)?**                                                                                                      |              |
| **Will this data be submitted to part of an existing repository or will a new repository be needed?**                                                                                |              |
| **Are there any anticipated cross-repository dependencies (e.g., new processes will require data from the electricity baseline)?**                                                   |              |
| **What is the anticipated timing of submission and timing of curation support?**                                                                                                     |              |
| **Can we share publicly that you are working towards publishing this dataset on the FLCAC?**                                                                                         |              |
| **Is this effort in collaboration with or in support of a governmental agency? If so, will that agency require a review process for data submitted to the FLCAC?**                   |              |
| **Point of contact for submission** **(name and email).**                                                                                                                            |              |
| **Please provide any other details about level of curation support needed.**                                                                                                         |              |

## Technical Assistance Resources for Data Providers
### openLCA
-	[openLCA Download](https://www.openlca.org/download/): openLCA download page. Recommended to download the .zip file format.
-	[openLCA Learning and Support](https://www.openlca.org/learning/): Includes the openLCA manual, case studies, and videos to review openLCA concepts.
-	[openLCA Blog](https://www.openlca.org/blog/): GreenDelta’s method for direct communication with the openLCA community. News about releases and bug fixes.
-	[openLCA Forum](https://ask.openlca.org/): Support platform for OpenLCA. Question and answer platform.
### Federal LCA Commons
-	[Landing Page](https://www.lcacommons.gov/): Select “Browse Repositories” to access the repositories
-	[LCIA Methods without Flows](https://www.lcacommons.gov/lcia-methods-without-flows): Recommended to download and use these flows in a database that already has flows in it. 
-	[Federal LCA Commons GitHub](https://github.com/FLCAC-admin/FLCAC-Curation/tree/main): Current GitHub page that include documentation, FAQs, and other resources for the Federal LCA Commons. Platform to document issues related to the Federal LCA Commons repositories.
### Submission Guidance:
- [USLCI Submission Handbook](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/00-sub-handbook-landing.md): Submission handbook for USLCI and other FLCAC repositories. Section 2: How do I publish my data in USLCI? Provides technical details of the publishing process.
-	[Metadata Guidance Tables](https://github.com/FLCAC-admin/uslci-content/blob/dev/docs/submission_handbook/02-how-to-publish-in-the-uslci.md#metadata-guidance-tables): These tables provide information on metadata that should be included in each openLCA field with examples.
    - It is preferred that data providers fill in their metadata directly in openLCA, but if needed an excel template can be provided to fill out metadata.
-	[YouTube Quick Help Series](https://www.youtube.com/playlist?list=PLmIn8Hncs7bFUOyXZNGXwG4LtdoTfLz6Q): Includes videos on how to work with repositories on the Federal LCA Commons, using USLCI as an example.
-	[YouTube Video on the Data Submission Process](https://www.youtube.com/watch?v=IlPlYet8llY&list=PLmIn8Hncs7bFUOyXZNGXwG4LtdoTfLz6Q&index=9): Overviews the submission process with an example dataset. Includes guidance on importing/exporting, aligning the folder structure with NAICS, flow mapping, completing metadata, and more.
