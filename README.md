# EV Charging Station Reliability Prediction

## Overview
This project builds a scalable machine learning pipeline to predict **EV charging station failures** using **6M+ records** across **97,000+ stations**.

The objective is to proactively identify high-risk stations and understand the key factors driving infrastructure reliability.

The dataset presented a severe **187:1 class imbalance**, making failure detection challenging. The model was optimized to improve recall and better capture rare failure events.

---

## Tech Stack

- **Language:** Python  
- **Framework:** PySpark (MLlib)  
- **Environment:** Google Colab Pro
- **Libraries:** Pandas, NumPy, Scikit-learn  
- **Data Source:** NREL API (https://developer.nrel.gov/docs/transportation/alt-fuel-stations-v1/electric-networks/)

---

## Data Pipeline

### Data Ingestion
- Automated data extraction using the **NREL API**
- Processed over **6 million records**
- Cleaned and standardized station-level data

### Data Preprocessing
- Handled missing values
- Feature encoding and transformation
- Structured dataset for distributed processing in PySpark

### Dimensionality Reduction
- Applied **Principal Component Analysis (PCA)**
  - Reduced features from **80 → 8**
  - Retained **96% of total variance**
- Improved computational efficiency while preserving key information

### Class Imbalance Handling
- Addressed **187:1 imbalance ratio**
- Applied **undersampling**
- Optimized model for recall

---

## Model Development
- Built classification pipeline using **PySpark MLlib**
- Trained and evaluated model on large-scale dataset
- Focused on improving recall for rare-event detection

---

## Results
The final model achieved **72.5% recall**, representing a **6.6× improvement over baseline** in detecting at-risk stations.
- Key reliability drivers identified:
  - Station age
  - Climate zone
  - Network size
---

 ## Key Takeaways
- Handling extreme class imbalance (187:1) is critical for rare-event prediction performance.
- Optimizing for recall significantly improves detection of high-risk stations.
- PCA effectively reduced dimensionality (80 → 8 features) while retaining 96% variance.
- Reliability risk is influenced by operational and environmental factors such as station age and climate.
- Scalable data processing with PySpark enables large-scale infrastructure analytics.
