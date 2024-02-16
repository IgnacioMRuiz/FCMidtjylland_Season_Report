# Raw Data Files
This folder contains the raw data files used in the project. These files are crucial for the data transformation processes and subsequent analyses. The raw data consists of several Excel spreadsheets with potentially extractable information. These files include:

- `GPS Data.xlsx`
- `Player Names Master.xlsx`
- `Players Info.xlsx`
- `Players Involvements.xlsx`

Each file contains a series of columns that need to be renamed to optimize the connections between the different files. The transformation code, located in the `Scripts` folder, processes each file and uploads the results to the `Data/ProcessedData` folder.

**Note:** While these files currently originate from Excel spreadsheets, the ideal data source for this project would be a database. This would streamline data management and potentially automate updates and transformations.
