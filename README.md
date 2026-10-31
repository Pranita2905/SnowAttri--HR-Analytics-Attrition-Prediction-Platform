# ❄️ SnowAttri — Snowflake-Powered HR Attrition & Predictive Analytics Platform

An end-to-end HR analytics and employee attrition prediction project integrating **Amazon S3, Snowflake, Python, Machine Learning, Streamlit, and Power BI** to transform HR data into actionable workforce insights.

## 📌 Project Overview

SnowAttri is a cloud-based HR analytics platform designed to analyze employee attrition patterns, identify potential workforce risks, and support data-driven HR decisions.

The project uses **Amazon S3 for cloud storage** and **Snowflake as the cloud data warehouse**. HR datasets are stored in Amazon S3 and loaded into Snowflake through a stage-based data ingestion workflow. Python is used for data processing, exploratory analysis, and predictive modeling, while Streamlit and Power BI provide interactive analytics and visualization.

## 🎯 Project Objectives

- Build a cloud-based HR data workflow using Amazon S3 and Snowflake.
- Load and manage HR datasets in a centralized data warehouse.
- Analyze employee attrition trends and workforce patterns.
- Identify factors associated with employee turnover.
- Develop a machine learning model to predict employee attrition.
- Create interactive dashboards for HR reporting and decision-making.

## 🏗️ System Architecture

```text
             HR Dataset (CSV)
                    |
                    v
              Amazon S3
            (Cloud Storage)
                    |
                    v
          Snowflake External Stage
                    |
                    v
          Snowflake Data Warehouse
                    |
                    v
           HR_ATTRITION_FINAL
                    |
          +---------+----------+
          |                    |
          v                    v
    Python Analytics       Power BI
          |              HR Dashboards
          v
    Machine Learning
    Attrition Model
          |
          v
       Streamlit
    Prediction App
```

## ☁️ Cloud Data Pipeline

### 1. Amazon S3 — Cloud Storage
- Stored HR dataset files in an Amazon S3 bucket.
- Used S3 as the cloud storage layer for the HR data workflow.
- Prepared the files for ingestion into Snowflake.

### 2. Snowflake — Cloud Data Warehouse
- Configured a Snowflake database, schema, and virtual warehouse.
- Created a stage to access HR files stored in Amazon S3.
- Loaded HR data into Snowflake tables.
- Used SQL to query and prepare data for analysis.
- Worked with the consolidated `HR_ATTRITION_FINAL` dataset.

### 3. Python — Data Processing & Analytics
- Connected Python to Snowflake.
- Retrieved HR data for analysis.
- Performed data cleaning and exploratory data analysis.
- Examined attrition across departments, job roles, salary groups, overtime, and employee tenure.

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Programming | Python, SQL |
| Cloud Storage | Amazon S3 |
| Cloud Data Warehouse | Snowflake |
| Data Analysis | Pandas, NumPy |
| Visualization | Plotly, Matplotlib, Seaborn |
| Machine Learning | Scikit-learn, XGBoost |
| Web Application | Streamlit |
| BI & Reporting | Microsoft Power BI |
| Development Tools | VS Code, Jupyter Notebook, Git, GitHub |

## 📊 Key Features

### 1. HR Data Integration
- Amazon S3-based HR dataset storage.
- Snowflake stage-based data ingestion.
- Centralized HR data management and SQL querying.

### 2. Exploratory Data Analysis
- Department-wise attrition analysis.
- Overtime and attrition relationship.
- Salary and attrition patterns.
- Employee tenure analysis.
- Workforce demographic analysis.

### 3. Predictive Analytics
- Machine learning-based employee attrition prediction.
- Model training and evaluation.
- Prediction functionality through a Streamlit application.

### 4. Interactive Streamlit Application
- HR Attrition Intelligence dashboard.
- Workforce analytics and KPI monitoring.
- Attrition prediction interface.
- Snowflake data integration.

### 5. Power BI Dashboard

The Power BI dashboard is organized into three analytical sections:

- **Executive Overview:** Workforce KPIs, employee attrition, department and job-role analysis.
- **Attrition Drivers:** Analysis of overtime, income, distance, satisfaction, performance, and age groups.
- **Risk Segmentation & Action List:** Employee risk-factor analysis and high-risk workforce identification.

## 📈 Business Value

SnowAttri helps HR teams:

- Understand employee attrition patterns.
- Identify workforce segments with higher attrition.
- Explore factors associated with employee turnover.
- Monitor important HR performance indicators.
- Use predictive analytics to support employee retention planning.

## 📁 Project Structure

```text
SnowAttri/
│
├── models/
│   └── attrition_model.pkl
│
├── outputs/
│   ├── attrition_by_department.png
│   ├── attrition_by_overtime.png
│   └── salary_vs_attrition.png
│
├── src/
│   ├── connect_snowflake.py
│   ├── eda.py
│   └── train_model.py
│
├── app.py
├── main.py
├── dashboard.pbix
├── requirements.txt
├── .gitignore
├── .env.example
└── README.md
```

*The virtual environment, credentials, and private configuration files should not be committed to GitHub.*

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/Pranita2905/SnowAttri--HR-Analytics-Attrition-Prediction-Platform.git

cd SnowAttri--HR-Analytics-Attrition-Prediction-Platform
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file in the project root using the following template:

```env
SNOWFLAKE_USER=your_username
SNOWFLAKE_PASSWORD=your_password
SNOWFLAKE_ACCOUNT=your_account_identifier
SNOWFLAKE_WAREHOUSE=hr_wh
SNOWFLAKE_DATABASE=hr_attrition
SNOWFLAKE_SCHEMA=raw
```

Use your own Snowflake account details. Never upload your actual `.env` file or credentials to GitHub.

### 5. Run the Streamlit application

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal to access the application.

## 🔐 Security

- Snowflake credentials are stored in environment variables.
- `.env` files and virtual environments are excluded through `.gitignore`.
- Do not commit confidential HR records or private cloud credentials.
- Configure appropriate AWS and Snowflake access permissions.

## 👩‍💻 Author

**Pranita Mothe**

Aspiring Data Scientist | Data Analyst | Machine Learning Enthusiast

- GitHub: https://github.com/Pranita2905
- LinkedIn: https://www.linkedin.com/in/pranita-mothe/

---

⭐ If you find this project interesting, feel free to explore the repository and share your feedback.

*Built to demonstrate practical skills in cloud data engineering, HR analytics, machine learning, and business intelligence.*
