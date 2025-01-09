# Bitcoin Price Prediction using LSTM

This project aims to predict the future price of Bitcoin using historical data. The model employs a Long Short-Term Memory (LSTM) neural network, a type of Recurrent Neural Network (RNN), to forecast Bitcoin prices based on past data.

## Overview

The dataset consists of daily Bitcoin prices, including the `Open`, `High`, `Low`, `Close`, and `Volume` for each day. The LSTM model is trained using the historical data to make predictions about future prices.

Key Features:
- Visualizes the Bitcoin price data for different years (2014-2019).
- Analyzes monthly Bitcoin price trends.
- Trains an LSTM model to predict Bitcoin closing prices.
- Visualizes actual vs predicted Bitcoin prices.

## Requirements

- Python 3.x
- Libraries:
  - pandas
  - numpy
  - sklearn
  - matplotlib
  - tensorflow
  - plotly

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone <repository-url>
   ```

2. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Dataset

The dataset used in this project is `BTC-USD.csv`, which contains the following columns:
- `Date`: Date of the Bitcoin price record.
- `Open`: The price at which Bitcoin opened for the day.
- `High`: The highest price Bitcoin reached that day.
- `Low`: The lowest price Bitcoin reached that day.
- `Close`: The price at which Bitcoin closed for the day.
- `Adj Close`: The adjusted closing price (not used in this model).
- `Volume`: The trading volume for that day (not used in this model).

## Data Preprocessing

The dataset is first cleaned to remove any unnecessary columns (`Adj Close`, `Volume`). The data is then normalized using MinMaxScaler to ensure that the LSTM model receives inputs within a specific range.

## Model Architecture

- The model consists of an LSTM layer followed by a dense output layer.
- The LSTM layer is used to capture the time-series dependencies in the Bitcoin price data.
- The output layer is used to predict the closing price for the next day.

## Training the Model

1. **Train and Test Split**: The data is split into training and test datasets.
2. **Model Training**: The LSTM model is trained using the training data.
3. **Prediction**: The model predicts Bitcoin closing prices on the test data.

## Visualizations

- **Monthly Average**: The average `Open` and `Close` prices for each month.
- **High/Low Comparison**: Monthly high and low Bitcoin prices.
- **Price Trend**: A line chart showing the historical Bitcoin prices for multiple years.

## Results

- **Performance Metrics**: The model’s performance is evaluated using metrics like Mean Squared Error (MSE) and R-squared.
- **Predicted vs Actual**: A comparison between the predicted Bitcoin prices and the actual prices.

## Usage

To run the entire process, including data preprocessing, model training, and prediction, simply run the following script:

```bash
python bitcoin_price_prediction.py
```

## Future Enhancements

- Implementing hyperparameter tuning for model optimization.
- Using additional features like trading volume for better predictions.
- Incorporating more advanced techniques like Attention Mechanism for better prediction performance.

## License

This project is licensed under the MIT License.

---
