# Telco Customer Churn: Segmentation & Advanced Analysis

An end-to-end analysis of customer churn at a telecommunications company, covering data cleaning, exploratory analysis, tenure-based customer segmentation, and advanced churn analysis, ending with actionable retention recommendations.

> Completed as part of the Business Analysis Internship at SaiKet Systems.

## Business Problem

Customer churn directly hurts revenue. This project identifies **who** is leaving, **when** they leave, and **which factors** are linked to churn, so the business can focus retention efforts where they matter most.

## Dataset

- **Source:** Telco Customer Churn dataset (public sample dataset)
- **Size:** 7,043 customers, of whom 1,869 churned (about 26.5%)
- **Features:** demographics (gender, senior citizen), account information (tenure, contract type, payment method), subscribed services, monthly and total charges, and a churn flag

## Project Workflow

| Step | Notebook | What I did |
|------|----------|------------|
| 1. Data understanding and cleaning | `01_data_understanding_and_cleaning.ipynb` | Loaded the data, checked types and missing values, removed duplicates, standardized column names |
| 2. Exploratory data analysis | `02_exploratory_data_analysis.ipynb` | Summary statistics (mean, median, mode), histograms, box plots, churn vs. non-churn proportions |
| 3. Customer segmentation | `03_customer_segmentation.ipynb` | Tenure groups (0-12, 13-36, 37+ months) with pie/donut charts and clustered bar charts of monthly charges |
| 4. Advanced analysis | `04_advanced_analysis.ipynb` | Churn by tenure, gender, senior citizen status, payment method, contract type, and lifecycle stage |

## Key Findings

- **Tenure is the strongest signal.** Churn falls from **47.44%** (0-12 months) to **25.54%** (13-36 months) to **11.93%** (37+ months). New customers are about 4 times more likely to leave than long-term customers.
- **New customers drive most of the churn.** About 55% of all churned customers (1,037 of 1,869) left within their first 12 months.
- **Contract type matters.** Month-to-month customers churn at **42.71%**, compared with **2.83%** for two-year contracts.
- **Payment method matters.** Electronic check users churn the most (**45.29%**); automatic-payment users churn the least (about 15-17%).
- **Senior citizens churn more:** **41.68%** vs. 23.61% for non-seniors.
- **Gender has almost no effect:** 26.92% (female) vs. 26.16% (male).
- **Riskiest segment:** new, month-to-month customers, at **51.4%** churn.
- **Long-term customers are more valuable.** Average monthly charges rise with tenure (56.10 → 63.25 → 72.01), and average total charges grow from about 275 to 1,514 to 4,214.

## Visualizations

<!-- Replace these with your own exported charts (saved in the images/ folder) -->
![Customer distribution by tenure](images/tenure_distribution.png)
![Churn rate by tenure group](images/churn_by_tenure.png)
![Churn rate by contract type](images/churn_by_contract.png)

## Recommendations

1. Offer discounts or rewards to move month-to-month customers onto 1- or 2-year contracts.
2. Encourage automatic payments (bank transfer or credit card) with a small incentive.
3. Run a strong onboarding and support program during the customer's first 12 months.
4. Give senior citizens dedicated support and simpler plans.

## Tech Stack

Python, pandas, NumPy, Matplotlib, Seaborn, Plotly, Jupyter Notebook (VS Code)

## Repository Structure

```
telco-churn-customer-segmentation/
├── data/
│   ├── raw/telco_customer_churn.csv
│   └── processed/telco_cleaned.csv
├── notebooks/
│   ├── 01_data_understanding_and_cleaning.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_customer_segmentation.ipynb
│   └── 04_advanced_analysis.ipynb
├── images/
├── requirements.txt
└── README.md
```

## How to Run

```bash
git clone https://github.com/chinmang3-ui/telco-churn-customer-segmentation.git
cd telco-churn-customer-segmentation
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Then open the notebooks in the `notebooks/` folder in order (01 to 04) using VS Code or Jupyter.

## Author

**Mang Chin Par**
[GitHub](https://github.com/chinmang3-ui) | [LinkedIn](https://www.linkedin.com/in/your-profile)
