# Write-up — Crypto Trading × Fear & Greed Analysis

## Methodology

Two datasets were merged on date: a daily Fear & Greed Index (2018–2025) and historical trade records (211,224 trades, 32 accounts, 2024). Sentiment was bucketed into Fear / Neutral / Greed. Per-account metrics (win rate, leverage proxy, trade frequency, PnL) were computed and joined with daily sentiment scores.

A Random Forest classifier was trained to predict next-day market profitability (profit vs loss) using sentiment score, trade count, win rate, average leverage, position size, and long ratio. K-Means (k=4) was used to cluster accounts into behavioral archetypes based on trading style features.

---

## Insights

**1. Fear days are more profitable than Greed days**
Average daily PnL and win rate are both higher during Fear sentiment. Traders appear to buy dips effectively, generating better returns during market pessimism than during optimism.

**2. Traders go more long during Fear**
The long/short ratio spikes on Fear and Extreme Fear days, confirming a strong dip-buying behavior. During Greed, the ratio drops and traders become more cautious or short the market.

**3. High-leverage infrequent traders lose money on Greed days**
Accounts with above-median leverage but low trade frequency consistently produce negative PnL during Greed. Low-leverage frequent traders remain profitable across all sentiment conditions.

---

## Strategy Recommendations

**Strategy 1 — Consistent winners should increase activity on Fear days**
Accounts with win rate ≥ 50% show their best PnL and win rate during Fear. These traders should raise trade frequency when sentiment is Fear and reduce it during Greed.

**Strategy 2 — High-leverage infrequent traders should cap leverage on Greed days**
This segment turns unprofitable, specifically during Greed. Rule of thumb: cap leverage to 1× account baseline when sentiment score ≥ 4 (Greed / Extreme Greed).
