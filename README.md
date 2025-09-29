# Rossmann Sales Forecasting  

This project focuses on **forecasting six weeks of daily sales** for 1,115 Rossmann drugstores across Germany. Using historical sales data and store attributes, it demonstrates the workflow of **data preprocessing, exploratory data analysis (EDA), and machine learning modelling**.  
 

## Dataset  
The datasets are provided by the **[Kaggle Rossmann Store Sales competition](https://www.kaggle.com/competitions/rossmann-store-sales)**.  

- `train.csv` – Daily sales records (Jan 2013 – July 2015)  
- `test.csv` – Test period (Aug – Sept 2015, no sales/customers)  
- `store.csv` – Store metadata (store type, assortment, competition, promotions)  

Due to GitHub’s file size limit (25 MB), the CSVs are **not included** in this repository. Please download them directly from Kaggle if you wish to reproduce the results.  


## Methodology  
- **Data Preprocessing**  
  - Imputed missing values in competition and promotion features using Random Forest.  
  - Encoded categorical variables (`StoreType`, `Assortment`, `PromoInterval`).  
  - Engineered temporal features (`Year`, `Month`, `WeekOfYear`, `Day`).  

- **Exploratory Data Analysis (EDA)**  
  - Sales distribution and seasonality trends.  
  - Effects of promotions, holidays, and competition.  
  - Variability across stores, types, and assortments.  

- **Forecasting Model**  
  - Random Forest Regressor to capture non-linear relationships.  
  - Evaluation using RMSE and R².  
  - Feature importance analysis to identify key sales drivers.  


## Results  
- **Training RMSE**: ~304  
- **Validation RMSE**: ~813  
- **Training R²**: 0.99  
- **Validation R²**: 0.96  

Key insights:  
- Promotions and store opening status strongly influence sales.  
- Competition distance and store type also affect performance.  
- December shows seasonal peaks in demand.  


## How to Run  
1. Clone this repository:  
   ```bash
   git clone https://github.com/USERNAME/rossmann-sales-forecasting.git
   cd rossmann-sales-forecasting
   ```
2. Open the notebook:  
   ```bash
   jupyter notebook rossmann_sales_forecasting.ipynb
   ```
3. Download the dataset from Kaggle and place it in the project folder before running.  

