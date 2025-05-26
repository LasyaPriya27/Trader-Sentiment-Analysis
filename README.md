# Trader-Sentiment-Analysis
Analyze the impact of Bitcoin market sentiment (Fear &amp; Greed) on trader behavior and performance using real Hyperliquid trading data. Includes data preprocessing, exploratory analysis, advanced metrics (Sharpe, Sortino), and behavioral clustering.

**Objective**
- Explore the relationship between Bitcoin market sentiment (Fear & Greed) and historical trader performance (PnL, win rate, ROI, risk metrics).
- Identify top-performing traders in each sentiment regime and uncover contrarian or momentum strategies.
- Present actionable insights via static report and interactive dashboard.

---

### Repository Structure
primetrade-assignment/
├── data/
│   ├── historical_data_sample.csv   # Sample of Hyperliquid trades (10K rows)
│   ├── fear_greed_index.csv         # Full sentiment index
│   └── README.md                    # Data summary & sampling note
├── notebooks/
│   ├── 01_data_preprocessing.ipynb  # Cleaning, merging, feature engineering
│   ├── 02_exploratory_analysis.ipynb # EDA with visualizations & correlation
│   └── 03_advanced_analysis.ipynb   # Sharpe, drawdown, clustering, ML
├── output/
│   ├── sentiment_summary.csv        # Aggregated metrics per sentiment
│   ├── top_traders_by_sentiment.csv # Ranked lists of traders
│   ├── figures/                      # PNGs of key plots
│   └── dashboard/                    # Streamlit app files
├── report/
│   └── insights_summary.pdf         # One-page summary report
├── requirements.txt                 # Python dependencies
└── README.md
