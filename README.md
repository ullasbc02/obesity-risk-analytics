# Obesity Risk Analytics

A comprehensive data analysis project investigating obesity risk factors across US counties through spatial analysis, machine learning, and temporal forecasting.

## Project Overview

This repository contains code and resources for analyzing obesity risk factors using multiple datasets and advanced analytical techniques. The analysis pipeline includes:

- **Data Preprocessing & Cleaning** - Merging and validating multi-year datasets
- **Exploratory Data Analysis (EDA)** - Spatial and temporal pattern discovery
- **Unsupervised Learning** - Clustering and segmentation analysis
- **Supervised Learning** - Predictive modeling for obesity rates
- **Multi-Criteria Decision Making (MCDM)** - Policy prioritization framework
- **Temporal Forecasting** - Early warning systems and 2030 projections
- **Interactive Dashboard** - Visual decision support tool

---

## Project Structure

###  Phase 1: Core Analysis (`notebooks/`)

**7 comprehensive notebooks** for baseline obesity risk analysis:

| Notebook | Purpose |
|----------|---------|
| `01_data_cleaning.ipynb` | Import, merge, and preprocess 7 datasets by FIPS code |
| `02_eda_spatial_analysis.ipynb` | Spatial correlations, feature distributions, Moran's I analysis |
| `03_unsupervised_learning_final.ipynb` | K-Means, hierarchical, DBSCAN clustering & UMAP visualization |
| `04_supervised_learning_final.ipynb` | Random Forest & Gradient Boosting predictive models |
| `05_MCDM_final.ipynb` | Multi-criteria decision analysis for policy targeting |
| `06_policy_decision_support.ipynb` | SHAP explanations & policy recommendations |
| `07_dashboard.ipynb` | Interactive Plotly dashboard for insights |

###  Phase 2: Temporal Analysis (`notebooks-forecast/`)

**7 focused notebooks** for time-series and forecasting analysis (2010-2023):

| Notebook | Purpose |
|----------|---------|
| `01_data_cleaning.ipynb` | Extract and merge temporal datasets |
| `02_eda_spatial_temporal.ipynb` | National trends, state comparisons, temporal patterns |
| `03_static_clustering.ipynb` | Baseline clustering on aggregated county features |
| `04_dynamic_joint_trends.ipynb` | Trend slopes, volatility, and trend-based clustering |
| `05_temporal_trend_early_warning.ipynb` | Early warning indicators for high-risk regions |
| `06_forecasting_early_warning.ipynb` | Next-year obesity predictions with lag features |
| `07_forecasting_2030.ipynb` | Long-term projections to 2030 |

---

## Key Datasets

The analysis integrates 7 socioeconomic and health behavior indicators:

- **Obesity Prevalence Rate** (%)
- **Poverty Rate** (%)
- **Median Household Income** ($)
- **Unemployment Rate** (%)
- **Physical Inactivity Rate** (%)
- **Low Access to Healthy Food** (%)
- **Health Professional Shortage Areas** (categorical)
- **County FIPS Geometries** (GeoJSON)
- **Population Estimates based on US Census Data** (for weighting and normalization)

