# IPL Data Analysis using Apache Spark (Databricks)

This project is a hands-on exploratory data analysis of  cricket data using **Apache Spark on Databricks**.  
The goal of this notebook was to understand how large-scale sports data can be processed using Spark SQL, schemas, and distributed transformations.

This was done purely for **learning Spark + Databricks fundamentals**, not for business optimization or production use.

---

## Tech Stack

- Apache Spark (PySpark)
- Databricks Notebook
- Spark SQL
- AWS S3 (data source)
- Python (Matplotlib, Seaborn)
- CSV-based structured datasets

---

## Datasets Used

The data was loaded directly from S3 and includes:

- `Ball_By_Ball.csv` – detailed ball-level match events
- `Match.csv` – match-level metadata
- `Player.csv` – player information
- `Player_Match.csv` – player participation per match

All datasets were read using **explicit Spark schemas** instead of inferSchema.

---

## Project Workflow & What I Learned

### 1. Spark Session Initialization
I started by creating a Spark session inside Databricks to enable distributed processing.

---

### 2. Defining Explicit Schemas
Custom `StructType` schemas were defined for each dataset.

**Why I did this:**
- Avoid schema inference errors
- Improve performance
- Gain better control over data types (Integer, String, Date)

**What I learned:**
- Schema-first design is important for large datasets
- Spark fails fast when schemas don’t align with data

---

### 3. Loading Data from S3
All CSV files were loaded from AWS S3 using Spark’s CSV reader.

**Why:**
- Simulates real-world cloud-based data pipelines
- Helps understand distributed file reading

---

### 4. Registering Temporary Views
Each DataFrame was registered in SQL view.

---

### 5. Analytical Queries Using Spark SQL

I explored multiple cricket-related insights using Spark SQL queries

---

### 6. Visualization
Converted selected Spark DataFrames to Pandas and visualized them using:
- Matplotlib
- Seaborn

---

## Key Learnings

- How Spark handles large datasets differently from Pandas
- Writing production-style schemas in PySpark
- Using Spark SQL for analytical workloads
- When and why to convert Spark DataFrames to Pandas
- End-to-end flow inside Databricks notebooks

---

## Project Nature Disclaimer

This project was done:
- For **self-learning**
- To gain **hands-on Spark + Databricks experience**
- Without focusing on business KPIs or predictive modeling

The analysis is exploratory and educational.

---

## How to Run

1. Upload the notebook to Databricks
2. Ensure access to S3 bucket or replace paths with local data ( " I had bit trouble while setting this up but it was alright once i went through 2-3 tutorials online and visiting documentation ")
3. Run cells sequentially

---

## Tanishq Dahiya (^-^)

Hands-on Spark & Databricks learning project  
Focused on understanding distributed data processing
