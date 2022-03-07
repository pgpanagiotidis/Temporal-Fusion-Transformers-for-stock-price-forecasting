# Temporal Fusion Transformers for stock price forecasting
In this project, we use Temporal Fusion Transformers to forecast the closing price of Pfizer. We use the approach proposed by Lim, Bryan, et al., "Temporal fusion transformers for interpretable multi-horizon time series forecasting." International Journal of Forecasting 37.4 (2021): 1748-1764 (https://www.sciencedirect.com/science/article/pii/S0169207021000637).
The Pfizer and AstraZeneca stocks prices were taken from the Yahoo Finance site. We follow two approaches:
1. We use the past 14 days' Pfizer closing prices to forecast the prices of the 3 following days (Pfizer stock closing price forecasting model.ipynb).
2. We enhanced the first model by giving as input also the past 14 days AstraZeneca closing prices to forecast the prices closing of the 3 following days of the  Pfizer stock (Pfizer stock closing price forecasting enhanced model.ipynb).

In both cases, the forecasts look rather accurate, although in the first case, the  Mean Absolute Error (MAE) is lower (i.e., 1.0167) compared to the second  (i.e., 1.7004). So, it seems that the AstraZeneca stock closing price as an input feature does not improve the forecast of Pfizer's stock closing price.
For the forecasts, used the PyTorch Forecasting (https://pytorch-forecasting.readthedocs.io/en/stable/index.html).
