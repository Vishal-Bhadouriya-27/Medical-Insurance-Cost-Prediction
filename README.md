# 🏥 Medical Insurance Cost Prediction using Multiple Linear Regression

An end-to-end Machine Learning data analytics project built on healthcare expenditure data. The analysis includes comprehensive Exploratory Data Analysis (EDA), outlier treatment using the Interquartile Range (IQR) method, multicollinearity reduction via Variance Inflation Factor (VIF), and predictive modeling using Multiple Linear Regression.

---

## 📊 Key Results & Insights
- **Model R² Score:** Achieved **~84.05%** variance coverage on unseen test data.
- **Primary Cost Drivers:** `Anual_Salary`, `past_consultations`, `Hospital_expenditure`, `Claim_Amount`, and `children` count show the strongest positive predictive relationship with medical charges.
- **Multicollinearity Elimination:** Statistical feature selection via VIF removed highly dependent variables (dropping redundant features such as `num_of_steps`, `NUmber_of_past_hospitalizations`, `age`, and `bmi`) to build a robust, non-overfitted model.

---

## 🛠️ Tech Stack & Python Libraries
- **Language:** Python 3.x
- **Data Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn` (`LinearRegression`, `train_test_split`, `r2_score`, `LabelEncoder`)
- **Statistical Modeling:** `statsmodels` (`variance_inflation_factor`)

---

## 📁 Dataset Overview
The dataset contains 1,338 transaction records detailing demographic, physical health, and historic financial expenditure attributes:
- **Demographic & Physical:** `age`, `sex`, `bmi`, `children`, `smoker`, `region`
- **Medical History & Metrics:** `Claim_Amount`, `past_consultations`, `num_of_steps`, `Hospital_expenditure`, `NUmber_of_past_hospitalizations`, `Anual_Salary`
- **Target Variable:** `charges` (Actual annual individual medical insurance expenditure)

---

## 🔄 Machine Learning Workflow
1. **Exploratory Data Analysis (EDA):** Evaluated summary statistics, distributions, and missing values across all 1,338 records.
2. **Outlier Treatment:** Applied IQR bounds ($Q1 - 1.5 \times IQR$ to $Q3 + 1.5 \times IQR$) across skewed numerical features to eliminate extreme records.
3. **Categorical Feature Encoding:** Converted categorical attributes (`sex`, `smoker`, `region`) into numeric representations using `LabelEncoder`.
4. **Multicollinearity Optimization (VIF):** Calculated Variance Inflation Factors and iteratively dropped highly collinear variables exceeding standard thresholds ($VIF > 6$).
5. **Model Evaluation:** Split data into an 80/20 train-test ratio (`random_state=0`) and evaluated performance using the Coefficient of Determination ($R^2$).

---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/Vishal-Bhadouriya-27/Medical-Insurance-Cost-Prediction.git](https://github.com/Vishal-Bhadouriya-27/Medical-Insurance-Cost-Prediction.git)
   cd "Medical insurance cost prediction"
