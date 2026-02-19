

TOOLS & TEECHNOLOGIES USED:
  1. Python (Pandas, Matplotlib)
  2. Jupyter Notebook
  3. MySQL
  4. SQLAlchemy
  5. CSV Files (Raw Data)


ETL PIPELINE: 

1. EXTRACT

    Loaded all CSV files into Jupyter Notebook using Pandas.

2. TRANSFORM (Data Cleaning & Business Rules)

    Age must be between 0 and 100
   
    Missing gender → assigned as 'U' (Unknown)
  
    Missing dosage or frequency → set to "Not Provided"
  
    Duplicate prescriptions removed
  
    Prescriptions with invalid patient, doctor, or medicine IDs rejected

3. LOAD
   
    Cleaned data inserted into MySQL tables:
  
        patients, doctors, medicines, prescriptions
  
    Database constraints ensure data integrity.
