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

## 🔗 Data Sources

| Data | Source |
|---|---|
| Tesla & GameStop stock price history | [`yfinance`](https://pypi.org/project/yfinance/) API (sourced from Yahoo Finance) |
| Tesla quarterly revenue | Scraped from [revenue.htm](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm) |
| GameStop quarterly revenue | Scraped from [stock.html](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html) |

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
   git clone https://github.com/jun2717-prog/Analyzing-Historical-Data.git
   cd Analyzing-Historical-Data
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

---
---

# 📊 株価・収益ダッシュボード：Tesla vs. GameStop

**Tesla（TSLA）**と**GameStop（GME）**の過去の株価および収益データを抽出・加工・可視化するデータ分析プロジェクトです。APIによるデータ取得とWebスクレイピングを組み合わせ、比較可能な財務ダッシュボードを構築しました。

## 🎯 プロジェクト概要

金融アナリティクス企業のジュニアデータアナリストという想定で、投資家にとって本質的な問いに答えることを目指しました：**株価は実際の収益の動きとどれだけ連動しているのか？**

本プロジェクトでは、性質の異なる2つのデータソース（金融データAPI、およびスクレイピング対象のWebページ）から情報を取得し、クリーンなデータセットへと整形した上で、両社の株価と収益の推移を同じ時間軸上で可視化し、アナリストが着目すべきパターンを浮かび上がらせています。

## 🛠️ 使用技術

| 用途 | ツール・ライブラリ |
|---|---|
| 株価データ取得（API） | `yfinance` |
| Webスクレイピング | `requests`, `BeautifulSoup4` |
| データ加工 | `pandas` |
| 可視化 | `matplotlib` |
| 実行環境 | Jupyter Notebook |

## 🔗 データソース

| データ | 取得元 |
|---|---|
| Tesla・GameStopの株価履歴 | [`yfinance`](https://pypi.org/project/yfinance/) API（Yahoo Finance経由） |
| Teslaの四半期収益データ | [revenue.htm](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/revenue.htm) からスクレイピング |
| GameStopの四半期収益データ | [stock.html](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0220EN-SkillsNetwork/labs/project/stock.html) からスクレイピング |

## 📁 プロジェクトの内容

1. **株価データの取得**：`yfinance` APIを使用し、TeslaとGameStopの過去全期間の株価データ（始値・高値・安値・終値・出来高）を取得
2. **四半期収益データのスクレイピング**：株価APIでは取得できないため、`requests` + `BeautifulSoup`を用いてHTMLテーブルから両社の四半期収益データをスクレイピング
3. **データクレンジング**：生のHTMLを構造化されたDataFrameへ変換し、通貨表記（`$`記号・カンマ）を除去、null・空文字の行を除去
4. **2段構成のダッシュボード構築**：各社について、株価と収益の推移を同じ時間軸で並べて表示し、視覚的に比較できるグラフを作成

## 📈 主な考察

- **Tesla**：分析期間を通じて収益・株価ともに力強く持続的な成長を示しており、特に2020年以降は株価の上昇が加速。市場がTeslaの事業拡大という基礎的な要因を織り込んでいったことがうかがえます。
- **GameStop**：2021年頃に株価が急騰した一方（いわゆる「ミームストック」現象として広く知られる出来事）、同時期の収益は横ばい〜減少傾向。株価の値動きが事業の実態から**乖離**した典型的な事例です。

この対比こそが本ダッシュボードの核心的な示唆です：**株価と収益は必ずしも連動しない**ということが、両者を並べて可視化することで一目で分かります。

## 🚀 実行方法

1. リポジトリをクローンする：
   ```bash
   git clone https://github.com/jun2717-prog/Analyzing-Historical-Data.git
   cd Analyzing-Historical-Data
   ```

2. 必要なライブラリをインストールする：
   ```bash
   pip install yfinance bs4 pandas matplotlib nbformat
   ```

3. Notebookを開く：
   ```bash
   jupyter notebook Analyzing_Historical_Stock_Revenue_Data_and_Building_a_Dashboard.ipynb
   ```

4. 全セルを実行（`Run All`）し、データ抽出・クレンジング・ダッシュボードの可視化を再現する

## 📂 リポジトリ構成

```
├── Analyzing_Historical_Stock_Revenue_Data_and_Building_a_Dashboard.ipynb
└── README.md
```

## 🔧 このプロジェクトで示せるスキル

- `yfinance`によるAPIベースのデータ取得
- `requests`・`BeautifulSoup`を用いたWebスクレイピング
- HTMLテーブルの解析、およびゼロからのDataFrame構築
- データクレンジング（正規表現によるテキスト処理、null・空文字への対応）
- `matplotlib`による時系列データの可視化
- 財務データの比較分析とインサイトの言語化

---

*本プロジェクトは、Pythonの基礎、データ構造、Webスクレイピング、および金融データ分析のためのデータ加工に焦点を当てたハンズオン形式の学習課題として作成しました。*
