
The following is what is in EECA project notebook. Lesson learnt:
- Have a clearly structured intro
- Use bullet points
- Use icons
- Provide version requirements

# Synthetic Data Generation Pipeline
## 📁 Project Overview

This project involves three main components:

1. **Clustering** users based on their time-series data.
2. **Fitting statistical distributions** to the data within each cluster at each timestamp.
3. **Generating synthetic data** from the fitted models for further analysis purposes.

## 📁 Project Structure

- **project/**
  - **data preprocessing/**
    - *key functions:* `process_energy_data()`, `compute_usage_features()` (note: the QTN data is quite clean, but data from other cities may require additional cleaning.)
  - **📈 clustering/**
    - dimension reduction - UMAP
    - cluster methods - Kmeans (Applying different clustering techniques may enhance the quality of the results.)
    - *key functions:* `clustering_parameter_est()`, `cluster()`
  - **📉 distribution fitting and synthetic generation/**
    - fit the data into half-hourly data, currently four different distribution used
        - gamma distribution
        - exponential distribution
        - weibull min 
        - inverse gaussian distribution
    - *key functions:* `find_best_distribution()`
  - **results/**
    Storage for output files, evaluation metrics, and visualizations.
  - **version requirements/**
    - `requirements.txt`

## 📊 Results

1. Summary statistics comparing original and synthetic data
2. Perform a comparison between cluster-specific synthetic distributions and synthetic distributions generated without clustering.
3. Evaluation plots: CDF, PDF, histogram overlays, Kolmogorov–Smirnov test (ks test)

