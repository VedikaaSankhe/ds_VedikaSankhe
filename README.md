# Trader Behavior Insights – ds_VedikaSankhe

## Project Overview
This project analyzes how **trader behavior** — including profitability, risk exposure, trading volume, and activity — aligns or diverges from **market sentiment**, as represented by the Bitcoin **Fear & Greed Index**.

The analysis combines:
- **Historical Trader Data (Hyperliquid)**
- **Bitcoin Market Sentiment Dataset**

The objective is to uncover hidden behavioral patterns, sentiment-driven performance shifts, and insights that can guide smarter, data-driven trading strategies.

---

## 🎯 Objective
To explore the relationship between trader performance metrics (profit/loss, trading volume, and activity) and overall market sentiment (Fear vs Greed), and to identify how emotional market behavior impacts real trading outcomes.

---

## 📂 Datasets
1. **Hyperliquid Trader Data**
   - Rows: 211,224  
   - Columns: 16  
   - Key fields: `Account`, `Execution Price`, `Size USD`, `Side`, `Closed PnL`, `Fee`, `Timestamp IST`

2. **Bitcoin Fear & Greed Index**
   - Rows: 2,644  
   - Columns: `timestamp`, `value`, `classification`, `date`  
   - Sentiment categories: *Extreme Fear, Fear, Neutral, Greed, Extreme Greed*

---

## ⚙️ Data Processing Summary
- Cleaned and standardized timestamp columns into a unified `date` format.
- Engineered daily aggregates:
  - `daily_pnl`, `daily_volume_usd`, `daily_fees`, `avg_execution_price`, `num_trades`
- Merged both datasets on `date`.
- Encoded sentiment as a binary variable (`1` = Greed, `0` = Fear).

**Final merged dataset shape:** 470 rows × 10 columns

---

## 🔍 Key Findings
| Aspect | Observation |
|--------|--------------|
| **Profitability** | Average daily PnL decreases during Extreme Greed phases. |
| **Trading Volume** | Volume and number of trades rise sharply during Greed periods. |
| **Risk Behavior** | Greed sentiment correlates with higher exposure and volatility. |
| **Market Psychology** | Fear reduces activity but yields more consistent performance. |

---

## 📊 Visual Outputs
All visualizations are saved in the `outputs/` folder:
- `sentiment_distribution.png` – Frequency of Fear vs Greed days  
- `avg_pnl_vs_sentiment.png` – Average PnL comparison across sentiments  
- `volume_vs_sentiment.png` – Trading volume variation with sentiment  
- `correlation_heatmap.png` – Correlation between trading and sentiment metrics  
- `sentiment_pnl_trend.png` – Time-based trend of sentiment vs profitability  

---

## 🧠 Insights
- Market optimism (Greed) leads to increased trading volume and activity.  
- Profitability tends to decline during Extreme Greed, suggesting riskier and more emotional decision-making.  
- Fear phases result in lower participation but more stable outcomes.  
- Sentiment influences trader intensity more than performance quality.

---

## 🚀 Future Work
Potential extensions of this analysis include:
- Predictive modeling to forecast next-day profitability from sentiment metrics.  
- Lag correlation analysis to examine how today’s sentiment affects next-day performance.  
- Clustering traders into behavioral groups (high-risk, conservative, consistent).  

---

## 🛠️ Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn  
- **Environment:** Google Colab  
- **Version Control:** GitHub  

---

## 📂 Folder Structure
ds_VedikaSankhe/
├── notebook_1.ipynb
├── csv_files/
│ ├── historical_data.csv
│ ├── fear_greed_index.csv
│ └── daily_sentiment_plus_metrics.csv
├── outputs/
│ ├── sentiment_distribution.png
│ ├── avg_pnl_vs_sentiment.png
│ ├── volume_vs_sentiment.png
│ ├── correlation_heatmap.png
│ └── sentiment_pnl_trend.png
├── ds_report.pdf
└── README.md

---

## 🏃 How to Run
1. Open `notebook_1.ipynb` in **Google Colab**.  
2. Mount Google Drive and ensure all CSV files are located in `/csv_files/`.  
3. Run all cells sequentially to reproduce the analysis.  
4. Generated visuals will automatically save in the `/outputs/` folder.  

---

## 👩‍💻 Author
**Vedika Sankhe**  
Email: [vsankhe240@gmail.com](mailto:vsankhe240@gmail.com)  

---

## 📄 License
This project was developed as part of a Data Science hiring assignment for **PrimeTrade.ai**.  
All datasets are used strictly for educational and evaluation purposes.
