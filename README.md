📊 Trader Behavior vs Market Sentiment (Fear–Greed Analysis)

🔎 Problem Statement

Financial markets are strongly influenced by trader psychology.
This project investigates how market sentiment (Fear vs Greed) impacts trader performance, risk-taking behavior, and execution patterns on the Hyperliquid trading platform, with the goal of translating behavioral insights into actionable trading heuristics.

The analysis is designed to reflect real-world trading decision-making, focusing on risk management, behavioral shifts, and performance stability.

📂 Data Sources
1️⃣ Bitcoin Market Sentiment (Fear & Greed Index)

Daily sentiment classification: Fear / Greed

Used as a proxy for overall market psychology

2️⃣ Hyperliquid Trader Execution Data

Trade-level records including:

account, side, size, leverage, execution price, closed PnL, timestamp

Enables reconstruction of daily trader behavior and performance

🧠 Analytical Approach

The analysis follows a behavior-first framework:

Data Alignment

Trade-level executions aggregated to daily trader-level metrics

Sentiment aligned at daily granularity

Feature Engineering

Performance metrics: daily PnL, volatility (drawdown proxy)

Behavioral metrics: trade frequency, leverage, position sizing

Directional bias: long/short ratio

Comparative Analysis

Fear vs Greed performance comparison

Behavioral shifts under different sentiment regimes

Trader Segmentation

Grouping traders by leverage usage, activity level, and performance consistency

Segment-wise risk and return evaluation

📈 Key Findings (Data-Backed)
🔹 Insight 1: Sentiment Amplifies Risk, Not Skill

Trader PnL volatility increases significantly during Fear periods, while average returns do not improve proportionally—suggesting heightened emotional risk-taking rather than superior trade selection.

🔹 Insight 2: Leverage Is the Primary Failure Mode

High-leverage traders experience disproportionately larger drawdowns during Fear days, making leverage exposure the strongest predictor of underperformance under stress.

🔹 Insight 3: Consistency Outperforms Aggression

Traders with historically stable performance maintain better risk-adjusted outcomes across both Fear and Greed regimes compared to high-frequency or highly aggressive traders.

(All insights are supported by comparative plots and summary tables in the notebook.)

🎯 Actionable Trading Heuristics
1️⃣ Dynamic Leverage Throttling

Implement sentiment-aware leverage caps:
Reduce leverage during Fear periods, especially for high-volatility traders, to limit downside exposure.

2️⃣ Conditional Aggression Rule

Increase trade frequency or exposure only for historically consistent traders during Greed periods, while enforcing conservative limits for inconsistent traders.

These heuristics can be directly incorporated into risk controls or strategy filters for systematic trading systems.

🛠️ Tools & Stack

Python (Pandas, NumPy)

Matplotlib & Seaborn

Jupyter Notebook (reproducible workflow)

▶️ Reproducibility

Clone repository

git clone https://github.com/anuradhasingh0423-ship-it/trader-behavior-sentiment-analysis.git


Run notebook end-to-end

Trader_Behavior_vs_Market_Sentiment.ipynb

👤 Author

Anuradha Singh
Data Science | Analytics | AI-ML
