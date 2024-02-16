# Tableau Data Connection and Dashboard Creation

## Introduction

After the data cleaning process, all cleaned files are stored in the `Data/ProcessedData` folder. This README outlines the process of connecting these cleaned datasets with Tableau, detailing how they are imported, connected, and utilized to feed into three main dashboards. It also describes the creation of calculated fields and the setup of interactivity through shared filters across dashboard sheets.

## Data Import and Connection

### Dataframes Imported into Tableau

The cleaned datasets from the `ProcessedData` folder imported into Tableau are:
- Player Names Master
- GPS Data
- Players Info
- Players Involvements

### Connections Between Dataframes

The datasets are interconnected through various columns to form a comprehensive data model:
- **Player Names Master** serves as the main dataframe.
- **GPS Data** is connected through the common column `First Name Initial`, forming a one-to-many relationship.
- **Players Info** connects via `Full Name`, establishing a one-to-one relationship.
- **Players Involvements** links through `First Name`, creating a one-to-many relationship.

## Calculated Fields and Parameters

### GPS Data Calculations

For the `GPS Data`, new metrics are calculated for `1st Half` and `2nd Half` using the following formulas:

- Accelerations, Decelerations, Playing Time, and Distance:
  - `IF [Half] = '1st half' THEN [Metric] ELSE 0 END`
  - `IF [Half] = '2nd half' THEN [Metric] ELSE 0 END`

### Players Involvements Calculations

1. **Total Actions** for each player, such as Finish, Assist, and 2nd Assist:
   - `IF [Action Type] = "Finish" THEN 1 ELSE 0 END`
2. **Actions Resulting in Goal or Big Chance**:
   - `IF [Action Type] = "Finish" AND [Outcome] = "Goal" THEN 1 ELSE 0 END`
   - `IF [Action Type] = "Finish" AND [Outcome] = "Big Chance" THEN 1 ELSE 0 END`
   - Applied similarly for Assist and 2nd Assist actions.
3. **Total Involvement**:
   - `Goal Involvement: [Goal Finish] + [Goal Assist] + [Goal 2ndAssist]`
   - `Big Chance Involvement: [Big Chance Finish] + [Big Chance Assist] + [Big Chance 2ndAssist]`

### General Workbook Calculated Fields and Parameter

- **Match Day**: `INDEX()` for counting match days.
- **Physical KPIs**:
  - A parameter to create dynamic tables based on physical performance metrics like Accelerations, Decelerations, and Distance.
  - `CASE [Parámetros].[Physical KPIs]
    WHEN "Accelerations" THEN SUM([Accelerations])
    WHEN "Decelerations" THEN SUM([Decelerations])
    WHEN "Distance" THEN SUM([Distance])
    END`

### Parameter Explanation

Parameters in Tableau allow users to input or select data to modify views or calculations dynamically. The `Physical KPIs` parameter is used here to create interactive, dynamic tables that adjust based on user selection, enhancing the analytical flexibility of the dashboards.

## Dashboards and Interactivity

The dashboards are designed to provide comprehensive insights, with worksheet filters shared among sheets within the same dashboard to enhance interactivity and user experience. Calculated fields and parameters further enrich the dashboards, offering custom analytics and perspectives on the data.

### Workbook and Dashboard Sharing

- The workbooks are meticulously organized, with non-essential sheets hidden to streamline the user interface.
- The dashboards are shared on Tableau Public to facilitate easy access.

## Files Included in the Folder

- **FCM_Season_Report.twb**: The Tableau Desktop document.
- **Sheet1+ (Varias conexiones).hyper**: Automatically generated upon data extraction for Tableau Public publishing.

## Tableau Public Link
[FCM Season Report - Team Physical Performance](https://public.tableau.com/views/FCM_Season_Report/TeamPhysicalPerformance?:language=en-US&:sid=&:display_count=n&:origin=viz_share_link)

