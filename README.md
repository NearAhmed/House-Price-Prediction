# 🏠 House Price Prediction

Machine learning solution for Kaggle's **House Prices - Advanced Regression Techniques** competition.

**Team:** Neural Nox  
**Best Local CV RMSE:** `0.11785`  
**Kaggle Public Score:** `0.126`

---

##  Objective

Predict residential house sale prices using 79 features describing property quality, size, location, age, garage, basement, and other characteristics.

---

##  Workflow

EDA  
→ Missing Value Handling  
→ Feature Engineering  
→ One-Hot Encoding  
→ Log Transformation  
→ Model Comparison  
→ XGBoost Tuning  
→ Cross Validation  
→ Kaggle Submission

---

## 🧹 Data Preparation

- Handled missing categorical and numerical values
- Used neighborhood median for `LotFrontage`
- One-hot encoded categorical features
- Applied `log1p()` to `SalePrice`
- Investigated potential outliers

---

##  Feature Engineering

Created features including:

- `TotalSF`
- `TotalBathrooms`
- `HouseAge`
- `RemodelAge`
- `TotalPorchSF`
- `TotalOutdoorSF`
- `GarageAge`
- `HasGarage`
- `HasBasement`
- `HasFireplace`
- `HasPool`
- `IsRemodeled`
- `IsNew`

---

##  Models Tested

| Model | CV RMSE |
|---|---:|
| Ridge Regression | 0.13980 |
| Gradient Boosting | 0.12236 |
| XGBoost V1 | 0.12118 |
| XGBoost + Features | 0.11890 |
| XGBoost V2 | 0.11801 |
| **XGBoost V2 + Extended Features** | **0.11785** |

The final model selected was **XGBoost V2**.

---

##  Kaggle Submission

**Submission 1**

- Team: **Neural Nox**
- Model: **XGBoost V2 + Feature Engineering**
- Local 5-Fold CV: `0.11785`
- Kaggle Public Score: `0.126`

---

##  Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## 📂 Repository Structure

```text
House_Price_Prediction/
│
├── dataset/
│   ├── train.csv
│   ├── test.csv
│   └── data_description.txt
│
├── House_Price_Prediction.ipynb
├── submission_xgb_v2.csv
└── README.md
