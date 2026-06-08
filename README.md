# NYC 311 Service Requests — Data Science Assignment
**Thalyann Olivo**

Analysis of 21 million NYC 311 service requests from 2020 to 2026, sourced from the [NYC OpenData API](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9).

## Start Here

**Open [`EDA.ipynb`](EDA.ipynb)** — this is the primary analysis notebook. It covers:

- Top complaint types and borough-level request volume
- Average resolution time by agency (before and after data cleaning)
- Seasonal patterns in complaint types
- Data quality investigation: status/closed_date inconsistencies and corrupt OLE Automation dates
- Statistical comparison of resolution times (Welch's t-test, Cohen's d, Bonferroni correction)
- Agency deep-dives: TLC vehicle complaints, DOT street conditions, DOB construction
- SQL integration with DuckDB and SQLite

## Other Files

| File | Description |
|------|-------------|
| `Data-Extraction.ipynb` | Fetches data from the Socrata API and converts CSVs to parquet by borough |
| `nyc311_by_borough/` | Parquet files split by borough (excludes UNKNOWN and UNSPECIFIED) |
| `nyc311_complaints.db` | SQLite database with agency/borough summary table |

## Requirements

```
pandas
numpy
matplotlib
scipy
duckdb
pyarrow
sqlite3
```
