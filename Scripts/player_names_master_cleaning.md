# Player Names Master Processing Script

## Introduction

This script is specifically designed to process the `Player Names Master.xlsx` file. Its main purpose is to map full player names to their corresponding player names, creating a clean, organized representation of player identities. This processed data can be crucial for ensuring consistency and accuracy in player identification across different datasets or analyses.

## Libraries Used

- pandas

## Features

The Player Names Master Processing Script includes the following key features:
- Importing player names from an Excel file.
- Creating a dictionary to map full names to player names.
- Generating a new DataFrame that includes first names, first name initials (where applicable), and full names.
- Sorting the new DataFrame by full names for easy lookup.
- Exporting the processed data back to an Excel file.

## Data Transformation Process

### Importing Data

- The raw data is imported from the `Player Names Master.xlsx` file using pandas.

### Mapping Creation

- A dictionary is created to map each player's full name to their possible player names. This facilitates easy identification and cross-referencing of players across different data sources.

### DataFrame Transformation

- For each player, the script creates a new row in a list, including the player's first name, the first name initial (if a second naming convention exists), and the full name.
  - The script is designed to handle cases where only one naming convention is available by leaving the `First Name Initial` field as `None`.
- This list is then used to create a new DataFrame, ensuring that player names are organized and easily accessible.

### Sorting

- The new DataFrame is sorted by `Full Name` to facilitate easy searching and integration with other datasets.

### Exporting Processed Data

- The processed DataFrame is exported to an Excel file named `Player Names Master.xlsx` within the `ProcessedData` folder. This file is now optimized for further use in analyses, including player identification and data merging tasks.

## Outputs

The script outputs a processed version of the player names data in Excel format:
- The data, now structured and cleaned, is saved to an Excel file, enhancing usability for analysis or integration with other datasets.

## Usage

1. Ensure pandas is installed in your environment. If not, install it using pip:
   ```bash
   pip install pandas
2. Execute the script in a Python environment. The script will read the Player Names Master.xlsx file, perform the necessary transformations, and save the processed data.
3. The processed data will be saved to the specified output path in Excel format.

## Dependencies
- Python 3.x
- pandas

## Configuration
No specific configuration is required to run this script, other than setting up a Python environment with pandas installed.

## Conclusion
By processing and organizing player names, this script significantly enhances the reliability and efficiency of player identification across various datasets, providing a solid foundation for accurate data analysis and reporting.
