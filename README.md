# COVID-19 Excess Deaths Trend Analysis — Nigeria

**Author:** David Solomon  
**Date:** 2025-10-09  
**Language:** Python (Pandas, Matplotlib, Seaborn, Statsmodels)  
**Dataset:** Our World in Data — Excess Deaths Dataset

---

## 📘 Project Overview
This notebook analyzes COVID-19–related excess-death trends using publicly available data.
The goal is to explore how cumulative excess deaths per 100,000 people evolved over time in Nigeria and compare them with other African countries.

---

## 🧩 Steps in the Analysis
1. **Data Loading:** Imported OWID excess-death dataset (local CSV).  
2. **Inspection & Cleaning:** Renamed long columns, converted dates, handled missing values.  
3. **Exploration:** Filtered Nigeria’s records, created summary tables.  
4. **Visualization:**  
   - Line chart of cumulative excess deaths (with 95 % CI).  
   - Multi-country comparison (Nigeria, Ghana, Kenya, South Africa).  
5. **Forecasting:** Simple 30-day projection using Exponential Smoothing.  
6. **Saving Outputs:** Exported cleaned data and saved final chart image.  

---

## 📊 Key Findings
- Excess deaths increased steadily through 2020–2022, then leveled off.  
- Nigeria shows lower cumulative excess-death rate per 100 k compared with some neighboring countries.  
- Rolling averages smooth short-term fluctuations, highlighting long-term trends.

---

## 📁 Files in This Repository
| File | Description |
|------|--------------|
| `covid_excess_trend.ipynb` | Main Jupyter notebook |
| `nigeria_excess_deaths_clean.csv` | Cleaned subset of dataset |
| `nigeria_excess_deaths_trend.png` | Visualization of excess-death trend |
| `requirements.txt` | Python dependencies |
| `README.md` | This documentation file |

---

## ⚙️ How to Run
```bash
# create venv and install requirements
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt

# launch JupyterLab
jupyter lab
