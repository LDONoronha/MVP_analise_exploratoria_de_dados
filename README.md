# MVP: Exploratory Data Analysis and Preprocessing of Air Quality and Health Data

## 📌 Project Description

This project is part of the development of a **Minimum Viable Product (MVP)** focused on exploratory data analysis and data preprocessing. It investigates the relationship between **air quality** and **public health indicators**, particularly hospital admissions due to respiratory diseases.

The dataset used — *Air Quality Health Dataset* — was sourced from Kaggle and contains environmental and hospitalisation records from various cities around the world. Variables include pollutant levels such as PM2.5, PM10, CO, NO2, SO2, O3, as well as indicators like population density and hospital admission rates.

The main goal is to uncover patterns and correlations, validate data-driven hypotheses, and prepare the data for supervised regression models that aim to predict hospital admissions based on environmental factors.

---

## 🎯 Objectives

- Conduct **Exploratory Data Analysis (EDA)** to identify patterns, outliers, and relevant correlations between environmental and health variables.
- Validate initial hypotheses regarding the impact of air pollution on hospital admissions.
- Perform **robust data preprocessing**, including transformations, encoding, normalisation, and feature engineering.
- Prepare the dataset for the **predictive modelling phase** with clean, structured, and optimised data.

---

## 🔍 Hypotheses Investigated

1. There is a strong positive correlation between the Air Quality Index (AQI) and hospital admission rates.
2. Particulate pollutants (PM2.5 and PM10) have the greatest impact on respiratory illnesses.
3. There are significant differences in the effects of pollution across cities.

---

## 🧪 Methodology

The project was carried out in clearly defined stages:

- **Initial Data Exploration**: checking data types, missing values, descriptive statistics, and variable distributions.
- **Data Visualisation**: histograms, box plots, and a correlation matrix to examine relationships between pollutants and hospital admissions.
- **Preprocessing**: type conversions, categorical variable encoding, train/test splitting, and scaling.
- **Advanced Transformations**:
  - Creation of *lag features* for time-based insights.
  - Feature selection using `SelectKBest`.
  - Dimensionality reduction using PCA.
- **Hypothesis Validation** through both quantitative analysis and visual exploration.

---

## 📁 Dataset Structure

The dataset contains **88,489 records** with the following key columns:

- `city`: the city of data origin  
- `date`: observation date  
- `aqi`, `pm2_5`, `pm10`, `co`, `no2`, `so2`, `o3`: levels of atmospheric pollutants  
- `temperature`, `humidity`, `population_density`: environmental and demographic conditions  
- `hospital_admissions`: number of hospital admissions recorded  

---

## ✅ Key Findings

- The variable `PM2.5` showed a moderate positive correlation (~0.39) with hospital admissions, while `PM10` had a weaker effect.
- There was no significant correlation between AQI and hospital admissions, invalidating the first hypothesis.
- Visualisations revealed clear differences in pollution levels across cities, supporting the third hypothesis.
- The preprocessing pipeline successfully prepared the data for regression modelling.

---

## 📂 Repository Contents

- **Main analysis notebook**: `air_quality.ipynb`
- **Original dataset**: [`air_quality_health_dataset.csv`](air_quality_health_dataset.csv)

---

## 🚀 Next Steps

With the data fully explored and preprocessed, the next steps include:

- Applying supervised regression models to predict hospital admissions.
- Evaluating model performance using metrics such as MAE, RMSE, and R².
- Exploring time-based variables for more robust modelling.

---

## 👨‍🎓 Author

**Lucas de Oliveira Noronha**  
Data Science Student  
[LinkedIn](www.linkedin.com/in/lucas-noronha-82ba74237) | [Email](noronharm2@gmail.com)

---
