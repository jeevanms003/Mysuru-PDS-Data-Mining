# Mysuru PDS Ration Distribution Data Mining & Analysis

A data mining and statistical analysis project evaluating the efficiency, workload, demographics, and trends of the Aadhaar-enabled Public Distribution System (AePDS) in the Mysuru district, Karnataka, India.

This repository contains a real-world, monthly taluk-level PDS distribution dataset scraped directly from the official portal of the Department of Food, Civil Supplies & Consumer Affairs, Government of Karnataka (`https://ahara.karnataka.gov.in/`), along with a comprehensive Jupyter Notebook discovering 15 data mining facts and visualizations.

---

## 📂 Repository Contents

* **`mysuru_ration_dataset.csv`**: A structured database of PDS transactions for the last 12 months (**June 2025 – May 2026**). It records monthly metrics for all **9 taluks** of Mysuru across **4 core commodities** (Rice, Wheat, Sugar, Ragi).
* **`mysuru_ration_analysis.ipynb`**: A Jupyter Notebook executing data loading, statistical mining, correlation plotting, outlier detection, and rendering 15 visual insights using `pandas`, `seaborn`, `matplotlib`, and `scipy`.

---

## 📊 15 Data Mining Insights & Findings

The analysis notebook investigates the following key trends in the Mysuru distribution network:

1. **Taluk Distribution Efficiency**: Ranks taluks by average ration lifting percentage (highest in Saraguru, lowest in urban Mysuru).
2. **Fair Price Shop (FPS) Workload**: Measures ration card density per shop (Mysuru urban has a massive workload of 900+ cards/shop).
3. **Active Card Utilization Rate**: Percent of registered cardholders who collect rations monthly (uncovering ~40% non-claim rates in urban sectors).
4. **Member-level eKYC Verification Rate**: Tracks biometric Aadhaar validation compliance among active card members (>98.8% compliance district-wide).
5. **Staple foodgrain Allotment Trends**: Time-series comparison tracking monthly allotments of staples (Rice vs Ragi).
6. **Correlation Analysis**: A statistical correlation matrix correlating active shops, card volumes, member counts, and allotted quantities.
7. **eKYC Pending Backlog**: Maps the absolute count of active beneficiaries with pending eKYC updates to identify target validation zones.
8. **Regional Staple Preference (Ragi-to-Rice Ratio)**: Tracks dietary patterns showing higher ragi preference in rural taluks like Hunsur and H.D. Kote.
9. **Seasonality in Lifting success rate**: Tracks monthly transaction success rate shifts across seasons.
10. **Grain Volume per Active Card**: Measures the average grain load (in Quintals) distributed per active cardholder monthly.
11. **Average Family Size**: Serves as a demographic proxy measuring average members per active card.
12. **Statistical Outlier Detection**: Flags month-taluk combinations with unusually high or low allotments using Z-score calculation.
13. **Stability of PDS Distribution (Variance)**: Evaluates network reliability using standard deviation of monthly lifting rates.
14. **Active Shop Trends**: Visualizes active shop counts month-wise to track expansion or closures.
15. **Combined Foodgrain Footprint**: Aggregates the combined monthly foodgrain footprint (Rice + Ragi + Wheat + Sugar) for the entire district.

---

## ⚙️ Setup and Installation

### Prerequisites
Make sure you have Python 3.8+ installed along with the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scipy notebook
```

### Running the Analysis
1. Clone the repository:
   ```bash
   git clone https://github.com/jeevanms003/Data-Mining-Event.git
   cd Data-Mining-Event
   ```
2. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Run `mysuru_ration_analysis.ipynb` to execute the cells and display the plots.

---

## 🏛️ Data Source
All data is sourced from the official Food Civil Supplies and Consumer Affairs Department, Government of Karnataka:
* **Portal**: [Karnataka Ahara Office Statistics](https://ahara.karnataka.gov.in/fcs_office_statistics/)
* **Target Endpoint**: `Stat_Ration_Taken_Details.aspx?code=1522` (District Code 1522: Mysuru)
