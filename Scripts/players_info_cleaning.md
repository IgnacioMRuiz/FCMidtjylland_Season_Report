# Players Info Processing Script

## Introduction

This script is designed to process the `Players Info.xlsx` file, focusing on organizing player information for enhanced data management and analysis. It simplifies player identification by standardizing name columns and sorting entries for better accessibility. This cleaned and structured data is essential for any analysis involving player-specific information.

## Libraries Used

- pandas

## Features

The Players Info Processing Script offers the following functionalities:
- Reading player information from an Excel file.
- Renaming columns for consistency across datasets.
- Sorting player information alphabetically by full names.
- Exporting the cleaned and organized data back into an Excel file for further use.

## Data Transformation Process

### Importing Data

- The script begins by importing the `Players Info.xlsx` file, which contains various pieces of information about players, using pandas.

### Renaming Columns

- To ensure consistency with other datasets or analyses that may use the data, the `player_name` column is renamed to `Full Name`. This change facilitates easier data integration and referencing.

### Sorting Data

- After renaming the columns, the script sorts the DataFrame alphabetically by the `Full Name` column. Sorting is a crucial step for improving the readability of the data and simplifying future searches and analyses.

### Exporting Processed Data

- The final step involves exporting the cleaned and sorted DataFrame back into an Excel file named `Players Info.xlsx`, located in the `ProcessedData` folder. This file is now ready to be used in subsequent analysis or reporting tasks, with improved structure and clarity.

## Outputs

The script outputs a processed version of the player information data in Excel format:
- The cleaned and organized data is saved to an Excel file, making it more accessible and useful for analysis or data integration purposes.

## Usage

1. Ensure you have pandas installed in your Python environment. If not, you can install it using pip: !pip install pandas
2. Run the script within a Python environment. It will automatically read the Players Info.xlsx file, apply the necessary transformations, and save the processed data.
3. The processed data will be stored in the specified output path in Excel format.

## Dependencies
- Python 3.x
- pandas

## Configuration
Running this script requires a basic setup of a Python environment with pandas installed. No additional configuration is needed beyond this setup.

## Conclusion
This script streamlines the management of player information by cleaning, organizing, and standardizing the data format. By doing so, it significantly aids in the efficiency and accuracy of data analysis processes involving player data.
