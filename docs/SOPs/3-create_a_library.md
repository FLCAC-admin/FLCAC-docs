# Creating a Library

## Purpose

...

## Procedure

1. Prepare the library database:
    - Adjust the database that is intended to be transformed into a library as needed. Once this database becomes a library, edits are more difficult to implement.
    - Delete all exchanges with an amount of zero, the matrices in a library do not currently support zeroes.
    - Run a validation check on the database (Right click on database  “Validate”) and resolve any major errors.

2. Transform the library database into a library element:
    - Tools --> “Library export (experimental)”
    - Assign a name to the library
    - Set the Allocation Method to “As defined in processes”
    - Selecting “Precalculate matrices” will speed up calculation times, but if this is selected then it is not recommended to choose “Only tag as library datasets” in a future step (this will cause issues with calculations)
    - Selecting “With uncertainty distributions” and/or “Regionalized” will bring additional metadata into the library. These options will increase the size of the library and may slow down calculations. For FLCAC uses it is recommended to select these options to ensure metadata consistency.
    - Press “Ok” and the database will be converted into a library. The database will remain the same and the library will appear in the navigation pane of openLCA under the “Libraries” folder.
