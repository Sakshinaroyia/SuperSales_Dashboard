# SuperSales_Dashboard
This interactive sales dashboard provides comprehensive insights into retail performance across multiple dimensions. Built with Power BI/Tableau, it transforms raw sales data into actionable business intelligence.
# 📊 SuperStore Sales Analytics Dashboard

![Dashboard Preview](screenshots/dashboard.png) *(Upload a screenshot and add path)*

## 🎯 Project Objective
Develop an interactive sales dashboard to:
- Analyze retail performance across regions, products, and customer segments
- Identify top-performing categories and underperforming markets
- Track payment trends and profitability (2019-2020)
- Enable data-driven decision making for business growth

## 📂 Dataset Used
**Dataset Characteristics**:
- **Type**: Synthetic retail data
- **Time Period**: 2019-2020
- **Records**: 1000+ transactions
- **Size**: ~2MB (CSV format)

**Key Fields**:
| Column | Description | Example |
|--------|-------------|---------|
| `OrderID` | Unique order identifier | CA-1001 |
| `OrderDate` | Date of transaction | 2020-01-15 |
| `Region` | Geographical division | East |
| `Category` | Product category | Technology |
| `SubCategory` | Product sub-category | Phones |
| `Sales` | Transaction amount | 620000 |
| `Profit` | Profit earned | 124000 |
| `PaymentMode` | Payment method | COD |

[Download Sample Dataset](data/sample_superstore.csv) *(Upload your dataset to `/data` folder)*

## 🔍 Key Business Questions (KPIs)
### 📈 Sales Performance
1. Which product category generates maximum revenue? *(Technology @ ₹0.62M)*
2. How do sales vary by region? *(East: 29% vs South: 10%)*
3. What is the month-over-month sales trend?

### 💰 Profit Analysis
1. Which products have highest profit margins?
2. How does discounting affect profitability?
3. Yearly profit comparison: 2019 vs 2020 *(₹175.26K total profit)*

### 👥 Customer Insights
1. Which customer segment dominates sales? *(Consumer: 48%)*
2. Payment mode preferences *(COD: 43%, Online: 35%)*

git clone https://github.com/yourusername/superstore-dashboard.git

Repository Structure
superstore-dashboard/
├── data/
│   ├── raw_sales.csv
│   └── cleaned_sales.csv
├── docs/
│   └── data_dictionary.md
├── screenshots/
│   ├── dashboard.png
│   └── data_model.png
├── SuperStore_Dashboard.pbix
└── README.md

## 🛠️ Technical Implementation
### ETL Process
```python
# Sample Data Cleaning Code (Python)
import pandas as pd

df = pd.read_csv('raw_sales.csv')
# Handle missing values
df['Profit'] = df['Profit'].fillna(0)
# Standardize categories
df['Category'] = df['Category'].str.title()
df.to_csv('cleaned_sales.csv', index=False)
