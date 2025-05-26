# Trader-Sentiment-Analysis
Analyze the impact of Bitcoin market sentiment (Fear &amp; Greed) on trader behavior and performance using real Hyperliquid trading data. Includes data preprocessing, exploratory analysis, advanced metrics (Sharpe, Sortino), and behavioral clustering.

**Objective**
- Explore the relationship between Bitcoin market sentiment (Fear & Greed) and historical trader performance (PnL, win rate, ROI, risk metrics).
- Identify top-performing traders in each sentiment regime and uncover contrarian or momentum strategies.
- Present actionable insights via static report and interactive dashboard.

---

### Repository Structure


---

### Data Sampling & Compression
- **Full dataset** is used locally for analysis.
- Only a **10,000-row sample** of `historical_data.csv` is included under `data/historical_data_sample.csv` to keep the repo light (~5 MB).
- Full `historical_data.csv` is shared via Google Drive link in `data/README.md`.

---

### Methodology
1. **Data Preprocessing** (`01_data_preprocessing.ipynb`)
   - Parse timestamps, standardize column names
   - Merge trade data with daily Fear & Greed classification
   - Compute derived metrics: PnL, ROI, win/lose flag, trade duration, drawdown

2. **Exploratory Data Analysis** (`02_exploratory_analysis.ipynb`)
   - Distribution of sentiment regimes over time
   - Summary statistics of PnL, ROI, win rate by sentiment
   - Correlation heatmap (sentiment value vs. performance metrics)
   - Identify outlier traders and anomalous periods

3. **Advanced Analysis** (`03_advanced_analysis.ipynb`)
   - Calculate performance ratios: Sharpe, Sortino, profit factor, max drawdown
   - Time-series clustering of trader PnL curves to uncover behavioral archetypes
   - Machine learning: classify traders as contrarian vs. momentum based on sentiment-response patterns
   - Feature importance: which market conditions drive PnL most

4. **Dashboard & Reporting**
   - **Streamlit App** under `output/dashboard/`: interactive filters by sentiment, trader, date range
   - Static **Insights Summary** (`report/insights_summary.pdf`) with key takeaways and recommendations

---

### Key Insights (Preview)
- **Momentum in Extreme Greed**: Avg PnL peaks at ~68 in Extreme Greed, Sharpe ratio highest in moderate Greed.
- **Contrarian Stars**: 5 accounts maintain positive PnL in Extreme Fear—ideal for mean-reversion strategies.
- **Risk Profiles**: Traders with lower max drawdown during volatile regimes deliver more stable returns.

---

### How to Run
1. Clone the repo: `git clone https://github.com/yourname/primetrade-assignment.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Launch notebooks in order or run:
   ```bash
