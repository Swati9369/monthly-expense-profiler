# Monthly Expense Profiler 

A Python data analysis pipeline built to process, clean, analyze, and visualize personal financial data using **NumPy**, **Pandas**, and **Matplotlib**.

## Project Overview
This project demonstrates an automated **Data Engineering Pipeline** that generates, cleans, and analyzes a 30-day personal expense dataset across 4 categories (*Food*, *Transport*, *Entertainment*, *Utilities*).

Rather than requiring manual entry of 120 separate data points, the pipeline uses **Synthetic Data Ingestion**—generating a realistic expense matrix scaled dynamically to a user's specified monthly budget.

## Key Features
- **End-to-End Pipeline:** Ingestion $\rightarrow$ Cleaning $\rightarrow$ NumPy Analytics $\rightarrow$ Visual Reporting.
- **Reproducible Data Ingestion:** Uses `np.random.seed()` to generate consistent synthetic testing data scaled to your budget.
- **Data Cleaning (Pandas):** Imputes missing values (`NaN`) using column mean replacement.
- **NumPy Vectorization:** High-performance matrix mathematics without Python `for` loops:
  - `axis=0`: Category total calculations.
  - `axis=1`: Daily spending total calculations.
  - **Broadcasting:** Instant currency conversion from USD to INR (₹83.50 rate).
  - **Boolean Masking:** Automatic threshold detection for over-budget days.
- **Visual Analytics:** Dual-chart display featuring category breakdowns (INR) and daily trend tracking against custom budget limits.

## Tech Stack
- **Python 3.x**
- **NumPy** (Matrix math & vectorization)
- **Pandas** (Data cleaning & DataFrame handling)
- **Matplotlib** (Data visualization)

## How to Run
1. Open the project in Google Colab: [![Open In Colab](https://colab.research.google.com/drive/1N0_h8aJkYn1HVU1xRCVSek8DA0zdrZCP?usp=sharing)
2. Run the code cell.
3. Enter your preferred **Monthly Budget** and **Daily Spending Limit** when prompted.

## Sample Output
- **Text Report:** Total spending in USD/INR, category totals, and flagged over-budget days.
- **Bar Chart:** Total expenditure by category in Indian Rupees (₹).
- **Line Chart:** 30-day expense trend with a red threshold line indicating daily budget limits.
