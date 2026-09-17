# 🚗 Insurance Claims Prediction & Risk Analytics

An end-to-end Machine Learning and Business Intelligence solution designed to assess policyholder risk, predict insurance claim likelihood, and assist underwriters in data-driven risk management. Deployed as an interactive web application.

---

## 📌 Project Overview
Insurance claim underwriting relies on accurately identifying high-risk profiles to balance premium pricing, optimize reserves, and minimize loss ratios. This project explores historical customer demographics, policy characteristics, and claims data to build predictive classification models and deploy an interactive decision-support interface.

* **Objective:** Predict whether an insurance policyholder will file a claim (`Claim Status: 0 / 1`).
* **Deployment:** Interactive user-facing application built with Streamlit to provide real-time probability estimates for new policy applicants.

---

## 🛠️ Tech Stack & Tools
* **Languages:** Python (Pandas, NumPy)
* **Machine Learning:** Scikit-Learn (Classification, Cross-Validation, Hyperparameter Tuning, Random Forest, XGBoost)
* **Visualization:** Matplotlib, Seaborn
* **Model Artifacts:** Pickle (`claim_model.pkl`, `model_columns.pkl`, `model_options.pkl`)
* **Web Application:** Python (`app.py`), Streamlit

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
