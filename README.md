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

**Data Sources:** CDC BRFSS, US Census Bureau, USDA Food Access Research Atlas

---

## Getting Started

### Prerequisites

- **Python 3.8+** or **Google Colab** (recommended)
- Install dependencies:

```bash
pip install -r requirements.txt
```

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ullasbc02/obesity-risk-analytics.git
   cd obesity-risk-analytics
   ```

2. **Set up your environment:**
   ```bash
   pip install -r requirements.txt
   ```

3. **For Google Colab users:**
   - Upload project folders to Google Drive
   - Notebooks include `drive.mount()` commands for seamless integration
   - All paths are configured for `/content/drive/MyDrive/` structure

### Running the Notebooks

#### Option 1: Local Jupyter
```bash
jupyter notebook notebooks/01_data_cleaning.ipynb
```

#### Option 2: Google Colab (Recommended)
- Click the "Open In Colab" badge at the top of each notebook
- Notebooks automatically mount Google Drive on first cell execution
- Run cells sequentially for end-to-end analysis

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

## Requirements

All dependencies are specified in `requirements.txt`:

**Core:** pandas, numpy, scipy  
**ML:** scikit-learn, hdbscan, umap-learn, pygam  
**Statistics:** statsmodels, dcor, shap  
**Geospatial:** geopandas, shapely, libpysal, esda  
**Visualization:** matplotlib, seaborn, plotly  

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

 **Google Colab Optimization**
- All notebooks are designed and tested for Google Colab environment
- Local execution may require path adjustments
- GPU acceleration available in Colab for faster model training

 **Data Structure**
- Raw datasets are loaded from Google Drive paths
- Processed data is cached to improve notebook execution speed
- GeoJSON files required for spatial visualizations

 **File Management**
- Ensure "obesity-analytics-notebooks" and "obesity-risk-analytics" folders exist in Google Drive
- Update data paths in notebooks if your drive structure differs

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

**Project Author:** Ullas BC  and Vishrutha Ravi
**Repository:** [github.com/ullasbc02/obesity-risk-analytics](https://github.com/ullasbc02/obesity-risk-analytics)



---

## Acknowledgments

- CDC BRFSS data for obesity prevalence metrics
- US Census Bureau for socioeconomic indicators
- USDA Food Access Research Atlas for food access data
- County FIPS geometries for spatial analysis

