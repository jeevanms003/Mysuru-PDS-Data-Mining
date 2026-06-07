# Mysuru PDS Ration Distribution Data Mining & Analysis

A data mining and statistical analysis project evaluating the efficiency, workload, demographics, and trends of the Aadhaar-enabled Public Distribution System (AePDS) in the Mysuru district, Karnataka, India.

This repository contains a real-world, monthly taluk-level PDS distribution dataset scraped directly from the official portal of the Department of Food, Civil Supplies & Consumer Affairs, Government of Karnataka (`https://ahara.karnataka.gov.in/`), along with a comprehensive Jupyter Notebook discovering 15 data mining facts and visualizations.

---

## 📂 Repository Contents

* **`mysuru_ration_dataset.csv`**: A structured database of PDS transactions for the last 12 months (**June 2025 – May 2026**). It records monthly metrics for all **9 taluks** of Mysuru across **4 core commodities** (Rice, Wheat, Sugar, Ragi).
* **`mysuru_ration_analysis.ipynb`**: A Jupyter Notebook executing data loading, statistical mining, correlation plotting, outlier detection, and rendering 15 visual insights using `pandas`, `seaborn`, `matplotlib`, and `scipy`.

---

## 📊 20 Advanced Data Mining Insights & Findings

The analysis notebook investigates the Mysuru PDS ration distribution network across four main pillars of data mining:

### A. Descriptive Data Mining (What the historical data shows)
1. **Taluk Distribution Efficiency**: Ranks taluks by average ration lifting percentage (highest in Nanjangud, lowest in urban Mysuru).
2. **Fair Price Shop (FPS) Workload Density**: Measures ration card density per shop (urban Mysuru has a high workload of 900+ cards/shop).
3. **Active Card Utilization Rate**: Percent of registered cardholders who collect rations monthly (uncovering non-claim rates in urban sectors).
4. **Member-level eKYC Verification Rate**: Tracks biometric Aadhaar validation compliance among active card members (exceeding 98.8% compliance district-wide).
5. **Staple Foodgrain Allotment Trends**: Time-series comparison tracking monthly allotments of staples (Rice vs. Ragi).
6. **Correlation Analysis**: A statistical correlation matrix correlating active shops, card volumes, member counts, and allotted quantities.
7. **eKYC Pending Backlog Map**: Maps the absolute count of active beneficiaries with pending eKYC updates to identify target validation zones.
8. **Regional Staple Preference (Ragi-to-Rice Ratio)**: Tracks dietary patterns showing higher Ragi preference in rural taluks like Hunsur and H.D. Kote.
9. **Seasonality in Lifting Success Rate**: Tracks monthly transaction success rate shifts across Monsoons and festival seasons.
10. **Grain Load Distributed per Active Card**: Measures the average grain load (in Quintals) distributed per active cardholder monthly.

### B. Predictive Data Mining (Forecasting and classification)
11. **Lifting Percentage Prediction (Linear Regression)**: Predicts ration lifting success based on features like active FPS, cards, and biometric eKYC rates.
12. **NFSA Grain Allotment Forecasting (Random Forest)**: Forecasts monthly allotment volumes utilizing an ensemble decision forest regressor.
13. **High/Low Performance Segment Classification (Decision Tree)**: Classifies taluk-month performances and extracts administrative workload splitting criteria.
14. **District-wide Monthly Allotment Forecasting (Time-Series)**: Uses rolling moving average trends to predict next-cycle NFSA grain footprint requirements.

### C. Clustering Data Mining (Grouping multi-dimensional performance patterns)
15. **Taluk Performance Clustering (K-Means)**: Groups the 9 taluks into 3 clusters (High, Medium, Low Performers) based on administrative efficiency and workload metrics.
16. **Optimal Cluster Count Selection (Elbow Method)**: Evaluates Within-Cluster Sum of Squares (WCSS) to statistically verify cluster groupings.
17. **Cluster Visualization (PCA Dimensionality Reduction)**: Uses Principal Component Analysis to visualize taluk clusters in a 2D space, highlighting urban performance outliers.

### D. Association Rule Mining (Finding behavioral patterns and correlations)
18. **PDS Indicator Rule Generation (Apriori)**: Discovers strong behavioral rules between discretised features like `{High_eKYC} -> {High_Lifting}`.
19. **Association Metric Validation (Support vs. Confidence vs. Lift)**: Validates rules using Support, Confidence, and Lift metric plots.
20. **FP-Growth vs. Apriori Execution Comparison**: Compares rule consistency and execution performance, demonstrating the speedup of FP-Growth for PDS scale-up.

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
