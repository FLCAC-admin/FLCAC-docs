---
title: Versioning
abbreviations:
  FLCAC: Federal LCA Commons
---

The {term}`FLCAC collaboration server <collaboration server>` now allows multiple repository versions to be published.
This guidance therefore aims to ensure that a standard version numbering system is used across FLCAC repos.

Elements of this guidance on when and why to increment each element of the MAJOR.MINOR.PATCH version numbers are derived from both the [Semantic Versioning](https://semver.org/) and [Data Package v2](https://datapackage.org/recipes/data-package-version/) standard approaches to versioning.

FLCAC repositories should adopt a MAJOR.MINOR.PATCH version number format, wherein:

- MAJOR version denotes updates to the openLCA and/or FLCAC schema(s) (the latter is pending formalization) which are non-backward-compatible
- MINOR uses the date stamp (YYYY-MM) of the release commit on the FLCAC collaboration server, and denotes additions and/or revisions to the repo
- PATCH is incremented for corrections (errors, omissions, etc.) and small additions/revisions (e.g., shuffling metadata between a Process and Source object)

For example, let's say that I—an FLCAC repo maintainer—have a repo with a current version number of 1.2024-03.0.
It's now June 2024, and I've committed a collection of new {term}`process` objects that I'd like to release.
In this case, the new release version number should be 1.2024-06.0. 
If sometime in July I catch and squash a few bugs in the data, metadata, etc. then my new version number would be 1.2024-06.1, since we only need to increment PATCH and not MINOR version.
