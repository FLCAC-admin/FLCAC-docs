# Creating a Library

## Purpose

This SOP documents procedures for creating libraries from Federal LCA Commons (FLCAC) repositories in openLCA. Please reference the [openLCA Libraries User Guide](https://flcac-admin.github.io/FLCAC-docs/flcac-openlca-library-user-guidance) for information on importing, exporting, and modeling with libraries. This SOP is inteded for use by the Data Curators.

## Procedure

**1. Prepare the library database**
 - Adjust the database that is intended to be transformed into a library as needed. Once this database becomes a library, edits are more difficult to implement.
- Delete all exchanges with an amount of zero, the matrices in a library do not currently support zeroes.

:::{dropdown} Python script to remove zero amounts from exchanges
**To use this script in openLCA, select "Tools" --> "Developer Tools" --> "Python".**

```python
from java.util import ArrayList
pDao = ProcessDao(db)
for d in pDao.getDescriptors():
  p = pDao.getForId(d.id)
  toRemove = ArrayList()
  for e in p.exchanges:
    if e.amount == 0 and e.id == p.quantitativeReference.id:
      log.info("Invalid: quantitative reference has zero amount in process " + p.name + " " + p.refId)
      continue
    if e.amount == 0 and e.isInput and e.flow.flowType == FlowType.WASTE_FLOW:
      log.info("Removing zero amount waste input " + e.flow.name + " from process " + p.name + " " + p.refId)
      toRemove.add(e)
    if e.amount == 0 and not e.isInput and e.flow.flowType == FlowType.PRODUCT_FLOW:
      log.info("Removing zero amount product output " + e.flow.name + " from process " + p.name + " " + p.refId)
      toRemove.add(e)
  log.info("toRemove.size(): " + str(toRemove.size()))
  if not toRemove.isEmpty():
    for e in toRemove:
      p.exchanges.remove(e)
    pDao.update(p)
```
:::

 - Run a validation check on the database (Right click on database --> “Validate”) and resolve any major errors. Please contact the Data Curators if questions arise about validation errors.

**2. Transform the library database into a library element**
 - Tools --> “Library export (experimental)”
 - Assign a name to the library
 - Set the Allocation Method to “As defined in processes”
 - Selecting “Precalculate matrices” will speed up calculation times, but if this is selected then it is not recommended to choose “Only tag as library datasets” in a future step (this will cause issues with calculations)
 - Selecting “With uncertainty distributions” and/or “Regionalized” will bring additional metadata into the library. These options will increase the size of the library and may slow down calculations. For FLCAC uses it is recommended to select these options to ensure metadata consistency.
 - Press “Ok” and the database will be converted into a library. The database will remain the same and the library will appear in the navigation pane of openLCA under the “Libraries” folder.
