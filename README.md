# Stock Price Forecasting with Gated Recurrent Unit (GRU)

![Cover Image](https://github.com/Brianhulela/GRU_stock_price_forecasting/blob/master/TSLA_test_predictions_close.png)

This repository contains the code for forecasting stock prices using Gated Recurrent Units (GRU) and Python. The model is trained to predict future stock trends based on historical market data.

The key steps of the process include:
1. **Data Preprocessing**: The dataset is first scaled using the **MinMaxScaler**, which normalizes the features to a range between 0 and 1. This is critical for training deep learning models and ensuring stable convergence during optimization.
  
2. **Sliding Window Approach**: A sliding window technique is used to create a time-series dataset. This means the model is trained on sequences of past data (e.g., 30 days) to predict the next day's values. This approach captures temporal dependencies crucial for stock price forecasting.
   
3. **Model Building**: The core of the model is a **GRU (Gated Recurrent Unit)** network, designed to handle sequential data. It is chosen over traditional methods like Linear Regression due to its ability to capture long-term dependencies, and its computational efficiency compared to more complex models like **LSTM (Long Short-Term Memory)**. A dropout layer is included to prevent overfitting.

4. **Model Evaluation**: The performance of the model is evaluated using metrics such as **Mean Absolute Error (MAE)**, **Mean Squared Error (MSE)**, and **R² Score**. The accuracy of predictions is visualized by plotting the predicted and actual closing prices, along with a 95% confidence interval for the predictions.

5. **Future Price Prediction**: After training the model, it can forecast future stock prices (e.g., for the next 30 days) based on the most recent data. A confidence interval is also generated for future predictions to quantify uncertainty.

For a detailed explanation of the approach and methodology, check out the accompanying article on [Medium](https://medium.com/@brianhulela/stock-price-forecasting-gated-recurrent-unit-gru-e17a6760047b).

Feel free to explore and adapt the code for your own forecasting tasks.
