# Database Exploration

## Overview
This project explores an **NYC school dataset stored in a PostgreSQL database** to analyze patterns in school distribution, demographics, and accessibility across boroughs.

The analysis was performed using **SQL queries executed within a Jupyter Notebook**, retrieving and examining information from multiple related tables.

### Data Sources

PostgreSQL database with the following tables:

- **high_school_directory** – School names, locations, school types, and program offerings.
- **school_demographics** – Enrollment data and student demographics such as English Language Learners (ELL), Free/Reduced Price Lunch (FRPL), and disability statistics.
- **school_safety_report** – Reported incidents by type and location.

Additional resources:
- **Jupyter Notebook:** `database_exploration.ipynb`
- **Table descriptions:** Google Sheet documentation.

---

## Key Insights

**Geographic Limitation:** The *school_demographics* table contains data exclusively for **Manhattan**, making city-wide comparisons across the five boroughs impossible.

**Temporal Ambiguity:** The dataset spans multiple school years without a specified filter, leading to redundant records and inconsistent ranking results.

**Critical Data Sparsity:** Significant missing values in the *sped_percent* field prevent a full "Top 3" analysis, as the query returns only a single valid school record.

---

## Recommendations

**Apply Time-Based Filtering**  
Introduce a filter for a specific school year to remove duplicate or inconsistent records and improve the reliability of comparisons.

**Improve Data Completeness**  
Address missing values in key fields such as *sped_percent* through data cleaning, imputation, or by sourcing additional data.

**Expand Borough Coverage**  
Integrate demographic data for all boroughs to enable meaningful city-wide comparisons and analyses.

**Enhance Data Validation**  
Implement validation checks during data ingestion to reduce missing values and ensure consistent data across datasets.
