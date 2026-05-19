# NZ Stats Portfolio

Portfolio project analyzing New Zealand statistics data (labour, population, housing) using Excel, Python, and Power BI.

## 📊 Project Overview

This portfolio demonstrates end-to-end data analytics workflows:
- **Data Sources**: Stats NZ open data
- **Processing**: Excel Power Query, Python pandas
- **Visualization**: Power BI dashboards
- **Documentation**: Complete technical documentation

## 📁 Project Structure

```
nz-stats-portfolio/
├── README.md                    # Project overview, data sources, tech stack
├── .gitignore
├── LICENSE
│
├── 01_raw_data/                 # Original Stats NZ & other CSVs
│   ├── labour_raw/
│   ├── population_raw/
│   └── housing_raw/
│
├── 02_cleaned_data/             # Output from Excel + Power Query
│   ├── labour_cleaned.xlsx
│   └── labour_output/
│       └── LabourByRegionQuarter.csv
│
├── 03_python_pandas/            # Python cleaning / feature‑engineering
│   ├── notebook/
│       └── 01_population_demo_analysis.ipynb
│   ├── scripts/
│       └── process_population_data.py
│   ├── data/
│       ├── raw_population.csv
│       └── output_regional_demographics.csv
│
├── 04_power_bi/                 # Power BI model + reports
│   ├── pbix_files/
│       └── HawkeBay_Housing_Workforce_Dashboard.pbix
│   ├── documentation/
│       └── data_model_spec.md
│
├── 05_docs/                     # Portfolio docs
│   ├── project_plan.md
│   ├── tech_stack.md
│   └── how_to_run.md
│
└── 06_assets/                   # Logos, screenshots for README
    └── dashboard_screenshots/
```

See each folder for more detail.

---

## Technologies used

- **Data Ingestion & Cleaning**:
  - Excel + Power Query (for labour‑force data).
- **Data Transformation & Feature Engineering**:
  - Python + Pandas (for population estimates and derived indicators).
- **Visualisation & Reporting**:
  - Power BI (multi‑page dashboard tying labour, population, and housing data together).

---

## Steps to reproduce

1. **Excel + Power Query layer (`02_cleaned_data/`)**  
   - Open `02_cleaned_data/labour_cleaned.xlsx`.  
   - Refresh all Power Query queries to re‑run the cleaning pipeline.  
   - Export the main table (e.g., `LabourByRegionQuarter`) as a CSV if needed.

2. **Python + Pandas layer (`03_python_pandas/`)**  
   - Ensure dependencies are installed:
     ```bash
     pip install pandas numpy
     ```
   - Run the processing script:
     ```bash
     python 03_python_pandas/scripts/process_population_data.py
     ```
   - This reads raw population data from `03_python_pandas/data/raw_population.csv` and outputs a cleaned demographics table (`output_regional_demographics.csv`) for use in Power BI.

3. **Power BI layer (`04_power_bi/`)**  
   - Open `04_power_bi/pbix_files/HawkeBay_Housing_Workforce_Dashboard.pbix`.  
   - Update data source paths if you placed CSVs in a different location.  
   - Refresh the model to see updated labour, population, and housing metrics.

---

## Data sources

- **Labour market data**:  
  Stats NZ Household Labour Force Survey – Labour force status by region (Infoshare / CSV tables).  
  - [Stats NZ Labour market](https://www.stats.govt.nz/topics/labour-market/)

- **Population estimates & projections**:  
  Stats NZ Estimated Resident Population (ERP) by region, age, sex, and ethnic group.  
  - [Stats NZ Population estimates](https://www.stats.govt.nz/information-releases/national-population-estimates/)

- **Housing / dwelling data**:  
  Dwelling counts and housing‑related statistics via Stats NZ "Large datasets" and related housing‑partners (e.g., Kāinga Ora or HUD Local Housing Statistics where used).  
  - [Kāinga Ora housing statistics](https://kaingaora.govt.nz/en_NZ/publications/oia-and-proactive-releases/housing-statistics/)
  - [HUD Local Housing Statistics](https://www.hud.govt.nz/stats-and-insights/local-housing-statistics/)

All datasets are free, open‑use, and credited to their respective New Zealand agencies.

---

## How to cite this project

This is a personal learning project built on **public‑sector data**. Credit the original data providers (Stats NZ, Kāinga Ora, HUD, etc.) when sharing results.

---

## License

This repository is for learning and portfolio purposes. You may reuse the code patterns and structure, but please respect the licensing of the original data providers.

See `LICENSE` file for details.
