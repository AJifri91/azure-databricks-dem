# Tech Layoffs 2026 – Data Pipeline Project

## Problem Statement
Analyse the wave of tech layoffs in Q1 2026. Identify which sectors, regions, and companies were most affected, and whether AI was cited as a reason. The pipeline ingests, cleans, and transforms the data, then visualises key trends.

## Tools Used
- **Cloud:** Microsoft Azure  
- **Data Platform:** Azure Databricks (Apache Spark)  
- **Languages:** Python (PySpark), SQL  
- **Data Source:** Public layoffs tracker (CSV from Kaggle)

## Data Source
The file `tech_layoffs_2026_tracker.csv` contains layoff events with columns: company, date, jobs cut, percentage, sector, country, AI cited, etc.

## Pipeline Steps
1. **Ingest:** Load CSV from DBFS (or public URL) into Spark DataFrame.
2. **Clean:** Convert data types, handle missing values, standardise strings.
3. **Transform:** Aggregate by sector, region, month; compute totals and percentages.
4. **Output:** Generate summary tables and visualisations; save cleaned data as Delta table.

## How to Run
1. Upload the CSV to your Databricks workspace (DBFS or mount Azure Blob).
2. Import the notebook `notebooks/layoffs_analysis.ipynb` into Databricks.
3. Attach it to a running cluster (use single node for simplicity).
4. Run all cells.
