# 🌍 Air Quality Pattern Discovery via K-Means Clustering

> **Unsupervised machine learning | Environmental health analytics | Python data science pipeline**

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange?logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 🎯 Project Summary

An end-to-end data science project that applies **k-means clustering** — an unsupervised machine learning algorithm — to **3,347 air quality observations** across five key pollutants (SO₂, NO₂, O₃, PM2.5, PM10).

The goal: **discover hidden pollution patterns** that traditional summary statistics miss, and translate those patterns into actionable insights for **public health officials and environmental policymakers**.

This project demonstrates a complete ML workflow — from raw data to interpretable, business-ready clusters.

> 📌 **Note:** This repository contains the **code, dataset, and exported clustering results only**. The accompanying written report is submitted separately for academic assessment and is **not included here**.

---

## 💡 Why This Project Matters

Air pollution is one of the leading environmental health risks worldwide, contributing to respiratory illness, cardiovascular disease, and premature mortality.

By clustering monitoring data into distinct pollution "profiles," decision-makers can:
- 🏥 **Target interventions** to specific pollution sources (traffic vs. industrial)
- 📢 **Issue tailored health advisories** based on dominant pollutant mixes
- 📈 **Track policy effectiveness** over time by monitoring cluster shifts
- 🗺️ **Prioritise resources** to the highest-risk zones

---

## 🛠️ Technical Stack

| Category | Tools |
|----------|-------|
| **Language** | Python 3.10+ |
| **Data Wrangling** | Pandas, NumPy |
| **Machine Learning** | scikit-learn (KMeans, StandardScaler, silhouette_score, PCA) |
| **Visualisation** | Matplotlib, Seaborn |
| **Environment** | Jupyter Notebook |

---

## 🔬 Methodology
┌─────────────────────┐
│ 1. Data Loading │ → 3,347 rows × 5 pollutant features
├─────────────────────┤
│ 2. EDA │ → Descriptive stats, correlation heatmap, distributions
├─────────────────────┤
│ 3. Preprocessing │ → StandardScaler normalisation (k-means is scale-sensitive)
├─────────────────────┤
│ 4. Optimal k │ → Elbow Method + Silhouette Score cross-validation
├─────────────────────┤
│ 5. Clustering │ → K-Means (k=3, n_init=10, random_state=42)
├─────────────────────┤
│ 6. Validation │ → PCA 2D visualisation, centroid profiling
├─────────────────────┤
│ 7. Interpretation │ → Cluster labelling & domain insights
└─────────────────────┘

text

---

## 📊 Key Findings

Three distinct pollution profiles emerged:

| Cluster | Dominant Pollutants | Interpretation |
|:-------:|---------------------|----------------|
| **0** | High NO₂ & Particulates (PM2.5, PM10) | 🚗 Urban traffic & industrial zones |
| **1** | Low across all pollutants | 🌿 Background / rural baseline |
| **2** | High SO₂ & O₃ | 🏭 Point-source industrial emissions |

**Correlation insight:** PM2.5 and PM10 showed a strong positive correlation (**r = 0.87**), confirming shared emission sources — a well-documented relationship in environmental science.
