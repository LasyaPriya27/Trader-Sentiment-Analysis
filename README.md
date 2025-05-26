### Trader-Sentiment-Analysis
## 🎯 Objective
- Analyze the interplay between Bitcoin market sentiment (Fear & Greed Index) and trader performance (PnL, win rate, ROI, risk metrics).
- Identify top-performing traders across sentiment regimes.
- Highlight potential contrarian or momentum-based strategies.
- Present findings via notebook reports and an interactive dashboard.

---

## 📁 Repository Structure
```bash
primetrade-assignment/
├── data/
│   ├── historical_data_sample.csv   # Sample of Hyperliquid trades (10K rows)
│   └── fear_greed_index.csv         # Full sentiment index
├── notebooks/
│   ├── 01_data_preprocessing.ipynb  # Data cleaning, merging, features
│   ├── 02_exploratory_analysis.ipynb # EDA: distributions, heatmaps, insights
│   └── 03_advanced_analysis.ipynb   # Metrics: Sharpe, Sortino, clustering
├── output/
│   ├── sentiment_summary.csv        # Aggregated metrics per sentiment
│   ├── top_traders_by_sentiment.csv # Top traders per sentiment regime
│   ├── figures/                     # Visualizations as PNGs
│   └── dashboard/                   # Streamlit dashboard code
├── report/
│   └── insights_summary.pdf         # Key takeaways & recommendations
├── requirements.txt                 # Python dependencies
└── README.md                        # Project overview
```

### Data Sampling & Compression
- **Full dataset** is used locally for analysis.
- Only a **10,000-row sample** of `historical_data.csv` is included under `data/historical_data_sample.csv` to keep the repo light (~5 MB).
- Full `historical_data.csv` is shared via Google Drive link in `data/README.md`.



### Methodology
1. **Data Preprocessing** (`01_data_preprocessing.ipynb`)
   - Parse timestamps, standardize column names
   - Merge trade data with daily Fear & Greed classification
   - Compute derived metrics: PnL, ROI, win/lose flag, trade duration

2. **Exploratory Data Analysis** (`02_exploratory_analysis.ipynb`)
   - Visualized sentiment regimes and trader performance metrics
   - Summary statistics of PnL, ROI, win rate by sentiment
   - Correlation heatmap (sentiment value vs. performance metrics)
   - Identify outlier traders and anomalous periods
  
     
     ![image](https://github.com/user-attachments/assets/a807022d-c8e2-4f8c-bca8-350539edd80f)
     **Insight:** The proportion of trades in "Fear" regimes spikes around late 2023, coinciding with major Bitcoin drawdowns.
     

     ![image](https://github.com/user-attachments/assets/53acf066-3ff1-40e7-8ece-90db7b9a8f31)
     **Observation:** The median PnL in "Fear" periods shows higher variance, indicating riskier outcomes when sentiment is optimistic.
     

     ![image](https://github.com/user-attachments/assets/2ec404f7-35c6-41be-a37f-5a8a01075b06)




3. **Advanced Analysis** (`03_advanced_analysis.ipynb`)
   - Calculate performance ratios: Sharpe, Sortino, profit factor, max drawdown
   - Clustered trader performance using unsupervised learning (e.g., KMeans)
   - Time-series clustering of trader PnL curves to uncover behavioral archetypes
   - Machine learning: classify traders as contrarian vs. momentum based on sentiment-response patterns
   - Identified feature importance affecting performance

---

### Key Insights (Preview)
- **Extreme Greed Drives Gains:** Avg PnL and Sharpe ratio are highest during Greed and Extreme Greed phases.

- **Contrarian Traders Excel in Fear:** A small subset of traders thrive in Fear and Extreme Fear conditions.

- **Consistency Beats Extremes:** Traders with low drawdowns and stable ROI tend to perform better across all regimes.



---

### How to Run
1. Open the notebooks in Google Colab using the links below:
   - 01_data_preprocessing.ipynb
   - 02_exploratory_analysis.ipynb
   - 03_advanced_analysis.ipynb

2. Upload the following datasets manually when prompted:
   - historical_data.csv
   - fear_greed_index.csv

3. Run all cells in order.
