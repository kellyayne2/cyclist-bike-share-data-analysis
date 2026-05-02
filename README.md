# cyclist-bike-share-data-analysis
End-to-end data analytics project using Python and Power BI (DAX) to analyze cyclist ride data and uncover usage patterns.
## Project Overview
This project analyzes 12 months of Cyclistic bike-share data to understand user behavior and identify strategies to convert casual riders into annual members.
## Business Problem
Cyclistic wants to increase the number of annual memberships. The Key question is: <b> How do casual riders and members use Cyclistic bikes differently?</b>
## Tools Used
- Python (pandas) → data cleaning & preparation
- Power BI (Dax) → dashboard & visualization

## Data Source
Public bike trip data from Divvy (Chicago bike-share system), covering January–December 2024.
The dataset used in this project is publicly available:
[Cyclistic Bike-Share Dataset] (https://divvy-tripdata.s3.amazonaws.com/index.html)
Note:
- Raw data is not included due to size limitations
- A cleaned sample dataset is provided in this repository

## Data Cleaning (Python)
The raw data was provided in 12 separate monthly files and required preprocessing:
- Combined all monthly datasets into one dataset using pd.concat()
- Removed duplicate records
- Converted date columns to proper datetime format
- Created new features:
  - Ride duration
  - Month
  - Day of week    
- Checked for missing or inconsistent values
- Removed invalid ride durations (≤0)
- Cleaned dataset was then exported for Power BI analysis.
  
## Outlier Handling
Ride duration contained extreme values (e.g., up to 1439 minutes).
Based on distribution analysis, values were filtered to focus on realistic behavior:

Minimum threshold: ≥ 2 minutes
Maximum threshold: ≤ 70 minutes

This ensured that averages and distributions reflect typical usage patterns.

## Key Analysis and Visualisation

