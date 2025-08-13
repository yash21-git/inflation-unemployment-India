# Inflation-Unemployment Chronicles — India’s Economic Timeline
Applied econometric analysis of India’s inflation (1960–2024) and unemployment (1991–2024) using Python in Google Colab. Includes EDA, statistical tests, AR/ARIMA/VAR models, forecasts, and real-world event insights with annotated visualizations.

# Project Overview
This project analyses the historical trends of inflation (1960–2024) and unemployment (1991–2024) in India using time series modeling and statistical techniques.It combines exploratory data analysis, model fitting (AR, ARIMA, VAR), and real-world event interpretation to explain economic fluctuations.

# Objectives
1.) Visualize long-term inflation & unemployment trends.
2.) Test for stationarity and identify autocorrelation patterns.
3.) Build AR(1), ARIMA, and VAR models for forecasting.
4.) Link data spikes/drops to historical economic events.

# Tools & Technologies
Python (Pandas, Matplotlib, Statsmodels, NumPy)
Jupyter Notebook / Google Colab
Statistical modeling & diagnostics

# Skills Demonstrated
1.) Data Cleaning & Preparation (structuring time series data)
2. ) Data Visualization (annotated line plots, ACF/PACF)
3.) Statistical Analysis (ADF stationarity tests, autocorrelation)

4.) Time Series Modeling:
   a.) Autoregressive models (AR)
   b.) ARIMA forecasting
   c.) Vector Autoregression (VAR)

5.) Interpretation & Storytelling:
    a.) Connecting trends to real-world events like:
    b.) 1974 Oil Shock (inflation spike)
    c.) 1991 Balance-of-Payments Crisis (inflation surge)
    d.) 2020 COVID-19 Pandemic (unemployment spike)

# Real-World Insights

1.) 1974 Inflation Spike (28.6%) — First Oil Shock (OAPEC embargo) → fuel price surge → inflation rise.

2.) 1976 Negative Inflation (-7.6%) — Commodity price drop & base effect post-oil crisis.

3.) 1991 Inflation Surge (13.9%) — Balance-of-payments crisis, rupee devaluation, IMF reforms.

4.) 2020–21 Unemployment Spike — COVID-19 lockdowns, job losses, slow recovery.

# DATA SOURCE : INFLATION (https://www.macrotrends.net/global-metrics/countries/ind/india/inflation-rate-cpi)
# UNEMPLOYMENT (https://www.macrotrends.net/global-metrics/countries/ind/india/unemployment-rate)

## Phillips Curve Analysis (1991–2024)

In this section, we test the **Phillips Curve** hypothesis — the inverse relationship between inflation and unemployment — using India's data from 1991 to 2024.

** Methodology:
- Used annual unemployment data (1991–2024) and inflation data for the same period.
- Ran an **OLS regression**: Unemployment ~ Inflation
- Plotted the scatter plot with a regression line.

** Results:
- Coefficient on Inflation: **+0.0652** (positive, not negative)
- p-value: **0.241** (> 0.05) → Not statistically significant
- R²: **0.043** (very weak explanatory power)

** Interpretation:
- The classic Phillips Curve expects a **negative relationship** — higher inflation leading to lower unemployment in the short run.
- For India (1991–2024), the coefficient is positive and insignificant, indicating **no strong evidence** of the Phillips curve.
- This could be due to structural unemployment, a large informal labor sector, and supply shocks like COVID-19 and global oil price changes.

** Economic Interpretation

The regression results indicate no strong evidence of a Phillips curve relationship for India during 1991–2024. The positive but insignificant coefficient suggests that inflation and unemployment moved largely independently in this period. This can be explained by India's large informal labor market, persistent structural unemployment, and frequent supply-side inflation shocks (e.g., food prices, oil imports) that raise prices without boosting employment. Policy measures like MNREGA and subsidies may have further weakened the short-run trade-off between inflation and unemployment.


# LIMITATIONS
The unemployment data in my analysis is only available from 1991 onwards while inflation data spans 1960–2024. This creates a mismatch in coverage that limits the scope of joint analysis. Any direct inflation–unemployment relationship, such as the Phillips curve, can only be studied from 1991 onwards, meaning earlier inflation spikes like the 1974 oil shock cannot be directly related to unemployment trends. It also means that VAR modeling, which requires both series to share the same time span, can only be applied to the post-1991 subset. As a result, we miss the opportunity to study long-term dynamics across different structural phases of the economy. Furthermore, India's labor market underwent significant reforms in the 1990s including liberalization, globalization and technology adoption which changed its behavior. Findings from 1991–2024 may not fully generalize to earlier decades. I have therefore clearly stated in my documentation that all joint analyses are based on the overlapping period and must be interpreted in that historical context.





