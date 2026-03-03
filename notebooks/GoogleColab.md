## 📊 Notebook 1: Exploratory Data Analysis (EDA)

### Objective
Explore the Superstore dataset to uncover sales patterns, 
profitability trends, and key business insights.

### Steps Performed
- Loaded and inspected the dataset (shape, dtypes, missing values)
- Feature Engineering: extracted Year, Month, and Profit Margin columns
- Converted Order Date & Ship Date to datetime format

### Visualizations
- Total Sales by Region (bar chart)
- Total Profit by Category (bar chart)
- Monthly Sales Trend over years (line chart)
- Discount vs Profit scatter plot (with break-even line)
- Sub-Category Profit analysis (highlighting loss-makers in red)
- Customer Segment analysis — Sales & Profit (pie charts)

### Key Findings
- West region leads in total sales
- Technology is the most profitable category
- Furniture (especially Tables & Bookcases) consistently loses money
- Orders with 40%+ discount almost always result in losses
- ~18.7% of all orders are loss-making

## 🤖 Notebook 2: Machine Learning Model

### Objective
Build a Profit Prediction model and a Sales Forecasting model 
to support data-driven business decisions.

### Models Used
| Model | Purpose |
|-------|---------|
| Facebook Prophet | Sales Forecasting for next 6 months |
| Random Forest Classifier | Predict if an order will be Profitable or Not |

### Steps Performed
- Sales Forecasting with Prophet (yearly seasonality)
- Feature Engineering: created binary target `Is_Profitable`
- Label Encoding of categorical features
- Train-Test Split (80/20)
- Random Forest model training (100 estimators)
- Confusion Matrix & Classification Report
- Feature Importance analysis
- Exported clean data, forecast & feature importance CSVs for Power BI

### Model Performance
- ✅ High accuracy in predicting profitable vs loss orders
- 🔑 Discount is the #1 feature driving profitability (importance ~0.6)
- Sub-Category, Sales, and Quantity are next most important features

### Exported Files
- `superstore_clean.csv` — cleaned dataset
- `sales_forecast.csv` — 6-month forecast with upper/lower bounds
- `feature_importance.csv` — feature importance scores
