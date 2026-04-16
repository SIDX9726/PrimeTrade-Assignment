# PrimeTrade-Assignment

Project Overview
This project analyzes the relationship between Bitcoin Market Sentiment (Fear/Greed Index) and trader behavior/performance on the Hyperliquid exchange. The objective is to identify patterns in profitability, risk (drawdown), and behavioral shifts to propose actionable trading strategies

 Data Preparation (Part A)The analysis was performed using two datasets provided: Bitcoin Market Sentiment and Historical Trader Data.Data Cleaning: Initial documentation of row/column counts (211,224 entries for trader data) and verification of null values.Time Alignment: Standardized "Timestamp IST" and "Date" columns using dayfirst=True to ensure accurate daily-level merging.Metric Engineering: Created key performance indicators (KPIs) including Daily PnL, Win Rate (PnL > 0), and Trade Size (USD)

 2. Analysis & Insights (Part B)
We addressed the core questions regarding sentiment-driven performance with data-backed evidence:

Performance Variance
Win Rate: Analysis reveals that Extreme Greed environments yield the highest win rate (46.5%), while Extreme Fear sees a significant drop to 37.1%.

PnL Distribution: Median profitability is noticeably higher during Greed phases, while Fear regimes are characterized by higher variance and outlier losses.

Behavioral Shifts
Traders show a distinct Long Bias during Greed phases.

Volatility in position sizes increases during Neutral and Fear days, suggesting less disciplined risk management during uncertainty.

Trader Segmentation (Archetypes)
Using behavioral clustering, I identified three primary segments:

High-Frequency  Trader: Frequent participants with positive total PnL.

High-Variance  Trader: High-frequency participants with negative PnL, likely due to over-leveraging.

Low Position Trader: Selective participants who prioritize quality over quantity.

3. Predictive Modeling (Bonus)
To add predictive depth, I developed a Random Forest Classifier to predict the probability of a "Win" day based on:

Current Market Sentiment Index (Value).

Trader-specific behavior (Trade frequency and average size).

Outcome: The model identifies sentiment as a primary driver of next-day profitability, validating the importance of sentiment-aware trading.

4. Actionable Strategies (Part C)
Based on the findings, I propose the following "Rules of Thumb":


Strategy 1 (Risk Mitigation): During Extreme Fear days, enforce a 30% reduction in position size for High-Variance traders to protect against the 37% low win-rate environment.

Strategy 2 (Performance Optimization): Increase API limits and execution frequency for Alpha Traders during Extreme Greed to capitalize on the 46.5% win-rate momentum.

5. How to Run
Dependencies: Ensure you have pandas, seaborn, scikit-learn, and matplotlib installed.


Execution: Run the Assignment.ipynb notebook from top to bottom
