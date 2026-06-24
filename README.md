#  Health Data Cleaning & Preprocessing Project

This project demonstrates a complete **Data Cleaning and Preprocessing Pipeline** for healthcare data. The objective is to handle missing values, detect and treat outliers, and prepare a **machine-learning-ready dataset** for disease risk prediction.



##  Project Overview

Healthcare datasets often contain:

- Missing values
- Incorrect or inconsistent records
- Extreme outliers
- Data quality issues

This project applies multiple preprocessing techniques to improve dataset quality before machine learning modeling.



## Dataset Description

The dataset contains patient health records with demographic and medical attributes.

| Feature | Description |
|----------|-------------|
| `patient_id` | Unique patient identifier |
| `age` | Patient age |
| `gender` | Male/Female |
| `region` | North/South/East/West |
| `bmi` | Body Mass Index |
| `blood_pressure` | Systolic blood pressure |
| `cholesterol` | Cholesterol level |
| `glucose` | Fasting glucose level |
| `disease_risk` | Target variable (0 = Low Risk, 1 = High Risk) |

---

## Objectives

- Perform missing value analysis
- Apply multiple imputation techniques
- Detect outliers using statistical methods
- Compare different preprocessing strategies
- Generate a clean dataset for machine learning
- Produce visualizations and summary reports

---

##  Techniques Implemented

### 1. Missing Value Handling

#### Simple Imputation
- Numerical Features → Mean Imputation
- Categorical Features → Most Frequent Value Imputation

#### Most Frequent Imputation
Used for:
- Gender
- Region

#### Missing Indicator + Random Sample Imputation
- Creates missingness indicator variables
- Replaces missing values using random sampling

#### KNN Imputation
- Uses nearest-neighbor information
- Preserves relationships between variables

#### MICE (Multiple Imputation by Chained Equations)
- Iterative multivariate imputation
- Uses feature correlations to estimate missing values

---

### 2. Outlier Detection & Treatment

#### Z-Score Method
Detects extreme values based on standard deviations from the mean.

#### IQR Method
Detects outliers using quartile ranges.

#### Percentile Method
Caps values below the 1st percentile and above the 99th percentile.

#### Winsorization
Limits extreme observations while preserving all records.

---

##  Workflow

```text
Raw Dataset
     │
     ▼
Missing Value Analysis
     │
     ▼
Imputation Techniques
     │
     ▼
Outlier Detection
     │
     ▼
Outlier Treatment
     │
     ▼
Comparison & Evaluation
     │
     ▼
Clean Dataset
     │
     ▼
Machine Learning Ready Data
```

---

##  Project Structure

```text
HealthDataClean_Project2/
│
├── Project_2_PRE.ipynb
├── patient_health_records_1000.csv
├── cleaned_patient_records.csv
├── README.md
│
├── images/
│   ├── missing_heatmap.png
│   ├── boxplot_before.png
│   └── boxplot_after.png
│
└── reports/
    └── summary_report.pdf
```



##  Results

### Missing Value Treatment

Successfully handled missing values using:

- Simple Imputer
- Most Frequent Imputation
- Random Sample Imputation
- KNN Imputer
- MICE Algorithm

### Outlier Treatment

Successfully detected and treated outliers using:

- Z-Score
- IQR
- Percentile Capping
- Winsorization

---

##  Final Dataset

The final cleaned dataset:

- Contains no missing values
- Has controlled outliers
- Preserves data distribution
- Is suitable for machine learning applications

---

##  Key Findings

### Best Imputation Technique: MICE

**Reason:**
- Uses relationships among variables
- Produces more realistic estimates
- Preserves statistical properties

### Best Outlier Treatment: Winsorization

**Reason:**
- Retains all observations
- Reduces influence of extreme values
- Prevents unnecessary data loss

---

##  Future Improvements

- Feature Engineering
- Data Normalization
- Feature Selection
- Machine Learning Model Development
- Hyperparameter Tuning
- Model Deployment

---

##  Visualizations

- Missing Value Heatmap
- Boxplot Before Outlier Treatment
- Boxplot After Outlier Treatment
- Distribution Comparison Charts

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Feature-engine
- Statsmodels

---

##  Author

**Mant Patel**

Data Cleaning & Preprocessing Project for Healthcare Analytics and Disease Risk Prediction.
