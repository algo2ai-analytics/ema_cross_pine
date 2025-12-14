📌 EMA – Cross (RK) | Risk-Aware Trend Strategy

Author: retaish_kumarci
Version: Pine Script v6
Market: Works on equities, indices, futures, crypto
Timeframes: Intraday to positional

🔹 Overview

This strategy combines EMA trend structure, RSI momentum confirmation, and ATR volatility filtering, enhanced with strict risk controls at both trade and portfolio level.

It is designed to:
Trade only when trend, momentum, and volatility align
Prevent revenge trading after large losses
Automatically flatten positions on adverse moves

🔹 Indicators Used

1️⃣ Exponential Moving Averages (EMA)
  > EMA 20, 50, 75, 100, 150, 200
  > Trend bias is determined using relative EMA ordering
  > Uses OR-based hierarchy to remain responsive

2️⃣ RSI Momentum Filter
  > RSI(14) vs RSI(28)
  > Long only if short-term momentum > medium-term
  > Short only if short-term momentum < medium-term

3️⃣ ATR Volatility Filter
  > ATR(14) vs ATR(28)
  > Trades only during contracting volatility
  > Avoids high-noise / expansion zones

4️⃣ ATR Bollinger Bands (Volatility Context)
  > Bollinger Bands applied to ATR(14)
  > Helps visualize volatility compression / expansion
  > Plotted with scale.none to avoid price distortion

🔹 Trade Logic

Long Entry:
  > EMA trend bullish
  > RSI momentum bullish
  > ATR short < ATR long
  > No cooldown active

Inside date range (if enabled)

Short Entry:
  > EMA trend bearish
  > RSI momentum bearish
  > ATR short < ATR long
  > No cooldown active

Inside date range (if enabled)

Only one position at a time (pyramiding disabled).

🔹 Risk Management (Core Feature)
✅ Set 1: Open Trade Loss Control
          Closes any open trade if unrealized loss exceeds X%

✅ Set 2: Last Closed Trade Protection
          If the previous trade lost more than X%:
          • Immediately closes any open position
          • Optionally blocks new trades for N bars (cooldown)


This prevents:
  > Over-trading
  > Emotional re-entries
  > Drawdown spirals

🔹 Date Range Control
  > Backtest only within selected date range
  > Uses constant epoch timestamps (Pine v6 safe)
  > No timezone mismatch or runtime errors

🔹 Recommended Usage
  > Use on liquid instruments
  > Works best on 15m – Daily
  > Enable cooldown after optimization
  > Combine with higher-timeframe trend bias if needed

⚠️ Disclaimer

This script is for educational and research purposes only.
Not financial advice. Always forward-test before live deployment.
