# DataThon — Dynamic Supply Chain & Logistics

This repository contains our final solution for the **2025 SUDATA × SUBAA Datathon**.

## 📂 Contents
- `hachathon.Rmd` — Main RMarkdown notebook with full analysis, forecasting, and accuracy evaluation.
- `dynamic_supply_chain_logistics_dataset.csv/` — Saved cleaned datasets (CSV).

## 🚀 How to Run

### 1. Prerequisites
Make sure you have **R (≥ 4.2)** and RStudio (optional).  
Install the following R packages:

```r
install.packages(c(
  "readr","dplyr","tidyr","stringr","lubridate","ggplot2",
  "naniar","visdat","corrplot","hexbin","zoo",
  "tsibble","fable","fabletools"
))

And Run

3. Project Workflow

The notebook is structured as follows:
	1.	Data Loading & Cleaning — handles missing values and prepares features.
	2.	Exploratory Data Analysis (EDA) — visual insights (costs vs congestion, risk class distributions, correlations).
	3.	Feature Engineering — time aggregations (daily, weekly, rolling averages).
	4.	Hierarchical Forecasting — using ETS with reconciliation methods (Bottom-Up, OLS, WLS).
	5.	Evaluation — accuracy metrics (RMSE, MAPE, sMAPE, WAPE, CV backtesting).
	6.	Business Insight — coherence checks and potential savings from improved forecasts.
	7.	Artifacts Export — cleaned data + results are written to CSV for easy sharing.

4. Reproducibility
	•	All random processes use set.seed(42).
	•	Missing values are filled consistently (zero for additive costs).
	•	Safe metrics wrapper prevents infinite MAPE errors.
