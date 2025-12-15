# Stock Price Predictor

This project uses **Random Forest** to predict the direction of stock price changes. Using historical data from the Nifty50 index (Indian stock market), the project first creates new features of rolling averages and trends and then builds a:
**Random Forest Classifier** to predict whether the stock price will increase or decrease.

### Running the Project:

1. **Training and testing the Model**:
   `stock_predictor.ipynb` --> This notebook pulls historical data from the Nifty50, trains a Random Forest Classifier and Regressor, and saves the models as `stockpred.pkl` and `price_change_predictor.pkl`.

2. **Use the Model**:
   Scroll down ,This notebook loads the saved models and tests them on new stock data. Modify the `new_data` DataFrame in this notebook to test predictions on your own data.

## Installation and Setup

### Requirements:
Install the required libraries:
```bash
pip install yfinance pandas scikit-learn joblib
```


## How the Models Work

The **Classifier**: Predicts whether the stock price will go up or down based on features such as `Close`, `Volume`, `Open`, `High`, and `Low`.
  
### Example Output:
From `stock_predictor.ipynb`:
```python
new_data = pd.DataFrame({
    'Close': [25127.95],
    'Volume': [206400],
    'Open': [25023.45],
    'High': [25159.75],
    'Low': [25017.50]
})
```
#### output
```output
Predictions for new data: [0] #0 means the price will go down
```

## Conclusion

This project provides a basic model for predicting daily stock price movements and changes using machine learning. It was build as my capstone project for CBSE 2025 AI practical.
