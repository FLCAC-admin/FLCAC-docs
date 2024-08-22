# openLCA Libraries User Guide
## What is a library?
The {term}`library` feature in openLCA 2.0 and later versions enables the use of databases together without needing to import them on top of one another. A library serves as a read only database that can easily be combined with other databases. Processes and other elements that are part of a library are not editable but can be utilized as part of processes or product systems in the main database.
Libraries are beneficial for the current set-up of the Federal LCA Commons (FLCAC) as they allow for multiple distributed repositories to be self-contained, while still promoting interoperability between repositories. The connections provided by libraries benefit multiple repositories on the FLCAC.
:::{note}
Libraries are currently an experimental feature in openLCA and may be updated based on user feedback.
:::

## Library Features

- When a library is included in a database, a new "Libraries" folder appears in the database navigation pane. Libraries are also stored in your openLCA navigation pane, outside of individual databases.

![image](https://github.com/user-attachments/assets/dd3a327b-bc76-4583-bd0f-99993eac768f)

- Library elements are incorporated into your database, but these elements are differentiated from main database elements by appearing in grey italics. Example below:
- No elements in the library database can be altered.
- Library flows and processes can be used in processes in the main database.
- Flows and providers in the main database can be replaced by library flows and providers by using the openLCA flow mapping or bulk replace features.
- Product systems and results will include library processes and their product systems.

## Downloading a repository with a Library
When you download and import a repository that is connected to a library on the FLCAC you will be prompted to connect to the library as well. The url field should automatically populate with the library FLCAC url or you can choose to add a library from a file.

If downloading a {term}`JSON-LD` file with a library from another source, aside from the FLCAC, the library file must also be downloaded and referenced when importing into openLCA.  

## Creating a process or product system
To create a process with library flows, use the same process as when adding flows from your main database. The only difference is that flows and processes are indicated as library elements with these symbol: ![image](https://github.com/user-attachments/assets/1ed6495f-9e0b-44cd-a3dd-95f7c9c13b91) ![image](https://github.com/user-attachments/assets/771adb5d-20fb-430b-b472-be087791dbd3).

Product systems also generate similarly with library processes. Ensure that library providers are connected in your model graph and check the results to ensure that they the library processes were included.

## Exporting a Library
To share a database with a library, the library must be exported and shared separately. To export a library, navigate to the "Libraries" folder in the main openLCA navigation pane, right click on the desired library, and select export.

## Importing a Library
To import a library into a main database, open the database by double clicking, right click the database name and select _"Add a library"_, then choose the desired library. The library can exist in the local version of openLCA or it can be imported from outside of openLCA.

:::{important}
If database elements (e.g., {term}`flow`s, {term}`process`es, etc.) overlap between the library and the main database, a **Tag conflicts** popup may appear.

1. _"Update data sets"_ will update all datasets with library elements
2. _"Update library tags only"_ will only tag library elements if they’re unique to the library and will not overwrite duplicate elements in the main database. **For FLCAC uses it is recommended that _"Update library tags only"_ is selected.** This allows data users to edit elements that are duplicated across the library and the main database.

![image](https://github.com/user-attachments/assets/37ed7e8b-729b-4ede-b11e-44b637fc2b96)
:::

:::{note}
A "Data conflicts" popup may appear if "Update data sets" in the above step was selected, this indicates that datasets in the main database are being updated with library datasets.
![image](https://github.com/user-attachments/assets/bddcf416-d384-4335-a1a0-bab51034431f)
:::

The library should now be added to the main database. A "Libraries" folder will appear in the main database and the added library can be viewed. Library elements appear in this folder as well as in the main database. Library elements are italicized and show as a lighter shade than the main database elements.

:::{seealso}
[How to create a library](../SOPs/3-create_a_library.md)

:::
