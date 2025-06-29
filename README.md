# Assignment-6
## NSE All Share Index 
This project supports the backend data pipeline for a fintech platform providing insights to Nigerian retail investors.
i built a robust ingestion, cleaning, and transformation pipeline to power dashboards and analytics on historical stock index data from NSE.
The final output includes a ready-to-use SQL table and queries for key performance indicators (KPIs) relevant to financial analysis.
## Data Ingestion & Storage
Source file: CSV format (historical daily prices and volumes)
Ingestion tools: Python (Pandas) for preprocessing
Target storage: SQL database(postgreesql)
##  Data Cleaning & Transformation
Columns cleaned:
Removed commas from numeric fields (e.g., prices).
Converted Change % to float and normalized (e.g., "1.25%" → 0.0125).
Parsed Vol. field, converting M (millions) and B (billions) to numeric values.
Converted Date column to proper datetime format and renamed to trade_date.
Dropped rows with invalid or missing dates.
## Challenges Faced
Incorrect or mixed data formats in the CSV file:
Extra commas and special characters in numeric fields.
Inconsistent volume notation ("M", "B", empty).
Some rows failing date parsing, leading to empty datasets if not carefully handled.
Ensuring that no accidental conversion of columns to lists occurred, which caused errors with Pandas string functions (.str, .astype).


