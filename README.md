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

---

## 🔄 End-to-End Workflow

### 1. Exploratory Data Analysis (EDA) & Data Preprocessing

* Cleaned missing values, checked distributions, and handled outliers in policy amounts and age distributions.
* Evaluated feature correlations with the target variable to uncover primary risk factors.
* Applied one-hot encoding for categorical variables (e.g., vehicle type, location, coverage plan) and scaled numeric inputs.

### 2. Machine Learning Modeling & Optimization

* Handled class imbalances commonly present in claim datasets to ensure the model accurately detects minority class claims.
* Trained and compared baseline classifiers against ensemble models (Random Forest, Gradient Boosting).
* Evaluated models using business-critical metrics: **Precision**, **Recall**, **F1-Score**, and **ROC-AUC** to balance false positives against unflagged claims.
* Serialized the top-performing pipeline into `claim_model.pkl` alongside encoder mappings.

### 3. Application Deployment (`app.py`)

* Created an interactive user interface allowing underwriters and users to select applicant inputs.
* Dynamically loaded serialized features (`model_columns.pkl`, `model_options.pkl`) to guarantee zero feature skew during inference.
* Displays instant risk predictions alongside claim probability scores.

---

## 📊 Key Insights & Business Value

* **High-Risk Segment Identification:** Identified demographic and vehicle profiles most correlated with claim frequency, allowing for better premium adjustments.
* **Feature Importance:** Isolated the key drivers influencing claim filings (e.g., vehicle age, driver profile, policy tier), empowering underwriters to make data-backed decisions.
* **Operational Efficiency:** The deployed Streamlit app reduces manual underwriting time by providing instant, automated risk assessments based on historical data patterns.

---

## 🚀 How to Run Locally

Follow these step-by-step instructions to set up the project and run the application on your local machine.

### Prerequisites

* **Python 3.8 or higher** installed on your system.
* **Git** installed to clone the repository.

### Step 1: Clone the Repository

Open your terminal or command prompt and run the following command to download the project files:

```bash
git clone [https://github.com/Anshulworld/Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project.git](https://github.com/Anshulworld/Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project.git)
cd Insurance-Claims-Prediction-with-Machine-Learning-Python-Data-Science-Project

```

### Step 2: Create a Virtual Environment (Recommended)

It is best practice to create a virtual environment to manage project dependencies without affecting your global Python installation.

* **For Windows:**
```bash
python -m venv venv
venv\Scripts\activate

```


* **For macOS/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate

```



### Step 3: Install Required Dependencies

With your virtual environment activated, install all the necessary Python libraries required to run the models and the web app:

```bash
pip install pandas numpy scikit-learn streamlit matplotlib seaborn

```

### Step 4: Verify Model Artifacts

Ensure that the following serialized Pickle files are present in your root directory (these are required for the app to make predictions):

* `claim_model.pkl`
* `model_columns.pkl`
* `model_options.pkl`

### Step 5: Launch the Web Application

Run the Streamlit server to start the interactive user interface:

```bash
streamlit run app.py

```

### Step 6: View in Browser

Once the server starts, Streamlit will provide a local network URL in your terminal. Open your web browser and navigate to:

```text
http://localhost:8501

```

You can now interact with the UI, input applicant data, and view real-time risk predictions!


