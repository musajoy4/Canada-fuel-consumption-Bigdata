# Big Data Project -- Fuel Economy Analysis (1995--2024)

## Overview

This project analyzes the **Fuel Economy dataset** (1995--2024), a
comprehensive collection of vehicle performance and environmental
metrics with 23,200 records. The data was sourced from
[open.canada.ca](https://open.canada.ca/data), cleaned, transformed, and
processed using **MongoDB, Python (pandas), SSIS, SQL Server, SSAS, and
Tableau**.

The goal is to explore trends in fuel efficiency, emissions, and vehicle
performance, providing insights for **manufacturers, policymakers, and
environmental analysts**.

------------------------------------------------------------------------

## Business Context

The dataset supports analysis of:\
- Fuel efficiency trends across decades\
- Vehicle class & transmission efficiency\
- CO₂ emissions vs. engine size\
- Make-level comparisons\
- Environmental policy impacts

------------------------------------------------------------------------

## Tools & Workflow

1.  **MongoDB** -- Imported and merged two CSV datasets (1995--2014,
    2015--2024).\
2.  **Python (pandas, pymongo)** -- Data cleaning, deduplication, and
    feature engineering.\
3.  **SSIS (ETL pipeline)** -- Migrated data from MongoDB to SQL
    Server.\
4.  **SQL Server** -- Structured data storage and query execution.\
5.  **SSAS** -- Prepared multidimensional analysis.\
6.  **Tableau** -- Visualization and dashboard creation.

------------------------------------------------------------------------

## Analysis & Insights

-   **Fuel Efficiency Trends (1995--2024):** Overall MPG improved from
    \~24 (1990s) to \~28 (2010s), with slight decline in 2020s.\
-   **Vehicle Class Comparison:** Compacts outperform SUVs & Pickups;
    diesel vehicles often more efficient than premium gas.\
-   **CO₂ vs. Engine Size:** Positive correlation, but emissions
    declined over decades for similar engine sizes.\
-   **Transmission Impact:** Manuals were historically more efficient,
    but automatics (CVT/advanced) have closed the gap.\
-   **Make-Level Analysis:** Toyota & Honda lead in efficiency (\~28--35
    MPG), luxury brands like Bentley trail (\~15 MPG).

------------------------------------------------------------------------
## 🔄 SSIS Integration (ETL Pipeline)

The ETL (Extract, Transform, Load) process was built using **SQL Server
Integration Services (SSIS)** to automate data migration and
integration.

**Steps:**\
1. **Source Connection:** Connected MongoDB collections
(`fuel_1995_2014`, `fuel_2015_2024`) as data sources.\
2. **Dataflow Setup:** Pulled merged data into the SSIS pipeline.\
3. **Transformation Tasks:**\
- Mapped MongoDB fields → SQL Server schema.\
- Applied data type conversions.\
- Handled NULLs and cleaned invalid entries.\
4. **Destination Connection:** Created the **FuelEconomy** table in SQL
Server (`BigDataProject` database).\
5. **Execution:** Ran ETL to migrate data into SQL Server.\
6. **Validation:** Queried the first 1000 rows to verify migration
accuracy.
------------------------------------------------------------------------

##  Data Sources

-   [1995--2014
    Dataset](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64/resource/e10efaa3-a8cc-4072-845a-13e03d996c30)\
-   [2015--2024
    Dataset](https://open.canada.ca/data/en/dataset/98f1a129-f628-4ce4-b24d-6f16bf24dd64/resource/42495676-28b7-40f3-b0e0-3d7fe005ca56)


------------------------------------------------------------------------

## Visualizations (Tableau)

- Fuel Efficiency Trends Over Time\
- Vehicle Class Efficiency Comparison\
- CO₂ Emissions vs. Engine Size\
- Transmission Impact on Efficiency\
- Make-Level Analysis
