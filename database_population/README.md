# Database Population

## Overview
This project implements a **basic ETL (Extract, Transform, Load) pipeline** for processing SAT score data.  
The pipeline performs **data exploration, cleaning, transformation, and storage** of the final dataset.

The workflow is executed in a **Jupyter Notebook** and results in a cleaned dataset that is saved both as a **CSV file** and loaded into a **PostgreSQL database** for further analysis.

---

## Data Sources

- **SAT Score Dataset:** `sat-results.csv`
- **Cleaned SAT Score Dataset:** `cleaned_sat_results.csv`
- **Jupyter Notebook:** `sat_modeling.ipynb`

---

## ETL Pipeline Steps

### 1. Data Extraction
The raw SAT dataset (`sat-results.csv`) is loaded into the notebook for initial exploration and processing.

### 2. Data Exploration
Initial exploration is performed to understand:
- Dataset structure
- Column formats
- Potential inconsistencies or missing values

This step helps identify necessary cleaning and transformation steps.

### 3. Data Cleaning
Data cleaning operations are applied to improve data quality, including:
- Handling missing or inconsistent values
- Standardizing column formats
- Preparing the dataset for analysis and database storage

### 4. Data Transformation
Relevant transformations are applied to ensure the dataset is structured appropriately for downstream use, including:
- Formatting columns
- Creating consistent data types
- Preparing the dataset for relational storage.

### 5. Data Loading
The cleaned dataset is persisted in two formats:

- **CSV Output:** `cleaned_sat_results.csv`
- **PostgreSQL Database:** for structured storage and querying

This enables the dataset to be used for further **SQL-based analysis and reporting**.

---

## Key Outcome
The pipeline produces a **clean and structured SAT score dataset** that can be reliably used for analysis, visualization, or integration with other educational datasets.

---

## Recommendations

**Automate the Pipeline**  
Convert the notebook workflow into a scheduled ETL process using tools such as workflow orchestration or scripts.

**Add Data Validation Checks**  
Introduce validation rules to automatically detect missing values, incorrect formats, or anomalies during the transformation stage.

**Implement Logging and Error Handling**  
Add logging to track pipeline execution and improve debugging when errors occur.

**Enable Incremental Updates**  
Design the pipeline to process only new or updated records rather than reprocessing the entire dataset each time.
