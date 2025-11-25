# Predicting-Price-Moves-with-News-Sentiment
# Predicting Price Moves with News Sentiment

## Project Overview
This project investigates the relationship between financial news sentiment and stock market movements. By analyzing headlines, calculating sentiment scores, and computing technical indicators, we explored how news impacts daily stock price fluctuations. The project demonstrates practical applications in Data Engineering, Financial Analytics, and Machine Learning Engineering.

---

## Business Objective
Nova Financial Solutions aims to improve its predictive analytics by leveraging news sentiment. The objectives of this project were:

1. **Sentiment Analysis** – Quantify the tone of financial news headlines and link sentiment scores to stock symbols.
2. **Correlation Analysis** – Measure the statistical correlation between news sentiment and stock price changes.
3. **Predictive Insights** – Provide actionable insights on how sentiment can be used to anticipate stock price movements.

---

## Dataset Overview

**Financial News and Stock Price Integration Dataset (FNSPID):**

- **headline**: News article title, often including key financial actions.
- **url**: Link to the full article.
- **publisher**: Author or organization publishing the article.
- **date**: Publication date and time (UTC-4).
- **stock**: Stock ticker symbol (e.g., AAPL, MSFT).

**Stock Price Data:** Daily OHLCV data for tickers `AAPL, AMZN, GOOG, MSFT, META, NVDA`.

---

## Completed Tasks

### Task 1 – Data Understanding and EDA
- Set up Python environment, Git, and repository structure.
- Conducted Exploratory Data Analysis:
  - Descriptive statistics (headline length, publisher counts, publication frequency).
  - Time series analysis of article publication trends.
  - Text analysis to extract keywords and potential topics (e.g., "FDA approval", "price target").
  - Publisher analysis to identify most active sources.

**Key Deliverable:** `notebooks/task1_eda.ipynb`

---

### Task 2 – Quantitative Analysis
- Loaded and prepared stock price data in pandas.
- Calculated **technical indicators**:
  - Moving Averages (MA20, MA50)
  - Relative Strength Index (RSI14)
  - MACD (with signal line and histogram)
- Calculated **financial metrics**:
  - Daily returns
  - Log returns
  - 30-day rolling volatility
- Created visualizations to understand stock trends and indicator impact.

**Key Deliverable:** `notebooks/task2_quantitative.ipynb`  
**Artifacts:** `outputs/merged_features.parquet`

---

### Task 3 – Correlation Between News and Stock Movement
- Normalized dates in both news and stock datasets for alignment.
- Performed **sentiment analysis** on news headlines using VADER.
- Calculated daily stock returns.
- Aggregated daily sentiment scores.
- Computed correlation between sentiment and daily stock returns to quantify the relationship.

**Key Deliverable:** `notebooks/task3_correlation.ipynb`  

---

## Project Structure

├── .vscode/
│ └── settings.json
├── .github/
│ └── workflows/unittests.yml
├── .gitignore
├── requirements.txt
├── README.md
├── src/
│ ├── init.py
├── notebooks/
│ ├── task1_eda.ipynb
│ ├── task2_quantitative.ipynb
│ └── task3_correlation.ipynb
├── tests/
│ ├── init.py
└── scripts/
├── get_prices.py
├── compute_indicators.py
└── init.py


---

## How to Run

1. Clone the repository and create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
pip install -r requirements.txt

2.Run notebooks in order:

task1_eda.ipynb

task2_quantitative.ipynb

task3_correlation.ipynb