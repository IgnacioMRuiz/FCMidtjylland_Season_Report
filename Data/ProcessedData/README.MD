# Processed Data

The `ProcessedData` folder contains transformed data files, which have been processed through scripts located in the `Scripts` folder. These scripts are designed to clean and prepare the raw data, making it suitable for analysis and visualization. There is a dedicated script for each data file, plus a Master script that orchestrates the execution of all individual scripts, ensuring a streamlined transformation process.
These files include:
- `GPS Data.xlsx`
- `Player Names Master.xlsx`
- `Players Info.xlsx`
- `Players Involvements.xlsx`

The processed files serve as the primary data source for a Tableau dashboard, providing insights and visualizations based on the cleaned data. Ideally, instead of relying on local files, this data would be managed within a database to facilitate more dynamic and automated data handling and integration with Tableau.

**Note:** While the current setup relies on processed Excel files, transitioning to a database as the primary data source for Tableau would enhance the efficiency and scalability of data management and visualization processes.
