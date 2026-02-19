# Digital_Prescription_Record_Analysis

Digital Prescription Record Analysis is a Healthcare Informatics project designed to digitize, clean, validate, store, and analyze medical prescription records.

The system implements an automated ETL pipeline using Python and stores structured, validated data in MySQL for analytical querying and visualization.

---

## Project Overview
In this project:

- Raw CSV files are loaded using Python (Pandas)
- Data cleaning and validation are performed using defined business rules
- Clean data is inserted into MySQL tables
- SQL queries are used to perform analytical operations
- Matplotlib is used to generate visual dashboards
This project demonstrates an end-to-end ETL and analytics workflow.
---
## Dataset

The project uses the following CSV files:

- `doctors_1000.csv` – Doctor master data
- `medicines_1000.csv` – Medicine catalog
- `patients_1000.csv` – Patient demographics
- `prescriptions_1000.csv` – Prescription transactions
---
## Business Rules Implemented
- Age must be between 0 and 100
- Duplicate prescriptions are removed
- Prescriptions without valid patient or doctor are rejected
- Missing dosage or frequency is replaced with "Not Provided"
- Unknown gender is marked as "U"
---
## System Architecture

```text
Raw CSV Files
        ↓
Python ETL (Pandas)
    • Deduplication
    • Null Handling
    • Business Rule Validation
        ↓
MySQL Database
    • Clean Tables
    • Constraints Applied
        ↓
SQL Analytics
        ↓
Matplotlib
```
---
## Tech Stack

| Technology | Usage |
|------------|-------|
| Python | ETL Processing |
| Pandas | Data Cleaning & Transformation |
| MySQL | Relational Data Storage |
| SQL | Analytical Queries |
| Matplotlib | Data Visualization |
---
## ETL PIPELINE

1. EXTRACT

    - Loaded all CSV files into Jupyter Notebook using Pandas.

2. TRANSFORM (Data Cleaning & Business Rules)

    - Age must be between 0 and 100
   
    - Missing gender → assigned as 'U' (Unknown)
  
    - Missing dosage or frequency → set to "Not Provided"
  
    - Duplicate prescriptions removed
  
    - Prescriptions with invalid patient, doctor, or medicine IDs rejected

3. LOAD
   
   Cleaned data inserted into MySQL tables:
  
        patients, doctors, medicines, prescriptions
  
    Database constraints ensure data integrity.
---
## Business Insights Generated
- Most frequently prescribed medicines
- Doctor-wise prescription volume comparison
- Gender-wise prescription distribution
- Age group vs number of prescriptions
- Detect doctors issuing unusually high prescriptions
- Daily prescription trend over time
- Data quality comparison (before vs after cleaning)
---
## Sample Outputs
