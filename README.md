# Primetrade-Trader-Behavior-Analysis

## Project Overview
This project analyzes the relationship between **Bitcoin Market Sentiment (Fear & Greed Index)** and **Historical Trader Performance**. The goal is to uncover hidden patterns in trader behavior to understand how market sentiment influences trading decisions, leverage usage, and overall profitability (PnL).

This analysis was completed as part of the hiring process for the **Junior Data Scientist** role at **Primetrade.ai**.

## Datasets Used
* **Historical Trader Data:** Contains individual trade details including execution price, size, side (buy/sell), leverage, and closed PnL.
* **Fear & Greed Index:** Daily sentiment classification (e.g., Fear, Greed, Neutral) for the crypto market.

## Methodology
1.  **Data Preprocessing:**
    * Converted timestamps from both datasets into a unified datetime format.
    * Normalized trade timestamps to match the daily resolution of the Sentiment Index.
2.  **Data Merging:**
    * Performed an inner join on the `Date` column to align specific trades with the market sentiment of that day.
3.  **Exploratory Analysis:**
    * Grouped data by `Classification` (Sentiment) to calculate total PnL, average PnL per trade, and trade volume.
    * Analyzed leverage usage across different sentiment states.
4.  **Visualization:**
    * Created bar charts to visualize the correlation between sentiment categories and trader profitability.

## Key Insights
* **Profitability:** The analysis suggests that **"Extreme Greed"** correlates with the highest Average PnL per trade, indicating traders perform better when the market is optimistic.
* **Risk:** Trades executed during **"Extreme Fear"** showed the lowest average performance, suggesting panic trading may lead to suboptimal outcomes.
* **Volume:** High trade counts were observed during "Fear" periods, indicating increased market activity during downturns.

## Tech Stack
* **Python** (Data Analysis)
* **Pandas** (Data Manipulation & Merging)
* **Matplotlib / Seaborn** (Data Visualization)

## How to Run
1.  Clone the repository.
2.  Ensure `historical_data.csv` and `fear_greed_index.csv` are in the root directory.
3.  Run the analysis script:
    ```bash
    python trader_analysis.py
    ```

---
*Submitted by [Sambodhi Barsagade]*
