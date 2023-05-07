# StockForecast

**Objective**:

Extract stock data of any one company from https://finance.yahoo.com/. Per hour per IP address one can pass 2000 requests, on an average. (note: there might be frequent changes to the request count by Yahoo Finance). Build a pipeline to extract the data on ongoing basis and forecast stock (long term and short term). Adjusted closing price must be forecasted.


## Architecture

![Screenshot 2023-05-07 at 3 16 32 PM](https://user-images.githubusercontent.com/105431583/236670166-0b819fa6-6b85-4971-ae40-f679d52ce849.png)

## Data Collection & Preparation

- Collection from yahoo finance, with option for user to change the stock. Data is collected from 1st Jan 2010 to last working date.
- The historical stock data with relevant financial metrics was collected to build a forecasting model with enhanced accuracy. User has the liberty of selecting a stock and compare with market index such as DJIA.
- Removed missing data, removed redundant features such as Open Price, High/Low etc
- Scaling or transformation for modeling using Min Max Scaler
- Engineered features like Return Price, Moving Average and Risk

![Screenshot 2023-05-07 at 3 20 54 PM](https://user-images.githubusercontent.com/105431583/236670395-fee530eb-94a1-4fcb-a9cc-13ac4aea49b8.png)

## Modelling

- LSTM is a type of recurrent neural network (RNN) that is well-suited for time-series data analysis. It was used to capture long-term dependencies and relationships between different data points over time.
- LSTM can learn from past data to make predictions about future trends. This is useful for stock forecasting since historical data can provide insight into patterns and trends that can inform future predictions.

![Screenshot 2023-05-07 at 3 25 37 PM](https://user-images.githubusercontent.com/105431583/236670594-f8ae1c18-650c-4710-9514-847a966d103b.png)

## Evaluation

- MAPE & RMSE are used as standard evaluation metrics to assess the robustness of the LSTM model. 
- The below images displays our model performance on predicting the stock price of Apple Inc. 

![Screenshot 2023-05-07 at 3 26 44 PM](https://user-images.githubusercontent.com/105431583/236670643-80a7e043-d690-4e5f-9ef6-2d59c72e85cf.png)

## Deployment

- The model was deployed on Streamlit Cloud
- https://archiesrii-fp-2-1--homepage-wcewkn.streamlit.app/


