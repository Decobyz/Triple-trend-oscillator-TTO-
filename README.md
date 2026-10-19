
# Triple-trend-oscillator-TTO-
A cTrader cBot for XAUUSD on the M15 timeframe, with out-of-sample backtesting, performance analysis, and quantitative trading research documentation.
# TTO Gold Swing — XAUUSD Algorithmic Trading Bot
<img width="816" height="445" alt="wone" src="https://github.com/user-attachments/assets/4775a3f3-f916-4e47-bc62-39958b3656d5" />

## Overview

**TTO Gold Swing** is an algorithmic trading bot developed for trading Gold against the US Dollar (XAUUSD) using the cTrader Automate platform.

The strategy uses a multi-timeframe trend and momentum approach to identify potential trading opportunities. It combines trend analysis across daily, hourly, and 15-minute timeframes with moving-average indicators and ATR-based stop-loss logic.

This repository documents the strategy configuration, backtesting results, and development of the trading bot.

## Strategy Features

- **Market:** Gold / US Dollar (XAUUSD)
- **Platform:** cTrader Automate
- **Trading timeframe:** M15
- **Strategy type:** Multi-timeframe trend and momentum
- **Major timeframe:** Daily (D1)
- **Intermediate timeframe:** Hourly (H1)
- **Entry timeframe:** 15 minutes (M15)
- **Trend indicators:** EMA, DEMA, and TEMA
- **Trigger EMA period:** 5
- **ATR period:** 14
- **ATR stop multiplier:** 1.5
- **Risk per trade setting:** 1%
- **Maximum volume setting:** 0.1 lots
<img width="805" height="327" alt="wtwo" src="https://github.com/user-attachments/assets/23eb0ace-bf65-4ec1-91d4-b1d5f5463a98" />

The bot is designed to analyze market conditions across multiple timeframes and manage trades using volatility-based stop-loss parameters.

## Backtesting Results

The following results were recorded in the supplied cTrader backtesting report.

| Metric | Result |
|---|---:|
| Trading instrument | XAUUSD |
| Timeframe | M15 |
| Backtest period | January 1, 2025 – October 18, 2026 |
| Initial balance | $5,000.00 |
| Final balance | $13,151.99 |
| Net profit | $8,151.99 |
| Reported return on investment | 163.04% |
| Total trades | 537 |
| Winning trades | 189 |
| Losing trades | 348 |
| Win rate | 35.20% |
| Profit factor | 1.36 |
| Average profit per trade | $15.18 |
| Largest winning trade | $1,370.48 |
| Largest losing trade | -$280.96 |
| Long trades | 352 |
| Short trades | 185 |
| Long-trade profit factor | 1.33 |
| Short-trade profit factor | 1.41 |
| Total commissions | -$856.22 |
| Total swaps | -$337.69 |
<img width="775" height="428" alt="wthree" src="https://github.com/user-attachments/assets/8178accc-8045-41dc-83a3-99c278348862" />

*These are historical backtesting results, not live trading results. The maximum drawdown estimate derived from the report's equity data is approximately 28.05%; it has not been independently verified.*

## Backtesting Methodology

The supplied report records a backtest using the following configuration:

- **Starting capital:** $5,000
- **Deposit currency:** USD
- **Broker environment:** Pepperstone
- **Account type:** Hedging
- **Leverage:** 1:400
- **Spread setting:** Fixed spread value of 1
- **Commission setting:** USD 30 per million USD volume, with automatic commission application disabled
- **Market data:** Server-provided M1 bars

Actual results may differ between brokers because of differences in spreads, commissions, swaps, execution quality, and market data.

## Out-of-Sample Testing

This project is intended to document the evaluation of an algorithmic trading strategy on historical market data.

The test period should be considered **out-of-sample (OOS)** only if it was kept separate from the data used to develop the strategy and select its parameters.

If the strategy was adjusted using data from this test period, the results should instead be described as historical backtesting results.

## Risk Management

The bot's reported configuration includes a 1% risk-per-trade setting, an ATR period of 14, an ATR stop multiplier of 1.5, and a maximum volume setting of 0.1 lots.

These are configuration parameters, not a guarantee that every trade risks exactly 1% of account equity. Actual risk depends on implementation details, position sizing, contract specifications, and execution conditions.

Gold can experience significant price movements, spreads can widen, and losses can exceed expectations.

## Repository Structure

```text
tto-xauusd-trading-bot/
├── README.md
├── .gitignore
└── docs/
    └── backtest-summary.md
```

The C# cBot source code can be added to the repository when it is ready for public release.

## Installation and Usage

1. Install cTrader and open the cTrader Automate environment.
2. Add the bot's C# source file to a cTrader Automate cBot project.
3. Build the project and resolve any compilation errors.
4. Configure the trading symbol, timeframes, risk parameters, and other settings.
5. Run a backtest using historical data.
6. Review profitability, drawdown, trade statistics, and transaction costs before considering any live deployment.

**Note:** This repository currently documents the strategy and its reported backtest. A complete runnable implementation requires the actual C# source code.

## Limitations

- Historical performance does not guarantee future results.
- Backtest results depend on the quality of historical data and execution assumptions.
- Transaction costs can materially affect profitability.
- The reported profit factor of 1.36 does not eliminate the possibility of substantial losses.
- Further validation, including independent out-of-sample testing and forward testing, is recommended before live deployment.

## Disclaimer

This project is provided for educational, research, and software-development purposes only. It is not financial advice or a recommendation to buy or sell any financial instrument.

Trading leveraged products, including gold CFDs, involves substantial risk and may result in the loss of capital. Users are responsible for independently evaluating the strategy and its suitability before use.

## Author

Developed as an algorithmic trading and quantitative research project.

Contributions, technical feedback, and suggestions for further testing are welcome.
