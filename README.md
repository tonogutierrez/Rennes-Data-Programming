# 💧 Water Access & WASH Mortality Analysis

A data analysis project exploring the relationship between safe drinking water access and WASH-related mortality using WHO data.

## 📊 Overview

This project analyzes global water access trends (2000-2022) and their correlation with public health outcomes.

**Key Questions:**
- How has water access evolved globally?
- What are the urban-rural disparities?
- Is there a link between water access and mortality rates?

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/yourusername/water-wash-analysis.git
cd water-wash-analysis
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Run Analysis
```python
# Data processing
python src/data_processing.py

# Generate visualizations  
python src/exploratory_analysis.py
```

## 📁 Project Structure
```
water-wash-analysis/
├── data/                           # WHO datasets
├── src/                           # Analysis code
├── notebooks/                     # Jupyter notebooks  
└── visualizations/               # Output charts
```

## 🔍 Key Findings

### 📈 Global Progress
- Water access improved from **76.5% (2000)** to **88.7% (2022)**
- Consistent annual growth of **~0.6%**

### 🏙️ Urban-Rural Gap
- **Urban**: 94.3% access
- **Rural**: 82.1% access  
- **12.2% difference**

### ⚕️ Health Impact
- **Strong negative correlation** (-0.73) between water access and mortality
- Higher water access = Lower WASH-related deaths

## 📊 Sample Code

```python
# Clean data
def clean_data(df):
    df = df.dropna(how='all')
    df = df.drop_duplicates()
    return df

# Analyze correlation  
correlation = merged['water_pct'].corr(merged['wash_mortality_per_100k'])
print(f"Correlation: {correlation:.3f}")
```

## 📋 Data Sources

- **Water Access**: WHO Global Health Observatory (2000-2022)
- **Mortality**: WHO Mortality Database (2019)

## 🤝 Contributing

Contributions welcome! Feel free to submit issues and pull requests.

---

## 👥 Team Members
[Name 1]

[Name 2]

[Name 3]

[Name 4]



*Using data science to understand global health challenges*
