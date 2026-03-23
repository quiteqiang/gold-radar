---
name: gold-intel-monitor
description: Real-time gold price monitoring and investment decision support system. Used for tracking gold price fluctuations, market trend analysis, and investment timing alerts. Supports customizable price alerts, technical indicator monitoring, and macroeconomic data tracking to help investors make timely trading decisions.
---

# Gold Intelligence Monitor

Real-time gold price monitoring and investment alert system.

## Features

- **Real-time Price Tracking** - Monitor international gold prices (XAU/USD) and gold denominated in major currencies
- **Multi-level Alert System** - Price breakouts, technical indicator signals, major economic events
- **Technical Analysis Support** - Key price levels, trend lines, support and resistance monitoring
- **Macroeconomic Linkage** - Federal Reserve policy, US Dollar Index, geopolitical impacts on gold prices
- **Investment Decision Support** - Buy/sell recommendations, position management tips

## Setup

Before use, configure your investment profile in `config.json`:

```json
{
  "user_profile": {
    "name": "Investor Name",
    "currency": "CNY",
    "timezone": "Asia/Shanghai"
  },
  "investment_params": {
    "holding_cost": 450.00,
    "target_profit": 600.00,
    "stop_loss": 380.00,
    "position_size": "10 grams"
  },
  "alert_thresholds": {
    "price_change_pct": 2.0,
    "daily_high_low": true,
    "key_levels": [380, 400, 450, 500, 550]
  },
  "watchlist": [
    {"symbol": "XAUUSD", "name": "Spot Gold", "priority": 1},
    {"symbol": "SHAU", "name": "Shanghai Gold T+D", "priority": 1},
    {"symbol": "GLD", "name": "SPDR Gold ETF", "priority": 2},
    {"symbol": "DXY", "name": "US Dollar Index", "priority": 2},
    {"symbol": "US10Y", "name": "US 10Y Treasury Yield", "priority": 3}
  ]
}
```

## Monitoring Workflow

### 1. Set Up Scheduled Tasks

Create two monitoring tasks:

**Daily Briefing (1 daily)**
```
Generate market briefing:
1. Get price trends for the past 24 hours
2. Check US Dollar Index movement
3. Review Fed officials' speeches/economic data releases
4. Provide position holding advice and risk management
```

**Weekly Analysis (Monday market open)**
```
Generate weekly outlook:
1. Review last week's gold price performance
2. This week's economic calendar (Fed meetings, NFP, etc.)
3. Technical analysis (trends, key support/resistance)
4. Next week's trading strategy recommendations
```

### 2. Alert Levels

| Level | Trigger Conditions | Response |
|-------|-------------------|----------|
| 🔴 Red | Price breaks target profit/stop-loss levels, daily movement >3%, major geopolitical conflicts | Immediate notification, execute trading decisions |
| 🟡 Yellow | Price breaks key round numbers, technical divergence, Fed officials' speeches | Prepare to trade, closely monitor |
| 🟢 Green | Normal price fluctuations, routine market monitoring | Regular briefings |

### 3. Alert Template

```
🚨 [Alert Level] {Alert Type}

💰 Instrument: {Gold Type}
📈 Current Price: {Price} ({Change})
🎯 Key Level: {Breakout Level}

⚡ Recommended Actions:
1. {Action 1}
2. {Action 2}
3. {Action 3}

📊 Market Analysis:
{Brief Analysis}

🔗 Influencing Factors:
- US Dollar Index: {DXY}
- Treasury Yield: {US10Y}
- Major Events: {event}
```

### 4. Briefing Template

```
📋 Gold Market Briefing - {Date}

🎯 Market Overview:
{Summary}

💰 Price Quotes:
| Instrument | Price | Change | Key Level |
|------------|-------|--------|-----------|
| {Name} | {Price} | {Change} | {Key Level} |

📊 Technical Analysis:
- Support: {levels}
- Resistance: {levels}
- Trend: {Direction}

📅 Economic Calendar:
- {Time}: {Event} (Impact: {High/Medium/Low})

💡 Investment Recommendations:
- Holding Cost: {cost}
- Current P&L: {P&L}
- Recommended Action: {recommendation}

⚠️ Risk Warning: {level}
{Risk Description}
```

## Investment Strategy Guide

### Buy Signals
1. Federal Reserve rate cut expectations rise
2. Geopolitical risks escalate
3. Technical breakout (breaks consolidation range)

### Sell Signals
1. Federal Reserve rate hike expectations rise
2. Technical breakdown (breaks support level)
3. Position reaches expected profit (take profit)

## Data Sources

### Official Data (Priority)
- Shanghai Gold Exchange (SGE)
- World Gold Council (WGC)

### Market Data
- Bloomberg/Reuters Gold Prices
- TradingView Technical Analysis
- Kitco Gold News
- Major bank gold quotes

### Macro Indicators
- Federal Reserve interest rate decisions, meeting minutes
- Non-farm payroll data
- CPI/PPI inflation data
- TWITER/X most recent post

### Geopolitics & Sentiment
- Geopolitical conflict news
- Central bank gold purchase/sale news
- Major institution research reports (Goldman Sachs, JPMorgan, etc.)

## Customization

Edit `config.json` to customize:
- Holding cost and target price levels
- Alert thresholds (price change percentage)
- Gold instruments to monitor (spot, futures, ETFs)
- Key price level settings
- Local timezone and currency

## Disclaimer

This system is for reference only and does not constitute investment advice. Gold investment involves risks; invest with caution. Please make investment decisions based on your own risk tolerance.
