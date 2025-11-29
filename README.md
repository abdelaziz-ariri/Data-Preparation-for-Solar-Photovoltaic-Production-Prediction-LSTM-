# 📘 Data Preparation for Solar Photovoltaic Production Prediction (LSTM)

## 📝 Project Overview
This project focuses on preparing photovoltaic (PV) solar production data for use in predictive models, specifically **Long Short-Term Memory (LSTM)** neural networks.  
The dataset spans **2019–2024** with measurements recorded every **5 minutes**. The objective is to clean, filter, and transform the raw data into a structured format suitable for deep learning time-series forecasting.

## 🎯 Objective
Prepare high-quality time-series datasets for LSTM-based solar energy production prediction by performing:
- Data cleaning  
- Outlier detection (with DBSCAN)  
- Feature engineering  
- Normalization  
- Dataset splitting  
- Reshaping into `(samples, sequence_length, features)` format

## 📂 Dataset Description
- Time period: **2019 → 2024**  
- Sampling frequency: **every 5 minutes**  
- Focus variables:
  - **Global Horizontal Irradiance (GHI)**
  - **Active Power**
- Only measurements **between sunrise and sunset** are considered (night data removed).

## 🛠️ Project Workflow

### 1. Data Cleaning
- Handle missing values (NaN)  
- Correct inconsistent or erroneous values  
- Detect & treat outliers:
  - Univariate outliers  
  - Multivariate outliers using **DBSCAN** on `GHI` and `Active_Power`

### 2. Data Enrichment
Add relevant contextual information if useful (e.g., time-based features such as hour, day-of-year, solar zenith angle).

### 3. Data Normalization
Apply scaling techniques (MinMax or StandardScaler) depending on model requirements.

### 4. Feature Engineering
Select and create meaningful variables needed for solar production forecasting (e.g., lag features, rolling statistics, clear-sky index).

### 5. Data Splitting
Data is separated chronologically into:

| Set         | Years       |
|-------------|-------------|
| **Train**   | 2019 — 2020 |
| **Validation** | 2021      |
| **Test**    | 2023        |


