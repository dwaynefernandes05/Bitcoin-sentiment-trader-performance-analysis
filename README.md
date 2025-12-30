# Bitcoin Market Sentiment & Trader Performance Analysis

##  Overview
Financial markets are heavily influenced by human psychology. In cryptocurrency markets, sentiment-driven behavior often leads to suboptimal trading decisions.  
This project explores the relationship between **Bitcoin market sentiment (Fear & Greed Index)** and **trader performance data** from Hyperliquid to uncover behavioral patterns and derive insights that can inform smarter trading strategies.

The analysis focuses on how sentiment impacts:
- Trader profitability
- Capital deployment behavior
- Trade direction effectiveness
- Performance consistency across sentiment regimes

---

##  Datasets Used

### 1. Bitcoin Market Sentiment Dataset
Provides daily market sentiment indicators.

**Columns:**
- `timestamp`
- `value` (numeric sentiment score)
- `classification` (Fear / Greed)
- `date`

[Fear & Greed Index](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing)

---

### 2. Historical Trader Data (Hyperliquid)
Contains detailed trade-level information for individual traders.

**Key Columns:**
- `Account`
- `Coin`
- `Execution Price`
- `Size Tokens`
- `Size USD`
- `Side`
- `Direction`
- `Closed PnL`
- `Fee`
- `Timestamp`
- `Trade ID`

[Historical Data](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

---

##  Methodology

1. **Data Cleaning & Alignment**
   - Converted timestamps to date format
   - Merged daily sentiment data with trade-level records
   - Removed non-trade rows introduced during merging

2. **Feature Engineering**
   - Profitability indicator (`Is_Profitable`)
   - Capital-normalized return (`Closed PnL / Size USD`)
   - Net PnL after fees
   - Absolute exposure as a proxy for trader risk behavior
   - Trader segmentation based on historical performance

3. **Exploratory Data Analysis**
   - Performance comparison across Fear vs Greed regimes
   - Position sizing behavior under different sentiments
   - Direction-based return analysis (Long vs Short)
   - Capital efficiency assessment
   - Identification of hidden trader performance patterns

---

##  Key Insights

- **Greed-driven markets** encourage higher capital deployment but result in more volatile and less consistent returns.
- **Fear periods** exhibit better capital efficiency and higher win rates especially for disciplined traders.
- **Contrarian strategies** (long during Fear, short during Greed) outperform sentiment-aligned trades on average.
- **High-skill traders** maintain profitability across sentiment regimes while low-skill traders suffer disproportionately during Greed.
- Each dollar deployed during Fear generates **higher PnL efficiency** compared to Greed periods.

---

##  Strategic Implications

- Incorporating market sentiment into position sizing decisions can significantly improve risk-adjusted performance.
- Sentiment-aware trade direction selection offers an edge over naive momentum-based strategies.
- Trader segmentation reveals that behavioral discipline, not aggression, drives long-term profitability.

---

##  Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---
