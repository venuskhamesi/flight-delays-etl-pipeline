# ✈️ Flight Delays ETL Project

## 📌 Project Overview  
This project simulates a real-world **data engineering workflow** by performing an ETL (Extract, Transform, Load) process on a large dataset containing commercial flight records. The goal is to **read, clean, and enhance the data**, then load it into a **MySQL database** for future querying and analysis.

---

## 🎯 Objectives  
- 📥 **Extract**: Load flight delay data from a CSV file using `pandas`.  
- 🔧 **Transform**:  
  - Convert date strings to `datetime` format.  
  - Create a new `TotalDelay` column.  
  - Handle missing values in the `DelayReason` column.  
  - Standardize column formatting.  
- 🗄️ **Load**: Insert cleaned data into a MySQL database using `SQLAlchemy`.  
- ✅ **Validate**: Confirm successful data insertion and structure.

---

## 🧰 Tools & Technologies  
- **Python**: `pandas`, `sqlalchemy`, `mysql-connector-python`  
- **Jupyter Notebook**  
- **MySQL Workbench** (local instance)  
- **GitHub** for version control

---

## 📊 Dataset Description  
Over 1 million commercial flight records including delays, cancellations, aircraft types, and airport info.  
**Key columns include**:
- `FlightID`, `Airline`, `FlightNumber`, `Origin`, `Destination`  
- `ScheduledDeparture`, `ActualDeparture`, `ScheduledArrival`, `ActualArrival`  
- `DelayMinutes`, `DelayReason`, `Cancelled`, `Diverted`  
- `AircraftType`, `TailNumber`, `Distance`

---

## 🔄 ETL Process Breakdown  

### 🟢 1. Extract  
- Loaded the CSV into a DataFrame using `pandas`  
- Ran initial data exploration and profiling  

### 🟡 2. Transform  
- Converted datetime strings to `datetime` objects  
- Created a new column `TotalDelay` (difference in scheduled vs actual arrival)  
- Replaced nulls in `DelayReason` with `"Unknown"` or other imputed values  
- Standardized Boolean columns and fixed formatting  

### 🔵 3. Load  
- Created a new table `flights` in MySQL  
- Inserted the cleaned dataset using SQLAlchemy engine  
- Verified data via MySQL Workbench queries  

---

## 📂 Project Structure
├── flight_delay_ETL.ipynb
├── Flight_delays_SQL.sql
├── ERD Flight_data.mwb
├── README.md

---

## ✅ Conclusion  
This ETL project successfully demonstrates a complete data pipeline using Python and SQL: from extracting and transforming over 1 million commercial flight records to loading them into a structured SQL database. The cleaned dataset is now ready for use in downstream applications like business reporting, dashboards, or predictive modeling—making it an ideal portfolio piece for aspiring data engineers and analysts.

---

## 💼 Author  
**Venus Khamesi (GitHub: [venuskhamesi])**  
Aspiring Data Analyst & Business Analyst | Python • SQL • ETL • MySQL  
