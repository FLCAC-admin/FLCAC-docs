# Updating the Federal Elementary Flow List

## Purpose

This SOP documents procedures for making changes to the Federal Elementary Flow List (FEDEFL) data objects on the Federal LCA Commons (FLCAC).

## Procedure

1. Any changes to the FEDEFL must align with a fedelemflowlist package release and update to the list version.
Fedelemflowlist release notes will indicate any changes to the flow list (via additions or deletions).

2. Upon package release, the FEDEFL is added to the [EPA Data Commons](https://dmap-data-commons-ord.s3.amazonaws.com/index.html?prefix=#fedelemflowlist/) in parquet and JSON-LD formats.

3. The FEDEFL is updated on the Federal LCA Commons Elementary Flow List repository:
Import the JSON-LD file into the repository and select "Overwrite all exisiting data sets".
If any flows need to be removed, delete them manually.

