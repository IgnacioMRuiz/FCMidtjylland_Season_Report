# Automated Data Cleaning Notebooks Execution Script

## Introduction

This script is designed to automate the execution of a series of Jupyter Notebooks, each responsible for cleaning different segments of data within a sports analytics context. By streamlining the execution of these notebooks, the script ensures that data cleaning processes are consistently applied, making the data ready for analysis and visualization.

## Libraries and Tools Used

- os
- subprocess

## Features

The Automated Data Cleaning Notebooks Execution Script offers the following functionalities:
- Maintains a dictionary of descriptive names and paths for each data cleaning Jupyter Notebook.
- Utilizes `nbconvert` to execute each notebook in place, allowing for the transformation and cleaning of data as defined within each notebook.
- Provides console feedback on the progress of notebook executions, enhancing transparency and traceability of the data cleaning process.

## Data Cleaning Notebooks

The script automates the execution of the following data cleaning notebooks:
- **Player Names Master Cleaning**: Cleans and organizes player names data.
- **Players Info Cleaning**: Standardizes and sorts player information data.
- **Players Involvements Cleaning**: Extracts and categorizes player involvement in matches.
- **GPS Data Cleaning**: Processes GPS data for player tracking and analysis.

## Execution Process

### Setting Up Notebook Paths

- A dictionary maps descriptive names to the file paths of Jupyter Notebooks responsible for data cleaning tasks.

### Automated Execution

- For each notebook, the script uses `nbconvert` to run the notebook in place. This process applies all data cleaning transformations specified within each notebook to the corresponding datasets.
- The script outputs progress messages to the console, indicating which notebook is currently being executed, enhancing the user's visibility into the process.

### Completion Confirmation

- Upon successfully executing all notebooks, the script prints a confirmation message, signaling that all data has been cleaned and is ready for subsequent analysis.

## Usage

Before running the script, ensure you have the necessary environment set up, including Jupyter Notebook and any dependencies required by the individual notebooks. To execute the script:

1. Open a terminal in the environment where Jupyter Notebook and the `subprocess` module are available.
2. Run the Python script. It will automatically process each specified Jupyter Notebook in turn.
3. Monitor the console output for progress updates and completion confirmation.

## Dependencies

- Python
- Jupyter Notebook
- nbconvert

## Configuration

Ensure all paths in the `notebooks` dictionary correctly point to the locations of your Jupyter Notebooks. Modify the paths as necessary to fit your project's directory structure.

### Conclusion

This script facilitates a hands-off approach to executing multiple data cleaning Jupyter Notebooks, streamlining the preparation of diverse datasets for analysis. By automating this process, it saves time and ensures consistency across data cleaning operations, contributing significantly to the efficiency of the overall data analysis workflow.

