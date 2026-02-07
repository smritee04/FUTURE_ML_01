# FUTURE_ML_01 – Sales & Demand Forecasting

**Domain:** Machine Learning  
**Track Code:** ML  
**Internship ID:** [FIT/JAN26/ML5123]

## Task Overview
This project focuses on forecasting future sales using historical retail data. It is part of the Machine Learning Internship at **Future Interns**, aimed at providing actionable business insights for inventory management and strategic planning.

## Dataset
- **Name:** Sample Superstore Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **Description:** Contains 9,900+ rows of order-level retail information, including Order Date, Sales, Region, and Category.

## Tools & Libraries
- **Language:** Python 3.x
- **Environment:** Jupyter Notebook / VS Code
- **Libraries:** - `Pandas` & `NumPy`: Data manipulation and cleaning
  - `Matplotlib` & `Seaborn`: Data visualization
  - `Scikit-learn`: Model building and evaluation (Random Forest Regressor)
  - `Statsmodels`: Time-series decomposition

## Methodology
1. **Data Preprocessing:** Handled missing values and converted date columns into standard datetime format.
2. **Aggregation:** Resampled daily transactional data into Monthly Sales to identify seasonal patterns.
3. **Feature Engineering:** Extracted `Year`, `Month`, and created a `Time_Index` to capture growth trends.
4. **Modeling:** Implemented a **Random Forest Regressor** to handle non-linear relationships and seasonality.
5. **Evaluation:** Measured performance using Mean Absolute Error (MAE).

## Model Performance
- **Mean Absolute Error (MAE):** [$11453.74]

## Visualizations

### 1. Historical Monthly Sales Trend (2014 - 2017)
Before forecasting, I analyzed the historical data to identify underlying patterns. The chart below reveals a strong upward trend and consistent year-end spikes, which are critical for model training.
![Monthly Sales Trend](Monthly Sales Trend.png)

### 2. Model Validation (Actual vs. Forecasted)
To ensure reliability, I split the data and compared the model's predictions for 2017 against the actual recorded sales. The red dashed line closely follows the green actuals, confirming the model's accuracy.
![Sales Validation](sales_validation.png)

### 3. Future 12-Month Sales Projection (2018)
Using the Holt-Winters Exponential Smoothing model trained on the full dataset, I generated the following forecast for 2018. This serves as the primary deliverable for business planning.
![Projected Sales 2018](Projected Monthly Sales for 2018.png)


## Business Insights
- **Seasonality:** Analysis confirms a recurring sales peak every **November and December**, likely due to holiday season demand.
- **Growth Trend:** The store shows a consistent upward trend year-over-year.
- **Actionable Insight:** It is recommended that the Superstore increase stock levels for "Technology" and "Furniture" categories by 15-20% starting in late October to prevent stockouts during peak months.

## Project Structure
FUTURE_ML_01/
├── data/
│   └── Superstore.csv
├── notebooks/
│   ├── task1_sales_forecasting.ipynb
│   ├── Monthly Sales Trend.png
│   ├── sales_validation.png
│   └── Projected Monthly Sales for 2018.png
└── README.md


## 🚀 Conclusion
This project demonstrates the application of Machine Learning in retail demand forecasting. By accurately predicting future sales, businesses can optimize supply chains and improve customer satisfaction.
