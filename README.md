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

### A. Descriptive Data Mining (Facts 1–8)
1. **Highest Distribution Efficiency Taluk**: Rank average lifting percentage by taluk to identify the top performer (Nanjangud).
2. **Lowest Distribution Efficiency Taluk**: Identify the worst performing average lifting taluk (urban Mysuru).
3. **Most Stable Taluk**: Find the taluk with the lowest standard deviation in monthly lifting percentage.
4. **Most Fluctuating Taluk**: Find the taluk with the highest standard deviation in monthly lifting percentage.
5. **FPS Workload Ranking**: Rank taluks by ration cards per Fair Price Shop.
6. **eKYC Adoption Ranking**: Rank eKYC coverage percent by taluk.
7. **Rice Allocation Ranking**: Identify the highest rice receiving taluk by total allotted volume.
8. **Ragi-to-Rice Ratio Analysis**: Uncover dietary food preference patterns by comparing Ragi and Rice allotment volumes.

### B. Predictive Mining (Facts 9–12)
9. **Predict Lifting Percentage**: Fit a Linear Regression model to identify which factors influence the lifting percentage most.
10. **Predict High vs. Low Performing Taluk**: Train a Decision Tree classifier to discover rules that predict high-lifting performance.
11. **Forecast Next Month Lifting %**: Model time-series trends to forecast next month's district-wide lifting percentage.
12. **Predict Commodity Requirement**: Use time-series forecasting to estimate next month's rice demand for the district.

### C. Clustering Mining (Facts 13–16)
13. **K-Means Taluk Segmentation**: Cluster taluks into High, Medium, and Low Performance categories.
14. **Beneficiary Density Clusters**: Group taluks based on Cards, Members, and active FPS counts.
15. **Digital Adoption Clusters**: Group taluks based on digital adoption metrics (eKYC % and Lifting %).
16. **Commodity Consumption Clusters**: Group taluks based on Rice and Ragi allocation profiles.

### D. Association Rule Mining (Facts 17–20)
17. **High eKYC ⇒ High Lifting**: Discover the strength of the association rule `High_eKYC -> High_Lifting` using Apriori.
18. **High FPS Density ⇒ High Efficiency**: Discover the strength of the association rule `Low_Workload -> High_Lifting` (High FPS density means low workload).
19. **Rural Taluk ⇒ High Participation**: Discover the strength of the association rule `Rural_Taluk -> High_Card_Utilization`.
20. **High Rice Allocation ⇒ High Member Participation**: Discover the strength of the association rule `High_Rice_Allocation -> High_Members_Taken`.

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
