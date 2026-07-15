#  Global Life Expectancy Prediction & Socio-Economic Analysis

A Machine Learning regression project that predicts **Life Expectancy** using socio-economic, demographic, and healthcare indicators collected from **WHO** and the **World Bank**.

This project explores the relationship between education, healthcare, economic status, and mortality indicators to determine the most influential factors affecting life expectancy and compares multiple regression models to identify the best-performing algorithm.

---

##  Project Overview

Life expectancy is one of the most important indicators of a country's healthcare and economic development.

The objective of this project is to:

- Predict life expectancy using Machine Learning.
- Analyze the relationship between health, education, and economic indicators.
- Compare different regression algorithms.
- Evaluate model performance using multiple evaluation metrics.
- Identify the best predictive model.

---

##  Team Members

- Islam Shehta Mohamed
- Ahmed Hossam Awad
- Aser Esam Abdellatif
- Mohamed Mohamed Reda

---

#  Dataset Information

**Source**

- World Health Organization (WHO)
- World Bank

### Dataset Size

| Property | Value |
|----------|------:|
| Rows | 2,864 |
| Features | 21 |
| Target | Life Expectancy |

---

#  Features

###  Target Variable

- **Life_expectancy**

---

###  Demographic Features

- Country
- Region
- Year
- Population

---

###  Economic Features

- GDP_per_capita
- Schooling
- Economy_status_Developed
- Economy_status_Developing

---

###  Healthcare Features

- Adult_mortality
- Infant_deaths
- Under_five_deaths
- Alcohol_consumption
- BMI
- Thinness_10_19_years
- Thinness_5_9_years

---

###  Immunization Features

- Hepatitis_B
- Measles
- Polio
- Diphtheria
- Incidents_HIV

---

#  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

#  Project Workflow

## 1- Data Loading

- Loaded the dataset
- Created a copy of the data

---

## 2️- Data Exploration

Performed:

- `head()`
- `shape`
- `describe()`
- `info()`

---

## 3️- Data Cleaning

### Checked

- Missing Values
- Duplicate Rows
- Duplicate Categories

No missing values or duplicate rows were found.

Used:

```python
isnull().sum()
duplicated().sum()
unique()
```

---

### Removed Unnecessary Columns

Dropped:

- Country
- Economy
- Infant Deaths
- Under Five Deaths
- Population

---

### Encoding

Applied **One-Hot Encoding** on:

- Region

---

##  Exploratory Data Analysis (EDA)

Performed:

- Distribution of Life Expectancy
- Outlier Detection
- Schooling Distribution
- Correlation Heatmap

Main observations:

- Schooling has a strong positive relationship with Life Expectancy.
- Adult Mortality negatively affects Life Expectancy.
- Healthcare indicators show significant correlation.
- Several variables contain outliers but remain meaningful.

---

#  Feature Engineering

Performed:

- Target Selection
- Feature Selection
- Train-Test Split
- StandardScaler

Target Variable:

```
Life_expectancy
```

Dropped Features:

- Life Expectancy
- Adult Mortality
- Under Five Deaths

---

#  Machine Learning Models

The following regression models were implemented:

- Linear Regression
- Lasso Regression
- Ridge Regression
- Polynomial Regression
- Random Forest Regression

---

#  Model Performance

| Model | Train R² | Test R² |
|--------|----------:|---------:|
| Linear Regression | **0.8416** | **0.8683** |
| Lasso Regression | **0.8041** | **0.7755** |
| Ridge Regression | **0.8416** | **0.8683** |
| Polynomial Regression | **0.9556** | **0.9405** |
| Random Forest | **0.9971** | **0.9856** |

---

#  Detailed Model Comparison

| Model | MSE | MAE | R² Score | Running Time (s) |
|--------|---------:|---------:|---------:|---------:|
| Linear Regression | **13.148284** | **2.932323** | **0.841570** | **0.0013** |
| Lasso Regression | **18.631997** | **3.540372** | **0.775494** | **0.0013** |
| Ridge Regression | **13.148731** | **2.932624** | **0.841565** | **0.0009** |
| Polynomial Regression | **4.941874** | **1.671119** | **0.940453** | **0.0004** |
| Random Forest | **1.192738** | **0.731378** | **0.985628** | **0.0430** |

---

#  Cross Validation

Cross Validation Mean Score

```
0.9870
```

The high cross-validation score indicates excellent generalization performance and confirms that the Random Forest model is reliable on unseen data.

---

#  Best Model

**Random Forest Regressor**

Performance:

- Train R² = **0.9971**
- Test R² = **0.9856**
- MAE = **0.7314**
- MSE = **1.1927**
- Cross Validation = **0.9870**

Reasons for selection:

- Highest prediction accuracy
- Lowest prediction error
- Excellent generalization
- Handles nonlinear relationships effectively
- Robust against overfitting

---

#  Key Findings

- Education (Schooling) is one of the strongest predictors of Life Expectancy.
- Healthcare indicators significantly influence life expectancy.
- Economic factors contribute positively to prediction performance.
- Random Forest substantially outperformed all linear models.
- Polynomial Regression successfully captured nonlinear relationships.

---

#  Future Improvements

- Hyperparameter Tuning
- XGBoost
- LightGBM
- CatBoost
- SHAP Explainability
- Feature Importance Analysis
- Model Deployment using Flask or FastAPI
- Interactive Dashboard using Streamlit

---

#  Project Structure

```
Global-Life-Expectancy-Prediction/
│
├── data/
│   └── Life_Expectancy.csv
│
├── notebooks/
│   └── Life_Expectancy_Prediction.ipynb
│
├── images/
│
├── README.md
│
└── requirements.txt
```

---

#  Libraries

```python
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

#  Visualizations

The project includes:

- Distribution Plots
- Correlation Heatmap
- Boxplots
- Linear Regression Coefficients
- Lasso Coefficients
- Ridge Coefficients
- Model Comparison Charts
- R² Score Comparison

---

#  Conclusion

This project demonstrates a complete end-to-end Machine Learning workflow, including data preprocessing, exploratory data analysis, feature engineering, model training, evaluation, and comparison.

Among all tested models, **Random Forest Regressor** achieved the best overall performance with an **R² Score of 0.9856** and a **Cross Validation Score of 0.9870**, making it the most reliable model for predicting global life expectancy.

---

## 📬 Contact

If you found this project helpful, feel free to ⭐ the repository and connect with me on LinkedIn.
