⚠️ Disclaimer
This script is for educational and research purposes only.
Not financial advice. Always forward-test before live deployment.

# ema_cross_pine
🔹 Overview  This strategy combines EMA trend structure, RSI momentum confirmation, and ATR volatility filtering, enhanced with strict risk controls at both trade and portfolio level.

# EMA – Cross (RK)

A risk-aware TradingView Pine Script strategy using:
- EMA trend hierarchy
- RSI momentum confirmation
- ATR volatility contraction filter
- Trade-level and open-position risk controls

## Scripts
- **EMA_Cross_RK.pine** – Main trading strategy (overlay)
- **ATR_Bollinger_RK.pine** – Volatility companion indicator (sub-pane)

## Features
- No pyramiding
- Date-range backtesting
- Open loss cut-off
- Last-trade loss protection with cooldown
- Designed for equities, indices, and futures

## Usage
1. Add the strategy to your TradingView chart
2. Add the ATR Bollinger indicator below the price chart
3. Tune parameters per instrument and timeframe

## License
Mozilla Public License 2.0 (MPL-2.0)

© retaish_kumarci

