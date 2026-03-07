# Telecommunications Customer Churn Analysis Dashboard

## Overview
Customer churn is one of the most significant challenges in the telecommunications industry. Because acquiring new customers can cost significantly more than retaining existing ones, organizations must identify patterns that lead customers to leave their service.

This project analyzes telecommunications customer data and presents insights through an interactive Tableau dashboard designed to support executive decision-making. The goal of the dashboard is to help leadership identify churn drivers and develop strategies to improve customer retention.

---

## Business Problem
Telecommunications companies operate in highly competitive markets where customers can easily switch providers. Understanding **why customers churn** allows organizations to improve service reliability, adjust pricing strategies, and strengthen customer engagement.

This project explores the following questions:

- Which contract types have the highest churn rates?
- Are operational issues contributing to customer churn?
- Are there geographic patterns in churn behavior?
- Which customer characteristics may influence churn risk?

---

## Dataset
The dataset used in this project contains information on **10,000 telecommunications customers** across the United States.

### Data Categories
The dataset includes 50 variables grouped into the following categories:

**Customer Demographics**
- Age
- Income
- Marital status
- Gender
- Geographic location

**Customer Account Information**
- Contract type
- Payment method
- Monthly charges
- Customer tenure

**Operational Service Data**
- Weekly outage time
- Equipment failures
- Technical support contacts

**Product Features**
- Internet service
- Streaming services
- Security features
- Device protection

**Customer Survey Responses**
- Service reliability
- Responsiveness
- Customer experience indicators

---

## Dashboard Features

The Tableau dashboard provides interactive visualizations to help leadership explore churn trends.

### Key Metrics
- **Overall Churn Rate**
- **Average Monthly Charge of Churned Customers**

### Data Visualizations
- Churn Rate by Contract Type
- Geographic Churn Distribution (Map)
- Operational Drivers of Churn (Scatter Plot)
- Executive KPI Indicators

### Interactive Filters
- **State**
- **Contract Type**

These filters allow users to dynamically explore how churn patterns change across regions and customer segments.

---

## Tools Used

- **Tableau** – Interactive dashboard development  
- **Python** – Data preprocessing and analysis  
- **Jupyter Notebook** – Exploratory data analysis  
- **GitHub** – Version control and project documentation  

---

## Key Insights

Some initial insights from the analysis include:

- Month-to-month contracts show higher churn rates compared to long-term contracts.
- Service reliability issues such as outages and equipment failures appear to correlate with increased churn.
- Certain geographic regions demonstrate higher churn concentrations.
- Customers with higher monthly charges may exhibit greater churn sensitivity.

These insights can help organizations prioritize improvements in service reliability and customer engagement.

---

## Repository Structure

telecom-churn-dashboard

│

├── data/
│ └── Telecommunications_Churn_Data.csv
│

├── dashboard/
│ └── churn_dashboard.twbx
│

├── analysis/
│ └── churn_analysis.ipynb
│

└── README.md


---

## Future Improvements

Future iterations of this project may include:

- Predictive churn modeling
- Customer segmentation analysis
- Machine learning models for churn prediction
- Integration with real-time business intelligence tools

---

## Author

**Taylor Wilkerson**

- B.S. IT Management  
- M.S. Data Analytics (in progress)

Interested in financial technology, risk analytics, and data-driven strategy.
