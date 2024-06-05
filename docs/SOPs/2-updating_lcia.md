# Updating Life Cycle Impact Assessment Methods using LCIA Formatter

## Purpose

This SOP documents procedures for making updates or adding new LCIA methods to the Federal LCA Commons (FLCAC).

## Procedure

1. Any changes to an LCIA Method must align with a lciafmt package release and update to the package version.
LCIA Formatter release notes will indicate changes to characterization factors for all methods.

2. Upon package release, revised methods are added to the [EPA Data Commons](https://dmap-data-commons-ord.s3.amazonaws.com/index.html?prefix=#lciafmt/) in parquet format.

3. The LCIA methods are updated on the Federal LCA Commons in the appropriate repository (if applicable):
Generate with the LCIA Formatter a JSON-LD version of the method _with_ all flows.
Import that JSON-LD file into the repository and select "Overwrite all exisiting data sets" to update both the LCIA method and the underlying elementary flows.
Confirm that no uncharacterized flows remain (e.g., due to a change in mapping).
If any remain, remove them from the repository.

4. The LCIA methods are added as JSON-LD to lcacommons.gov ["No-flows" LCIA Method page](https://www.lcacommons.gov/lcia-methods-without-flows):
Generate with the LCIA Formatter a JSON-LD version of the method _without_ flows.
Create a new entry in the USDA Ag Data Commons.
Once approved, the entry will be added to Data.gov.
Add links to the No-flows page, and move the prior version to the archive section of the page.

