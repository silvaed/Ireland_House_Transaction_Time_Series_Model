### README File

---

# Property Transactions Forecasting in Ireland

This project aims to forecast property transaction volumes in Ireland for the upcoming year using data from the **Residential Property Price Register** over the past 10 years. Using Facebook’s **Prophet** library, we developed a time series model to understand trends and predict future transaction volumes based on historical data.

## Project Structure

- **Time_Series_Ireland_House_Market.ipynb**: Main Jupyter Notebook containing the entire analysis, from data cleaning to model evaluation and prediction.
- **data/**: Folder containing the property transaction data from the Residential Property Price Register (not provided here; download separately if necessary).
- **README.md**: Project overview and instructions.

## Requirements

- Python 3.8 or newer
- Libraries: pandas, numpy, matplotlib, seaborn, fbprophet (or prophet), scikit-learn

Install dependencies with:

```bash
pip install -r requirements.txt
```

## Project Workflow

### 1. Data Collection

- Data was collected from the **Residential Property Price Register**, covering transaction records from the past 10 years.

### 2. Data Preprocessing

- Cleaned the data, handled missing values, and filtered for relevant entries.
- Treated **outliers** by identifying and capping extreme values to prevent skewing the model.

### 3. Exploratory Data Analysis (EDA)

- Analyzed seasonal patterns, transaction trends, and monthly/yearly variations.
- Visualized transaction volume over time to understand key patterns and potential anomalies.

### 4. Feature Engineering

- Added features like month, year, and seasonal indicators to capture periodic trends and improve model accuracy.

### 5. Building and Training the Model

- Used **Prophet**, a time series forecasting tool, with custom settings for **floor** and **cap** to restrict predictions to realistic transaction volumes.
- **Logistic Growth Model**: Chose this to allow the model to adapt to trends while staying within practical limits.
  
### 6. Model Evaluation

- Evaluated using **Mean Squared Error (MSE)** and **Root Mean Squared Error (RMSE)** to assess model accuracy.
- Fine-tuned parameters to improve predictions, especially for capturing seasonal trends accurately.

### 7. Forecasting Future Transactions

- Forecasted property transactions for the next year, providing monthly estimates based on past trends and patterns.
- Presented insights to stakeholders for better decision-making in the property market.

## Key Insights

- **Seasonality**: The model identified seasonal peaks in transactions, with higher activity in certain months.
- **Trends**: Long-term trends in the data helped the model capture market behavior effectively.

## How to Use

1. **Run the Jupyter Notebook**: Open `Time_Series_Ireland_House_Market.ipynb` in Jupyter Notebook or JupyterLab and execute cells in order.
2. **Input Data**: Make sure to provide the data from the Residential Property Price Register in the appropriate format.
3. **Adjust Parameters**: Modify `periods` or frequency settings in the forecast if you want different prediction ranges.

## Results

The model provides a monthly forecast for property transactions in Ireland, helping users understand expected activity levels for the coming year.

