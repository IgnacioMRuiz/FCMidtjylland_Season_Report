# GPS Data Cleaning Script

## Introduction

This script is designed for cleaning GPS data. It serves as a critical step in preparing raw GPS data for further analysis and visualization. The script automates the cleaning process, ensuring consistency and accuracy in the data prepared for analysis.

## Libraries Used

- pandas

## Features

The GPS Data Cleaning Script includes the following features:
- Data loading and preprocessing
- Cleaning operations to handle missing values, outliers, and inconsistencies
- Standardization of data formats

## Data Transformation Process

The GPS Data Cleaning Script performs several key transformations and calculations on the raw GPS data to prepare it for further analysis. Here's an overview of the steps involved:

### Importing Data

- The script starts by importing the raw GPS data from an Excel file (`GPS Data.xlsx`) using pandas, a powerful data manipulation library in Python.

### Column Separation

- A crucial transformation is the separation of the `Drill Title` column into several new columns: `Drill Type`, `Half`, `Time Division`, `Players Involved`, `Size`, and `Additional Info`. This is done to break down the combined information into more granular and analyzable components.

### Column Adjustment

- The `Half` column is then adjusted to include information from the `Time Division` column, effectively combining these two pieces of information into a single, more descriptive column.
- After the adjustment, the `Time Division` column, along with the original `Drill Title` column, is removed from the dataset as they are no longer needed in their original form.

### Data Cleaning

- The script performs specific replacements to standardize the terminology within the dataset. For example, it replaces occurrences of 'game' with 'Game' and 'full pitch' with 'Full pitch' in the `Drill Type` and `Size` columns, respectively.

### Renaming Columns

- To enhance clarity, certain columns are renamed. For instance, `Session Date` is simplified to `Date`, and `Player Name` is changed to `First Name Initial`.

### Mapping and Adding New Data

- Additionally, the script imports a separate file (`Players Involvements.xlsx`) to create a mapping between dates and match identifiers. This mapping is then applied to the GPS data to add a new `Match` column, linking each data entry with its corresponding match.

### Exporting Processed Data

- Finally, the cleaned and transformed data is exported to a new Excel file (`GPS Data.xlsx`) within the `ProcessedData` folder. This file is now cleaned, more organized, and ready for analysis or visualization, particularly in tools like Tableau.

### Conclusion

The script's processing ensures that the GPS data is not only more manageable but also primed for insightful analysis, laying a solid foundation for subsequent analytical tasks.

## Outputs

The script outputs a cleaned version of the GPS data in Excel format:
- The cleaned data is saved to an Excel file, making it easy to use in subsequent analysis or visualization tools.

## Usage

1. Ensure pandas is installed in your environment. If not, install it using pip:!pip install pandas
2. Run the script in a Python environment. The script reads the raw GPS data file and performs cleaning operations.
3. The cleaned data will be saved to the specified output path in Excel format.

## Dependencies

- Python 3.x
- pandas

## Configuration

No specific configuration is needed to run this script beyond the basic setup of a Python environment with the required libraries installed.

