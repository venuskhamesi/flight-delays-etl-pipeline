🛫 Flight Delays ETL Project – Data Pipeline with Python & SQL

This project simulates a real-world ETL (Extract, Transform, Load) pipeline by processing over a million commercial flight records. The cleaned data is loaded into a MySQL database —ready for further analysis, dashboarding, or machine learning.

---

## 🎯 Project Goals

- 📥 Extract flight delay records from a CSV file using `pandas`  
- 🛠️ Transform the raw data:
  - Parse and convert date strings into `datetime` objects
  - Calculate a new `TotalDelay` field
  - Handle missing values in `DelayReason`
  - Standardize column names and boolean fields  
- 🗃️ Load the cleaned data into a MySQL database using `SQLAlchemy`  
- 🔍 Validate the data structure and confirm successful upload

---

 🧰 Tools & Technologies

- Python: `pandas`, `sqlalchemy`, `mysql-connector-python`  
- Database: MySQL (via Workbench, local instance)  
- Environment: Jupyter Notebook  
- Version Control: GitHub  

---

 📦 Dataset Overview

The dataset contains flight operations and delay information for over 1 million U.S. commercial flights.  

Key features include:  
- `FlightID`, `Airline`, `FlightNumber`, `Origin`, `Destination`  
- `ScheduledDeparture`, `ActualDeparture`, `ScheduledArrival`, `ActualArrival`  
- `DelayMinutes`, `DelayReason`, `Cancelled`, `Diverted`  
- `AircraftType`, `TailNumber`, `Distance`

---

# ETL Process Breakdown

 1. 🟢 Extract  
- Loaded data from a CSV file into a DataFrame  
- Performed initial profiling to understand structure and quality  

2.🛠️ Transform  
- Parsed datetime columns to improve consistency  
- Created a `TotalDelay` column based on actual vs. scheduled arrival times  
- Handled null values in `DelayReason` with `"Unknown"` or imputed categories  
- Cleaned and standardized column names and Boolean fields  

3. 🔵 Load  
- Defined the schema and created a new table `flights` in MySQL  
- Loaded the cleaned dataset using the `SQLAlchemy` engine  
- Verified data through queries in MySQL Workbench  

---

 🗂️ Project Files

