# WHO Water & WASH – Analysis

## About the Project
This is a project for the course **Programming for Data Analytics** at **Rennes School of Business**. It analyzes the factors related to **safe drinking-water coverage** and its association with **WASH-related mortality** using two official WHO datasets (`1548EA3_ALL_LATEST.csv` and `ED50112_ALL_LATEST.csv`). By employing **descriptive analytics**, **exploratory data analysis (EDA)**, and **baseline predictive modeling**, we identify key patterns that influence coverage (global trends, urban–rural gaps, gender differences) and quantify the 2019 relationship between water access and WASH mortality. We also build simple linear models to forecast coverage for **2025** and **2030**.

Our approach includes visualizing distributions, examining correlations, and building lightweight forecasts to highlight where targeted interventions can have the greatest impact.

**Research question:** 
*1. How has access to safe drinking water evolved globally (2000-2022)?
2. Which countries have the highest mortality rates from unsafe WASH?
3. Is there a correlation between access to water and mortality?
4. Are there significant differences by gender and urbanization?*

---

## Datasets
- **`1548EA3_ALL_LATEST.csv`** – % population with **safe drinking water**, by `GLOBAL/REGION/COUNTRY` and **urbanization** (`URBAN/RURAL/TOTAL`), ~2000–2022.
- **`ED50112_ALL_LATEST.csv`** – **WASH mortality** (deaths per 100k), by geography and **sex** (`FEMALE/MALE/TOTAL`). We focus on **2019** for cross-section comparability.

## Folder Structure
```
FinalProject/
├── venv/ # local virtual environment (not tracked in git if .gitignore is set)
├── .gitignore
├── 1548EA3_ALL_LATEST.csv # WHO – Safe drinking-water coverage (%)
├── ED50112_ALL_LATEST.csv # WHO – WASH mortality (deaths per 100k)
├── FinalProject.ipynb # main notebook (cleaning, EDA, correlation, forecasts)
└── README.md
```
## Install dependencies
- pip install -U pip
- pip install pandas numpy matplotlib seaborn scikit-learn

## What the Notebook Does
# 1 Cleaning and Standardization
- Drop empty rows/duplicate, normalize numeric types
- Map WHO columns to a consisten schema:
    - Water -> country, year, geo_type, urbanization, water_pct
    - Mortality -> country, year, geo_type, sex, wash_mortality_per_100k

# 2 EDA and Key Visuals
- Global coverage tren
- Urban vs rural levels and evolution
- Top/Bottom countries
- Gender comparison (2019)

# 3 Correlation
- Country level water with 2019 mortality

# 4 Country Classification and Forecasts
- Classify by latest coverage: LEADER / ON_TRACK / MODERATE / LAGGING.
- Simple linear regression per country to forecast 2025/2030 (clipped to [0,100]) and estimate     annual change (slope)

## Team Members
- [@tonogutierrez](https://github.com/tonogutierrez)
- [@zhngsimin-cloud](https://github.com/zhngsimin-cloud)
- [@OHHO-ZHANG](https://github.com/OHHO-ZHANG)
- [@nancyhed-ui](https://github.com/nancyhed-ui)
- [@Chrristy](https://github.com/Chrristy)


