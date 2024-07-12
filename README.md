# Introduction

The disruptive impacts of climate change have created an urgent need to transition to a low-carbon economy, with a significant part of this transition involving the increased use of clean energy. This greater adoption of clean energy is opening up new opportunities for clean energy equity investing.

Existing literature primarily focuses on the dynamic relationships between clean energy equities, oil prices, technology stock prices, and other critical macroeconomic variables such as market volatility and economic policy uncertainty. However, there is a notable gap in the literature regarding the forecasting of clean energy stock prices, which is crucial for making informed investment decisions.

This paper aims to address this gap by employing machine learning methods to predict clean energy stock prices. Initially, the primary objective of the project was to predict the direction of clean energy stock prices. However, I chose to use a regressor model, reasoning that even if there were some loss, the model would still provide high-precision directional forecasts.

## Feature Prediction

**Independent Features:**  
The chosen independent features included the Oil Volatility Index (OVX), the Volatility Index (VIX), metal prices such as zinc (HZNC), and the Economic Policy Uncertainty (EPU) index as non-technical indicators. Additionally, technical indicators included the Williams Accumulation/Distribution (WAD) and moving averages (MA20, MA10).

**Model Selection:**  
Initially, a basic Long Short-Term Memory (LSTM) model was employed to predict the future prices of these independent features. Although this model achieved an R² of up to 0.85 for some stocks, it required optimization for improved accuracy.

**Model Optimization:**  
By refining the LSTM model, I enhanced the prediction accuracy, achieving an R² exceeding 0.95.

## Price Prediction of JSW Energy Stocks

After predicting the independent features, I employed a Support Vector Machine (SVM) to train a model for predicting the price of JSW Energy stocks. This approach resulted in an R² of 0.91. To further improve accuracy, I used a Random Forest Regressor with 500 trees, which significantly enhanced the R² to 0.99, outperforming the SVM regressor model.

## Correlation Analysis

The primary motive of the project was to analyze how the prices of clean energy stocks correlate with market volatility and economic policy uncertainties. Utilizing SHAP (SHapley Additive exPlanations) graphs, I visually represented the correlations. The analysis revealed that technical indicators had a high correlation, with MA10 having the maximum and MA20 the minimum correlation among them. Among non-technical indicators, OVX showed the highest correlation, followed by VIX, metal prices, and EPU prices.
