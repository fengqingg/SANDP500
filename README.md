# S&P500 Analysis

<p align="center">
<img width="1100" alt="image" src="https://user-images.githubusercontent.com/85885666/236658670-402c15fb-7a62-4640-9218-9cb6ef31a5e9.png">
</p>

As a beginner investor, I'm always looking for ways to improve my investment strategy and make more informed decisions. One of the key tools in my arsenal is forecasting, which can help me predict when to buy and sell stocks.

In this notebook, I'll be using historical data of the S&P500 from kaggle, which is an index of 500 large-cap stocks traded on the US stock market. Then I'll be analyzing the data of the stock to see the trend and seasonality of the data. Finally, I'll build models to forecast future prices and compare their performance.

I'll be exploring two popular time series forecasting techniques: ARIMA and LSTM. ARIMA(AutoRegressive Integrated Moving Average) is a classic statistical model that's been used for decades while LSTM(Long Short-Term Memory) is a type of neural network that's become increasingly popular in recent years.

## Data Analysis
The moving average (MA) is a simple technical analysis tool that smooths out price data by creating a constantly updated average price. The average is taken over a specific period of time. This allows the user to analyse the general trend of the market and gain insights.
<p align="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660172-17a66e86-33d6-4f19-af8b-565bf076768d.png">
</p>

### Seasonality
In Time Series data, seasonality is the presence of variations that occur at specific regular intervals less than a year, such as weekly, monthly, or quarterly. It is useful to analyze if the data has such trend so that we can improve the performance of modeling with machine learning.
<p align="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660234-d855308f-e8c7-4cb8-858a-bec23198ea18.png">
</p>

<p align ="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660260-92cca0a1-08aa-452c-9f4f-4cc493f82cc4.png">
</p>

### Correlation
Correlation quantifies the degree of a linear relationship between two variables. It is useful to analyse the correlation to see how sequential observations in a time series affect each other. If we can find structure in these observations then it will likely help us improve our forecasts and simulation accuracy.
<p align="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660288-d8ae8e6c-6ba8-41e6-8715-02cf29a4c6b0.png">
</p>

## Long Short-Term Memory
LSTM is a type of recurrent neural network that is particularly useful for working with sequences of data, such as time series data. It is designed to handle the issue of vanishing gradients, which can occur when training deep neural networks by using a more complex structure that includes gates to control the flow of information. LSTM models are able to remember past data and use that information to predict future data points, making them well-suited for time series forecasting
<p align="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660321-51545591-01ba-417e-acb4-f7bd85081730.png">
</p>

## Auto Regressive Integrated Moving Average 
Autoregressive Integrated Moving Average (ARIMA) is a popular statistical model for analyzing time series data. ARIMA models are based on the assumption that a time series can be described as a combination of an autoregressive component, a moving average component, and a differencing component. The autoregressive component models the dependence of the current value on previous values, the moving average component models the dependence on past errors, and the differencing component removes any trend or seasonality in the data. ARIMA models are widely used for forecasting future values of a time series, as well as for identifying trends, cycles, and other patterns in the data.
<p align="center">
<img width="1129" alt="image" src="https://user-images.githubusercontent.com/85885666/236660347-9de483b6-a0f1-4c94-8f28-d4bf3b7c3c7f.png">
</p>

## Conclusion
In conclusion, both LSTM and ARIMA are powerful techniques for time series analysis and each has its own advantages and limitations. LSTM is particularly effective in handling complex, high-dimensional sequences and can capture non-linear relationships between variables, while ARIMA is better suited for modeling linear relationships and stationary time series.

However, in the given dataset, LSTM outperformed ARIMA, indicating that the dataset may have complex and non-linear patterns. Therefore, an LSTM model may be better suited to capture such patterns and provide more accurate predictions.

|      | ARIMA |  LSTM |
|:----:|:-----:|:-----:|
| RMSE | 6.234 | 82.7% |
|  MAE | 5.343 | 80.4% |

It is worth noting that there are other models to explore, such as the Prophet model, which may also be suitable for this dataset. Thus, it is important to consider the characteristics of the dataset and the goals of the analysis when selecting the appropriate time series model.

## Requirements
To run the notebook, you will need to have Python 3 and the following libraries installed:

<ol>
  <li>numpy</li>
  <li>pandas</li>
  <li>matplotlib</li>
  <li>seaborn</li>
  <li>sklearn</li>
  <li>tensorflow</li>
  <li>keras</li>
  <li>pmdarima</li>
  <li>statsmodels</li>
</ol>
You can install these packages by running the following command using pip:
<code>pip install numpy pandas matplotlib seaborn sklearn tensorflow keras pmdarima statsmodels</code>

## Usage
To use this notebook, you can either download it directly from the repository or clone the entire repository to your local machine. Once you have the notebook, you can open it using Jupyter Notebook or JupyterLab. 

To run the notebook, you can execute each cell in sequence. The notebook includes detailed explanations of each step and how the function is created. You can import different stocks from the S&P500 to see how they perform with this two model.

## Dataset
The sandp500 is a comprehensive dataset that contains information of the 500 stocks that are traded in the US stock market. Each of the company stock can be found in the individual_stocks_5yr folder. In this notebook, we will be using Apple stock AAPL_data.csv to do the forecasting.

You can find the dataset from the following link: https://www.kaggle.com/datasets/camnugent/sandp500

## License
The code in this repository is licensed under the MIT License. See [LICENSE.md](LICENSE.md) for more information.
