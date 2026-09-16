# Predictive Solar Generation Modeling for Decentralized Energy Systems in Ibadan

This repository contains the replication code, data ingestion routines, and analytical artifacts for evaluating machine learning algorithms on short-term solar irradiance forecasting in Ibadan, Nigeria ($7.38^\circ\text{N}, 3.94^\circ\text{E}$).

## Overview

Accurate solar insolation forecasting is vital for decentralized micro-grid management and battery energy storage dispatch in sub-Saharan urban centers. This study evaluates Multiple Linear Regression, Random Forest, and Gradient Boosting algorithms on hourly surface meteorological data obtained from the NASA POWER database across 2023.

## Key Empirical Findings

* **Top Performer:** Gradient Boosted Trees yielded an $R^2$ of 0.9849 with an MAE of 17.226 W/m² and RMSE of 32.207 W/m².
* **Baseline Comparison:** Non-linear ensemble learning produced a 48.45% reduction in MAE relative to Multiple Linear Regression.
* **Atmospheric Drivers:** Diurnal cyclical encoding (`Hour_Cos`) and one-hour autoregressive persistence dominate predictive feature importance, while ambient relative humidity serves as a strong negative indicator of cloud-induced suppression.

## Directory Layout

* `data/`: Contains the NASA POWER meteorological time-series records.
* `src/`: Python execution scripts for preprocessing, feature engineering, and model training.
* `figures/`: High-resolution (300 DPI) analytical plots formatted for publication.
* `tables/`: Summary statistics and model comparative tables in both CSV and LaTeX formats.

## Quickstart Guide

### 1. Clone and Install Dependencies

```bash
git clone [https://github.com/](https://github.com/)<your-username>/ibadan-solar-forecasting.git
cd ibadan-solar-forecasting
pip install -r requirements.txt
