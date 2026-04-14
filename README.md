# Ethereum Whale Behavior Analysis (DEX Trading)

## Overview
Identification and analysis of whale wallets on Ethereum DEX using real on-chain data 
from Dune Analytics. Analyzed 1,000 largest trades over 7 days (min $100,000 per trade).

## Business Problem
Identify high-value traders (“whales”) on Ethereum DEXs and understand their behavior to detect potential market-moving activity.

## Data Source
- Dune Analytics — live Ethereum blockchain data
- 1,000 transactions, all above $100,000
- Period: last 7 days

## Methodology 
Aggregated trades by wallet
Calculated:
- Total Volume
- Number of Trades
- Average Trade Size
Classified wallets into:
- Mega Whale
- Active Whale
- Bot / HFT
Time analysis:
- Hourly aggregation (UTC)

## Key Findings

### 1. Whale Types
| Wallet | Type | Total Volume | Trades | Avg Trade |
|---|---|---|---|---|
| 0x555f24... | Active Whale | $388M | 81 | $4.8M |
| 0x1f2f10... | Bot / HFT | $355M | 236 | $1.5M |
| 0xbab386... | Mega Whale | $164M | 24 | $6.8M |
Insight:
- Market structure is not homogeneous — different whale types play different roles.

### 2. Token Preference
- 87% of volume is stablecoins (USDC + USDT)
Insight:
Whales are primarily:
- moving capital
- managing liquidity
- NOT gambling on tokens

### 3. Trading Hours
- Peak activity at 16:00 UTC (NYSE open)
Insight:
- Whales follow traditional market hours — institutional behavior


## Conclusion
Ethereum whale activity is dominated by institutional players and bots.
Monitoring these wallets can provide early signals of large market movements.

## Visualizations
![Whale Volume](whale_chart.png)
![Whale Scatter](whale_scatter.png)
![Hourly Activity](whale_hourly.png)
![Top Tokens](whale_tokens.png)

## Tools
Python, Pandas, Matplotlib, Dune Analytics API
