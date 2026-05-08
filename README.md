# STL-Decomposition
STL Decomposition to find Cyclical Patterns in Automobile Sales
# STL Decomposition of Automobile Sales (1976–2026)
## Analyzing Cyclical Patterns and Macroeconomic Correlation

### 📊 Project Overview
This project focuses on decomposing the **Business Cycle** impact on the Indian Automobile industry. By applying **STL (Seasonal-Trend decomposition using Loess)**, this analysis separates long-term growth trends and seasonal fluctuations from the underlying cyclical patterns, which are then compared against GDP growth rates over a 50-year horizon.

### 🛠 The Problem
Automobile sales are highly sensitive to both seasonal trends (festive seasons, year-end sales) and the broader economic climate. The goal of this study is to:
1. Isolate the **Seasonal** and **Trend** components to see the "true" cyclical noise.
2. Correlate the cyclical movements in auto sales with **Quarterly GDP Data** (1976–2026) to detect lead or lag indicators of economic health.

### 🖼 Business Cycle Synchronization
The following visualization illustrates the synchronization between Automobile Sales and Real GDP from 1976 to 2026. By isolating the deviations from the trend, we can observe how the auto industry reacts to broader economic shifts.

![Auto Sales vs GDP Synchronization](BUSINESS_CYCLE_VS_GDP.png)

**Statistical Validation:** 
The analysis yielded a **Correlation Coefficient of 0.4787**, indicating a moderate-to-strong positive synchronization between the two cycles. Significant downturns, particularly around 2008 and 2020, show near-perfect alignment in volatility.

### 📉 Methodology: STL Decomposition
Unlike simple moving averages, STL decomposition provides a robust way to handle seasonality that may change over time.
* **Trend Component:** Captures the long-term expansion of the automobile sector.
* **Seasonal Component:** Isolates quarterly fluctuations (e.g., Q4 festive peaks).
* **Remainder/Cycle:** This is where the "Business Cycle" lives. This component was analyzed against GDP data to observe how closely auto sales track with the national economy.

### 🚀 Technical Implementation
* **Data Alignment:** Merged quarterly automobile sales with quarterly GDP data (1976–2026).
* **Log Transformation:** Applied to stabilize variance across the 50-year timeline.
* **Decomposition:** Executed using Python’s `statsmodels` library.
* **Correlation:** Analyzed cyclical residuals against GDP growth to visualize the impact of major economic shifts.

### 📁 Repository Contents
* `STLdecomposition.ipynb`: Jupyter Notebook containing the Python implementation for STL decomposition and visualization.

### 🧰 Tech Stack
`Python` | `Pandas` | `Statsmodels` | `Matplotlib` | `Seaborn`
