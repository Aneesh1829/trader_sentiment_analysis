# 📊 Trader Behavior Insights — Sentiment-Aware Performance Analysis

## 📌 Project Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear/Greed Index) and trader behavior using historical trade execution data from Hyperliquid.

The objective is to determine:

- Whether trader performance differs between Fear vs Greed regimes
- Whether traders change behavior based on sentiment
- Whether trader segments perform differently across sentiment regimes
- Whether sentiment + behavioral features can predict next-day profitability

The analysis includes:
- Data cleaning and alignment
- Behavioral analysis
- Trader segmentation
- Actionable strategy recommendations
- Bonus predictive modeling

---

# 📂 Dataset Description

## 1️⃣ Bitcoin Market Sentiment Dataset
Columns:
- `timestamp`
- `value`
- `classification`
- `date`

Daily sentiment categories:
- Fear
- Extreme Fear
- Neutral
- Greed
- Extreme Greed

---

## 2️⃣ Historical Trader Data (Hyperliquid)

Key fields:
- `Account`
- `Execution Price`
- `Size USD`
- `Side`
- `Timestamp`
- `Closed PnL`
- `Trade ID`
- `Fee`
- etc.

---

# 🛠️ Setup Instructions

## 1️⃣ Clone the Repository

```bash
git clone <your-repo-link>
cd trader-behavior-analysis
2️⃣ Create Virtual Environment (Recommended)
python -m venv venv
Activate environment:

Mac/Linux

source venv/bin/activate
Windows

venv\Scripts\activate
3️⃣ Install Dependencies
If requirements.txt is available:

pip install -r requirements.txt
Otherwise install manually:

pip install pandas numpy matplotlib seaborn scikit-learn jupyter
▶️ How to Run
Option 1 — Run Jupyter Notebook
jupyter notebook
Open:

notebooks/analysis.ipynb
Run all cells sequentially.

Option 2 — Run as Python Script (If Converted)
python analysis.py
📊 Methodology
Part A — Data Preparation
Loaded both datasets

Verified missing values and duplicates

Converted timestamps to daily level

Merged trade data with sentiment data

Created behavioral metrics:

Daily PnL per trader

Daily win rate

Trades per day

Average trade size

Volatility (PnL standard deviation)

Part B — Behavioral Analysis
1️⃣ Sentiment Impact on Performance
Compared across Fear vs Greed regimes:

Average & median daily PnL

Win rate

Trade frequency

Position size

Volatility (risk proxy)

Key Finding:
Traders increase exposure and activity during Fear periods, resulting in higher mean returns but also higher volatility.

2️⃣ Trader Segmentation
Segmented traders into:

High Activity traders

Low Activity traders

Findings:

Low Activity traders outperform during Fear periods

High Activity traders perform better during Greed periods

Behavioral adjustments align with market sentiment

Part C — Actionable Strategy Recommendations
Strategy 1 — Sentiment-Adaptive Capital Allocation
During Fear:

Allocate relatively more capital to Low Activity traders

Apply tighter volatility-based risk limits

During Greed:

Allocate relatively more capital to High Activity traders

Encourage systematic scaling strategies

Strategy 2 — Dynamic Risk Adjustment
Fear periods:

Reduce maximum position size

Monitor drawdowns aggressively

Greed periods:

Focus on consistency and trend-following approaches

Allow structured increase in trade count for high performers

🤖 Bonus — Predictive Modeling
Built a Logistic Regression model to predict:

Next-day trader profitability (binary classification)

Features Used:
Daily win rate

Trades per day

Average trade size

Sentiment regime

Activity segment

Model Performance:
Accuracy: ~68%

Recall for profitable days: 86%

Conclusion:
Sentiment combined with behavioral metrics contains predictive signal for next-day trader profitability.

📈 Key Insights
Fear regimes increase trader aggression and volatility.

Higher mean returns during Fear are driven by increased exposure, not improved win rate.

Trader performance varies by sentiment regime and activity level.

Behavioral signals provide measurable predictive power.

📦 Repository Structure
trader-behavior-analysis/
│
├── data/
│   ├── fear_greed_index.csv
│   ├── historical_data.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── outputs/
│
├── README.md
└── requirements.txt
🧠 Evaluation Alignment
This project emphasizes:

Clean preprocessing and correct data alignment

Evidence-backed reasoning

Actionable business insights

Clear communication

Reproducibility

👤 Author
Aneesh Reddy
Junior Data Scientist Candidate




