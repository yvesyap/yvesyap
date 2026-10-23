<h1 align="center">Hi, I'm Yang Yi (Yves)</h1>
<p align="center">
  <b>Final year · BSc (Hons) Computer Science (Data Science)</b><br/>
  Multimedia University, Cyberjaya · Graduating 2027
</p>
<p align="center">
  I work with messy, real-world datasets, cleaning them, modelling them, and turning the results into something a business can actually use.<br/>
  Now moving towards ML engineering, with a focus on MLOps: deploying, monitoring and maintaining models after they are trained.
</p>
<p align="center">
  <a href="https://www.linkedin.com/in/yang-yi-yap-2b3125284/">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:yvesyyy18@gmail.com">
    <img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

## Tech Stack

### Languages & Data
<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white" />
</p>

### Databases
<p>
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
</p>

### Tools
<p>
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white" />
</p>

### Currently Learning
<p>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Apache%20Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/XGBoost-337AB7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/LightGBM-02A8EF?style=for-the-badge" />
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=for-the-badge&logo=pytest&logoColor=white" />
</p>

---

## Currently Building

### End to End MLOps Pipeline for Transaction Fraud Detection
> Final Year Project · Python · MLOps · Machine Learning · **In progress**

A deployed fraud model loses accuracy as fraud patterns change. This project automates the maintenance loop: it validates incoming data, monitors drift, retrains the model automatically, promotes a new version only when it is clearly better, and rolls back when something goes wrong.

**Planned pipeline:**
- Replay transactions in time order and quarantine invalid records
- Train, version and serve a baseline gradient boosting model through a containerised API
- Monitor input and prediction drift, and retrain automatically when drift is detected
- Promote a candidate model only if it beats the live model, with automatic rollback
- Evaluate against a model that is never updated, using injected drift scenarios

**Planned stack:** Python, XGBoost, LightGBM, MLflow, FastAPI, Docker, GitHub Actions

Dataset: [IEEE-CIS Fraud Detection, Kaggle](https://www.kaggle.com/c/ieee-fraud-detection)

<a href="https://github.com/yvesyap/mlops-fraud-drift-pipeline">
  <img src="https://img.shields.io/badge/GitHub-View%20Repository-181717?style=for-the-badge&logo=github&logoColor=white" />
</a>

---

## Projects

### Shopee Malaysia: Demand & Price Elasticity Analysis
> R · Statistical Analysis · Regression · **Completed**

Analysed 20,000+ Shopee Malaysia transactions across 8 product categories to investigate whether price drives sales volume.

**Key findings:**
- Sales volume CV = **217.99**, Price CV = **266.77**, a highly volatile marketplace with extreme right-skewed distributions
- On the raw scale the linear relationship is negligible: Pearson **r = −0.086**, explaining under **1%** of variance in sales volume
- A **log–log transformation** recovered the underlying elasticity, lifting R² to approximately **65%**
- **Conclusion:** the price and volume relationship is multiplicative rather than linear, so linear correlation alone materially understates price sensitivity on this marketplace

Built a custom R text-parsing pipeline to extract geographic seller metadata from unstructured fields.

Dataset: [Shopee Sales Data, Apr to May 2023, Kaggle](https://www.kaggle.com/datasets/yoongsin/shopee-sample-data)

---

### Global Sustainable Energy: Cross-National Analysis (2000–2020)
> Python · Pandas · Seaborn · Scikit-learn · SciPy · **Completed**

End-to-end data science pipeline analysing 3,649 observations across 176 countries and 21 years to investigate how economic development and energy consumption patterns influence renewable energy adoption and CO₂ emissions globally.

**Pipeline:**
- Data cleaning: standardised 21 columns (including embedded-newline fix), IQR outlier inspection, pairwise missing-value handling
- EDA: univariate distributions, bivariate trend analysis, regional comparisons

**Four analytical questions (distinct techniques):**
- **Q1 Correlation:** Pearson (*r* = −0.371) and Spearman (*ρ* = −0.651) correlation between GDP per capita and renewable energy share, both significant at *p* < 0.0001. The relationship is monotonic but non-linear
- **Q2 Regression:** Multiple linear regression modelling CO₂ emissions from renewable capacity and energy intensity
- **Q3 Clustering:** K-Means segmentation of countries by energy access, renewable share, and emissions profile
- **Q4 Classification:** Decision Tree / Random Forest classifying countries by electricity access level from economic and energy indicators

**Key insight:** The negative correlation between GDP and renewable share is driven by a biomass accounting effect. Lower income countries report high renewable shares due to traditional biomass reliance, not modern clean energy adoption.

Dataset: [Global Data on Sustainable Energy, Kaggle (CC0)](https://www.kaggle.com/datasets/anshtanwar/global-data-on-sustainable-energy)

---

## Certifications & Awards

| Certification / Award | Year |
|-----------------------|------|
| Huawei ICT Competition 2023–2024 APAC, National Phase (Computing Track) | 2024 |
| HCIA-openGauss V1.0, Huawei Certified ICT Associate | 2024 |
| Huawei Data Management and Analytics Course Certificate | 2024 |
| Dean's List, Foundation in IT, Nov 2023 Trimester (GPA: 3.89) | 2023 |
