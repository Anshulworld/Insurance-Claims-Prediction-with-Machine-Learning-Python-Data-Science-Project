```markdown
# 🚗 Insurance Claims Prediction & Risk Analytics

An end-to-end Machine Learning and Business Intelligence solution designed to assess policyholder risk, predict insurance claim likelihood, and assist underwriters in data-driven risk management. Deployed as an interactive web application.

---

## 📌 Project Overview
Insurance claim underwriting relies on accurately identifying high-risk profiles to balance premium pricing, optimize reserves, and minimize loss ratios. This project explores historical customer demographics, policy characteristics, and claims data to build predictive classification models and deploy an interactive decision-support interface.

* **Objective:** Predict whether an insurance policyholder will file a claim (`Claim Status: 0 / 1`).
* **Deployment:** Interactive user-facing application built with Streamlit/Dash to provide real-time probability estimates for new policy applicants.

---

## 🛠️ Tech Stack & Tools
* **Languages:** Python (Pandas, NumPy)
* **Machine Learning:** Scikit-Learn (Classification, Cross-Validation, Hyperparameter Tuning)
* **Visualization:** Matplotlib, Seaborn
* **Model Artifacts:** Pickle (`claim_model.pkl`, `model_columns.pkl`, `model_options.pkl`)
* **Web Application:** Python (`app.py`)

---

## 📂 Repository Structure
```text
├── Data-Visualizations/        # Exploratory data analysis charts & plots
├── Insurance claims data.csv   # Raw dataset containing policyholder records
├── Project_Notebook.ipynb      # End-to-end EDA, preprocessing, and model training
├── app.py                      # Interactive web app script for inference
├── claim_model.pkl             # Serialized trained classification model
├── model_columns.pkl           # One-hot encoded feature matrix references
├── model_options.pkl           # Valid categorical input mappings for UI
└── README.md                   # Project documentation

```

---

## 🔄 End-to-End Workflow

### 1. Exploratory Data Analysis (EDA) & Data Preprocessing

* Cleaned missing values, checked distributions, and handled potential outliers in policy amounts and age distributions.
* Evaluated feature correlations with the target variable to uncover primary risk factors.
* Applied one-hot encoding for categorical variables (e.g., vehicle type, location, coverage plan) and scaled numeric inputs.

### 2. Machine Learning Modeling & Optimization

* Handled potential class imbalances commonly present in claim datasets (using resampling or balanced class weighting).
* Trained and compared baseline classifiers against ensemble models (e.g., Random Forest, Gradient Boosting, Extra Trees).
* Evaluated models using business-critical metrics: **Precision**, **Recall**, **F1-Score**, and **ROC-AUC** to balance false positives against unflagged claims.
* Serialized the top-performing pipeline into `claim_model.pkl` alongside encoder mappings.

### 3. Application Deployment (`app.py`)

* Created an interactive user interface allowing underwriters and users to select applicant inputs.
* Dynamically loaded serialized features (`model_columns.pkl`, `model_options.pkl`) to guarantee zero feature skew during inference.
* Displays instant risk predictions alongside claim probability scores.

---

## 📊 Key Insights & Visualizations

*(Add references to your saved charts in the `Data-Visualizations` folder)*

* **High-Risk Segment Identification:** Visualized demographic and vehicle profiles most correlated with claim frequency.
* **Feature Importance:** Key drivers influencing claim filings (e.g., vehicle age, driver profile, policy tier).

---

## 🚀 How to Run Locally

1. **Clone the repository:**
```bash
git clone [https://github.com/Anshulworld/Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project.git](https://github.com/Anshulworld/Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project.git)
cd Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project

```


2. **Install required dependencies:**
```bash
pip install -r requirements.txt
# Or install core packages:
pip install pandas numpy scikit-learn streamlit matplotlib seaborn

```


3. **Launch the web application:**
```bash
streamlit run app.py
# Or if using Dash/Flask: python app.py

```



```
