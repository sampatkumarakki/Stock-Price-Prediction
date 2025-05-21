# Stock-Price-Prediction

# Stock Price Prediction - Amazon (AMZN)

## Objective
The goal of this project is to predict the closing stock price of Amazon (AMZN) using historical data from 2006 to 2018. This is achieved using Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models for time series forecasting.

## Dataset
- File: `AMZN_stock_data.csv`
- Total records: 3,019
- Columns: Date, Open, High, Low, Close, Volume, Name

## Models Used
The following models were trained and evaluated:

- Simple RNN  
- RNN with Hyperband Tuning  
- Simple LSTM  
- LSTM with Hyperband Tuning  

## Results

| Model                  | Mean Squared Error (MSE) | R² Score |
|------------------------|--------------------------|----------|
| Simple RNN             | 0.0085                   | 0.9305   |
| RNN with Hyperband     | 0.0194                   | 0.8417   |
| Simple LSTM            | 0.0096                   | 0.9213   |
| LSTM with Hyperband    | 0.1387                   | -0.1335  |

**Best Model**: Simple RNN  
It achieved the lowest error and highest R² score among all models tested.

## Conclusion
Among all the models, the Simple RNN performed best, showing the lowest Mean Squared Error and the highest R² score. While LSTM models are generally strong in time series prediction, in this case, the Simple RNN was more effective.

Hyperparameter tuning using Hyperband did not lead to performance improvements. In fact, the LSTM with Hyperband performed significantly worse, mostly due to elimination of best model prematurely due to less epochs.
