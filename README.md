# ============================================================
# 📊 Crypto Trade Sentiment EDA
# ============================================================

# ------------------------------------------------------------
# 📌 Project Overview
# ------------------------------------------------------------
# This project studies the relationship between trader
# performance and market sentiment using the Crypto
# Fear & Greed Index.
#
# Instead of predicting price direction, the analysis
# focuses on understanding how sentiment affects:
#   - Trader behavior
#   - Risk-taking
#   - Execution style
#   - Probability of winning
#
# The study is conducted at a per-trade level to preserve
# behavioral signals that are usually lost in aggregated data.

# ------------------------------------------------------------
# 🎯 Objectives
# ------------------------------------------------------------
# - Analyze how market sentiment impacts:
#     • Trade size
#     • Execution aggressiveness
#     • Win rate
#     • Risk-adjusted returns
#     • Loss severity
# - Identify sentiment regimes that are favorable or risky
# - Extract insights useful for real-world traders

# ------------------------------------------------------------
# 📂 Data Summary
# ------------------------------------------------------------
# Trades data:
#   - Coin, Execution Price
#   - Trade Size (USD, Tokens)
#   - Closed PnL, Fees, Net PnL
#   - Execution type (Crossed: Market vs Limit)
#   - Timestamp
#
# Market sentiment data:
#   - Daily Fear & Greed Index value
#   - Sentiment classification:
#       Extreme Fear, Fear, Neutral, Greed, Extreme Greed

# ------------------------------------------------------------
# 🔧 Data Processing Overview
# ------------------------------------------------------------
# - Trades were merged with daily sentiment data by date
# - Non-informative fields (accounts, IDs, hashes) were removed
# - Analysis retained per-trade granularity
# - Sentiment was ordinally encoded for correlation analysis

# ------------------------------------------------------------
# 📈 Key Visual Insights
# ------------------------------------------------------------

# ============================================================
# 1️⃣ Trade Size vs Market Sentiment
# ============================================================

# ![Trade Size vs Market Sentiment](screenshots/trade_size_vs_sentiment.png)

# Observations:
# - Trade size increases during Greed and Extreme Greed
# - Neutral sentiment shows smaller, conservative positions
# - All regimes show long-tailed distributions

# Insight:
# Traders tend to increase position size as market optimism rises.

# ============================================================
# 2️⃣ Aggressive Trading (Market Orders) by Sentiment
# ============================================================

# ![Aggressive Trading by Sentiment](screenshots/aggressive_trading_by_sentiment.png)

# Observations:
# - Market orders are more frequent during Fear and Greed
# - Extreme sentiment regimes show reduced execution aggression
# - Neutral sentiment reflects balanced execution behavior

# Insight:
# Traders become more aggressive in emotionally charged markets,
# prioritizing speed over price.

# ============================================================
# 3️⃣ Win Rate by Market Sentiment
# ============================================================

# ![Win Rate by Sentiment](screenshots/win_rate_by_sentiment.png)

# Observations:
# - Extreme Greed shows the highest win rate
# - Extreme Fear shows the lowest win rate
# - Neutral sentiment lies between the two extremes

# Insight:
# Trend-following environments (Extreme Greed) improve the
# probability of winning trades, while fearful markets reduce it.

# ============================================================
# 4️⃣ Risk-Adjusted Performance (Sharpe-like Ratio)
# ============================================================

# ![Risk Adjusted Performance](screenshots/risk_adjusted_performance.png)

# Observations:
# - Extreme Greed has the highest risk-adjusted performance
# - Neutral sentiment offers stable but moderate returns
# - Extreme Fear has the worst risk-adjusted profile

# Insight:
# Profitability alone is misleading — Extreme Greed provides
# the best balance between return and volatility.

# ============================================================
# 5️⃣ Loss Severity Analysis (Median Loss)
# ============================================================

# ![Median Loss by Sentiment](screenshots/median_loss_by_sentiment.png)

# Observations:
# - Extreme Fear and Greed show the largest median losses
# - Neutral sentiment has the smallest median loss
# - Fear produces frequent but relatively smaller losses

# Insight:
# Neutral sentiment environments are best for capital protection,
# while extreme sentiment regimes increase downside risk.

# ============================================================
# 6️⃣ Feature Correlation with Market Sentiment
# ============================================================

# ![Feature Correlation Heatmap](screenshots/feature_correlation_heatmap.png)

# Observations:
# - Market sentiment has near-zero linear correlation with Net PnL
# - Strong correlation exists between trade size and fees
# - Weak correlations with execution aggressiveness

# Insight:
# Market sentiment does not directly predict returns; it
# influences trader behavior, which indirectly impacts outcomes.

# ------------------------------------------------------------
# 🧠 Key Takeaways
# ------------------------------------------------------------
# - Market sentiment affects HOW traders trade, not price direction
# - Behavioral variables respond more strongly to sentiment
#   than raw profitability
# - Extreme Greed offers the best risk-adjusted environment
# - Extreme Fear is highly volatile and dangerous
# - Fear & Greed Index is best used as a behavioral context filter

# ------------------------------------------------------------
# 📁 Screenshots Directory
# ------------------------------------------------------------
# screenshots/
# ├── trade_size_vs_sentiment.png
# ├── aggressive_trading_by_sentiment.png
# ├── win_rate_by_sentiment.png
# ├── risk_adjusted_performance.png
# ├── median_loss_by_sentiment.png
# └── feature_correlation_heatmap.png
# ============================================================
