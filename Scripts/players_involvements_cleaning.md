# Players Involvements Processing Script

## Introduction

This script processes the `Players Involvements.xlsx` file, extracting crucial match and player involvement information from a composite `file` column. It transforms this data into a more structured format, enhancing its usability for analysis. By parsing detailed match information and categorizing player actions, this script facilitates deeper insights into player performances and match outcomes.

## Libraries Used

- pandas

## Features

The Players Involvements Processing Script is equipped with the following capabilities:
- Loading player involvements data from an Excel file.
- Extracting and transforming date information into a standardized format.
- Parsing match details, results, and competition types from a composite string.
- Renaming columns for clarity and consistency with broader data analysis standards.
- Determining match outcomes for FCM based on extracted scores.
- Exporting the transformed data into a new, structured Excel file.

## Data Transformation Process

### Importing Data

- The raw data is imported from the `Players Involvements.xlsx` file, leveraging pandas for efficient data manipulation.

### Date and Match Information Extraction

- A custom function, `transform_date`, is used to convert date strings into a standardized date format.
- New columns (`Date`, `Match`, `Match Result`, `Competition`) are extracted from the `file` column, which contains concatenated match and date information.

### Column Cleanup and Renaming

- The original `file` column, now redundant, is removed from the dataset.
- Columns are renamed for enhanced clarity, aligning with the dataset's intended analysis use cases.

### Match Outcome Determination

- A function, `determine_result`, is implemented to evaluate whether FCM won, lost, or drew a match based on the parsed match result and the specific game's context. This adds valuable context for analyzing player performances within the framework of match outcomes.

### Exporting Processed Data

- The processed data, now richly structured and annotated, is exported back into an Excel file (`Players Involvements.xlsx`) within the `ProcessedData` folder. This file is primed for further analytical tasks, offering a deep dive into the nuances of player involvements and match dynamics.

## Outputs

The script outputs a processed version of the player involvements data in Excel format:
- This enhanced dataset, saved to an Excel file, is now ready for in-depth analysis, supporting both individual player performance reviews and broader match outcome studies.

## Usage

1. Ensure pandas is installed in your environment. If not, install it using pip: !pip install pandas
2. Run the script within a Python environment. It will read the Players Involvements.xlsx file, perform the transformations, and output the processed data.
3. The transformed data will be available at the specified output path in Excel format.

## Dependencies

- Python 3.x
- pandas

## Configuration

No special configuration is needed beyond a standard Python environment with pandas installed.

## Conclusion

By systematically transforming and enriching player involvements data, this script unlocks new avenues for analysis, offering insights into player contributions, match outcomes, and competition dynamics. It's an essential tool for detailed sports analytics, particularly within the context of FCM's performance evaluation.
