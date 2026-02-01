# BirdEye API Documentation

Complete API documentation for BirdEye - the leading DeFi data provider for Solana and EVM chains.

## Overview

BirdEye provides comprehensive DeFi data and analytics APIs including:

- **DeFi** - Real-time token prices, OHLCV candlesticks, liquidity data, trading volume
- **Wallet** - Portfolio tracking, PnL calculations, balance changes, net worth history
- **Token** - Metadata, holder distribution, security analysis, market data
- **Trader** - Top traders, gainers/losers, trading activity
- **WebSocket** - Real-time price feeds, transaction streams, new token alerts
- **Utils** - Network information, credit usage

## Supported Networks

- Solana
- Ethereum
- Arbitrum
- Avalanche
- BSC (Binance Smart Chain)
- Optimism
- Polygon
- Base
- zkSync
- And more...

## Documentation Structure

```
docs/
├── defi/       # Price, OHLCV, trades, token data
├── wallet/     # Portfolio, PnL, balances, net worth
├── websocket/  # Real-time subscriptions
├── trader/     # Trader analytics
└── utils/      # Utility endpoints
```

## Authentication

All API requests require authentication via the `x-api-key` header or as a query parameter.

## Base URL

```
https://public-api.birdeye.so
```

## Official Documentation

https://docs.birdeye.so

## Source

Documentation compiled from BirdEye's official API reference (February 2026).
