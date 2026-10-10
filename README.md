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
| `covid_trend.ipynb` | Main Jupyter notebook |
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

```

Open `covid_trend.ipynb` with the repository root as the working directory and run cells in order from a fresh kernel. The notebook reads the committed `owid-covid-data.csv`; the filename is generic, while the code expects excess-death columns (`Entity`, `Day`, and estimate/bound columns).

## Reproducibility and interpretation

Existing charts and exported CSVs are historical outputs. Re-run and inspect the analysis before quoting the findings above. The forecast is exploratory and assumes an appropriate regular daily series; check date spacing and missing observations first. The final save cell calls `plt.savefig` after `plt.show`, so the saved chart needs visual verification. Running export cells overwrites the tracked CSV and PNG.

`requirements.txt` preserves the original environment snapshot. Its Windows-only packages now have platform markers so they are skipped elsewhere. On PowerShell activation is `.venv\\Scripts\\Activate.ps1`; on macOS/Linux use `source .venv/bin/activate`.
