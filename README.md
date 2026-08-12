# 📊 Stock & Revenue Dashboard: Tesla vs. GameStop

A data analysis project that extracts, cleans, and visualizes historical stock price and revenue data for **Tesla (TSLA)** and **GameStop (GME)**, combining API data retrieval and web scraping to build a comparative financial dashboard.

## 🎯 Project Overview

Acting as a Junior Data Analyst at a financial analytics firm, this project answers a core investor question: **how does a company's stock price relate to its actual revenue performance over time?**

The project collects data from two different sources — a financial data API and a scraped web page — merges them into clean datasets, and visualizes both companies' share price and revenue trends side by side to surface patterns human analysts would look for.

## 🛠️ Tech Stack

| Purpose | Tool / Library |
|---|---|
| Stock price data (API) | `yfinance` |
| Web scraping | `requests`, `BeautifulSoup4` |
| Data manipulation | `pandas` |
| Visualization | `matplotlib` |
| Environment | Jupyter Notebook |

## 📁 What This Project Does

1. **Extracts stock price data** for TSLA and GME using the `yfinance` API, pulling full historical price history (Open, High, Low, Close, Volume).
2. **Scrapes quarterly revenue data** for both companies from HTML tables using `requests` + `BeautifulSoup`, since this data isn't available via the stock API.
3. **Cleans the data** — parsing raw HTML into structured DataFrames, stripping `$` symbols and commas from currency values, and removing null/empty rows.
4. **Builds a two-panel dashboard** for each company, plotting historical share price against historical revenue on a shared timeline to visually compare the two trends.

## 📈 Key Insights

- **Tesla**: Both revenue and share price show strong, sustained growth over the analyzed period, with a especially sharp share price acceleration from 2020 onward — suggesting the market priced in Tesla's expanding fundamentals.
- **GameStop**: Share price spiked dramatically around 2021 (the well-documented "meme stock" event), while revenue over the same period stayed flat to declining — a clear case where price action **decoupled** from underlying business performance.

This contrast is the core takeaway of the dashboard: **stock price and revenue don't always move together**, and visualizing them side by side makes that gap immediately visible.

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<jun2717-prog>/<Analyzing-Historical-Data>.git
   cd <Analyzing-Historical-Data>
   ```

2. Install the required libraries:
   ```bash
   pip install yfinance bs4 pandas matplotlib nbformat
   ```

3. Open the notebook:
   ```bash
   jupyter notebook Analyzing_Historical_Stock_Revenue_Data_and_Building_a_Dashboard.ipynb
   ```

4. Run all cells (`Run All`) to reproduce the data extraction, cleaning, and dashboard visualizations.

## 📂 Repository Structure

```
├── Analyzing_Historical_Stock_Revenue_Data_and_Building_a_Dashboard.ipynb
└── README.md
```

## 🔧 Skills Demonstrated

- API-based data retrieval with `yfinance`
- Web scraping with `requests` and `BeautifulSoup`
- HTML table parsing and DataFrame construction from scratch
- Data cleaning: regex-based text processing, handling nulls/empty values
- Time-series data visualization with `matplotlib`
- Comparative financial analysis and insight generation

---

*This project was built as a hands-on lab exercise focused on Python fundamentals, data structures, web scraping, and data manipulation for financial data analysis.*