**Data Sources:** 
(https://www.ruralhealthinfo.org/)
(https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-detail.html)

---

## Getting Started

### Important: Google Colab Only

**All notebooks in this project are specifically designed to run ONLY on Google Colab.** They are not intended for local execution due to:
- Pre-configured Google Drive integration
- Optimized file paths for Colab environment
- Built-in GPU acceleration support
- Automatic dependency management in Colab

### Setup Instructions (Google Colab)

#### Step 1: Prepare Your Google Drive

1. **Upload the data folders from the data directory to your Google Drive:**
   - Create or locate the following folders in your Google Drive:
     - `/MyDrive/obesity-analytics-notebooks/` (contains multi-year temporal datasets)
     - `/MyDrive/obesity-risk-analytics/` (contains processed analysis data)
   - Ensure all raw datasets are placed in the appropriate folders

2. **Verify the folder structure:**
   ```
   Google Drive/
   └── MyDrive/
       ├── obesity-analytics-notebooks/
       │   └── Multi-Year-Trend/Dataset/
       └── obesity-risk-analytics/
           ├── data/
           │   ├── raw/
           │   └── processed_final/
           └── dashboard_data_final/
   ```

#### Step 2: Open Notebooks in Google Colab

1. **Access the notebooks:**
   - Click the **"Open In Colab"** badge at the top of any notebook
   - Or navigate to [Google Colab](https://colab.research.google.com/) and upload the `.ipynb` files

2. **Mount Google Drive:**
   - Each notebook includes a `drive.mount('/content/drive')` cell
   - Run this cell first and authorize access to your Google Drive

3. **Run the analysis:**
   - Execute cells sequentially from top to bottom
   - Dependencies are automatically installed via `!pip install` commands in notebooks
   - All file paths are pre-configured for the Colab environment

#### Step 3: Follow the Workflow

- Start with **Phase 1** (`notebooks/` folder) for core analysis
- Then proceed to **Phase 2** (`notebooks-forecast/` folder) for temporal forecasting
- Each notebook is self-contained with markdown explanations

---

## Key Features

 **Comprehensive Data Pipeline** - From raw data to actionable insights  
 **Spatial Analysis** - County-level geographic patterns and clustering  
 **Temporal Modeling** - 14-year trend analysis and future forecasting  
 **Interactive Visualizations** - Plotly dashboards for exploration  
 **Explainable ML** - SHAP values for model interpretation  
 **Policy Framework** - MCDM for evidence-based decision-making  
 **Early Warning System** - Identify at-risk counties for intervention  

---

## Dependencies

**All dependencies are automatically installed within Google Colab notebooks** via `!pip install` commands in the first cells.

The `requirements.txt` file is provided for reference only and includes:

**Core:** pandas, numpy, scipy  
**ML:** scikit-learn, hdbscan, umap-learn, pygam  
**Statistics:** statsmodels, dcor, shap  
**Geospatial:** geopandas, shapely, libpysal, esda  
**Visualization:** matplotlib, seaborn, plotly  

> **Note:** You do NOT need to manually install these packages. Colab handles all installations automatically when you run the notebooks.  

---

## Workflow Guide

### Phase 1 Execution Order
1. Start with `01_data_cleaning.ipynb` to prepare the dataset
2. Run `02_eda_spatial_analysis.ipynb` to understand patterns
3. Execute `03_unsupervised_learning_final.ipynb` for clustering insights
4. Use `04_supervised_learning_final.ipynb` for predictive modeling
5. Apply `05_MCDM_final.ipynb` for policy prioritization
6. Generate explanations with `06_policy_decision_support.ipynb`
7. Explore results in `07_dashboard.ipynb`

### Phase 2 Execution Order
1. Run `01_data_cleaning.ipynb` for temporal data
2. Execute `02_eda_spatial_temporal.ipynb` to analyze trends
3. Use `03_static_clustering.ipynb` and `04_dynamic_joint_trends.ipynb` for clustering
4. Generate early warnings with `05_temporal_trend_early_warning.ipynb`
5. Create forecasts using `06_forecasting_early_warning.ipynb` and `07_forecasting_2030.ipynb`

---

## Important Notes

 **Google Colab REQUIRED**
- **DO NOT attempt to run these notebooks locally** - they are configured exclusively for Google Colab
- All file paths use `/content/drive/MyDrive/` structure specific to Colab
- Notebooks automatically install required dependencies via `!pip install` commands
- GPU/TPU acceleration is automatically available in Colab for faster training

 **Google Drive Structure is Critical**
- The exact folder names "obesity-analytics-notebooks" and "obesity-risk-analytics" MUST exist in your Google Drive
- Data paths are hardcoded in notebooks - changing folder names will break the notebooks
- GeoJSON files must be in the `dashboard_data_final/` folder
- All raw data files must match the expected filenames in the notebooks

 **Data Management**
- Processed datasets are saved back to Google Drive automatically
- Trained models (.pkl files) are stored in `processed_final/` folders
- Intermediate outputs are cached to speed up re-runs
- Each notebook saves its outputs for use by subsequent notebooks

---

## Output & Results

Notebooks generate:
- **CSV outputs** - Predictions, cluster assignments, trend analysis
- **Visualizations** - Static plots (PNG) and interactive dashboards (HTML)
- **Models** - Trained ML models saved as pickle files (`.pkl`)
- **Data summaries** - Statistical tables and feature importance rankings

---

## License

This project is open source

---

## Contact & Contributors

**Project Author:** Ullas Basavapatna Chandrashekar  and Vishrutha Ravi

**Repository:** [github.com/ullasbc02/obesity-risk-analytics](https://github.com/ullasbc02/obesity-risk-analytics)



---

## Acknowledgments
- Data sourced from Rural Health Information Hub and US Census Bureau

