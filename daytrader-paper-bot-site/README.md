# Daytrader Paper Bot

A paper-trading research dashboard for testing liquidity-sweep and FVG-style setups using Alpaca paper trading.

> **Educational only.** This is a prototype for learning and research. Not financial advice. No guarantee of performance.

## Overview

The Daytrader Paper Bot is an Electron + Python desktop application that:

- Connects to Alpaca Markets' paper-trading API for live market data
- Scans completed one-minute bars for liquidity-sweep, break-of-structure, and fair-value gap patterns
- Renders a real-time candlestick chart with VWAP, EMA20, opening-range, and prior-day level overlays
- Places simulated paper orders through Alpaca's paper environment with configurable risk guardrails
- Records session and account state for review

## Public Site

Detailed documentation, feature descriptions, and screenshots are available on the **public static site**:

```
index.html
```

Open `index.html` in any browser to view:

- Feature overview and architecture
- Concept glossary (liquidity sweep, BOS, FVG, VWAP, etc.)
- Dashboard screenshots
- Risk and safety design
- What is intentionally kept private

### Documentation Pages

| Page | Description |
|---|---|
| [How It Works](docs/how-it-works.html) | Concepts and data flow |
| [Risk & Safety](docs/risk-and-safety.html) | Position sizing, guardrails, backtest limitations |
| [Screenshots](docs/screenshots.html) | Dashboard screenshot gallery |

## Local Setup

Setup and usage instructions are maintained in the private project documentation. This public README points to the static site above for general concept information.

## What Is Not Published Here

- **Source code** — the full Python and JavaScript implementation is not included on this public site.
- **API credentials** — Alpaca API keys, secret keys, and account identifiers are never published.
- **Exact strategy implementation** — specific thresholds, filtering logic, and order-routing decisions are not disclosed.
- **Raw logs and trade data** — session logs, backtest results, and paper-trading records remain local.

## License

Private — source code is not publicly distributed.

