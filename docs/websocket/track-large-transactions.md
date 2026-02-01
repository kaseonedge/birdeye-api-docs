# Subscribing to Real-Time Large Trades Volume (SUBSCRIBE\_LARGE\_TRADE\_TXS)   [Skip link to Subscribing to Real-Time Large Trades Volume (SUBSCRIBE_LARGE_TRADE_TXS)](https://docs.birdeye.so/reference/track-large-transactions\#subscribing-to-real-time-large-trades-volume-subscribe_large_trade_txs)

This WebSocket message is used to subscribe to large trade transactions filtered by specified volume thresholds in USD.

**Key Notes:**

- Only swap transactions are included.
- The `min_volume` parameter is **mandatory** and sets the lower bound for the trade volume in USD, the min allowable set is `0`.
- The `max_volume` parameter is **optional** but must be higher than `min_volume` when provided.
- Transactions outside the specified volume range will be excluded from the subscription.
- The response includes trades for all tokens that meet the volume criteria, regardless of token type or trading pair.

## Subscribe Large Trades   [Skip link to Subscribe Large Trades](https://docs.birdeye.so/reference/track-large-transactions\#subscribe-large-trades)

### Message   [Skip link to Message](https://docs.birdeye.so/reference/track-large-transactions\#message)

JSON

```json
{
    "type": "SUBSCRIBE_LARGE_TRADE_TXS",
    "min_volume": 10000,
    "max_volume": 20000
}
```

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/track-large-transactions\#output-example)

JSON

```json
{
    "type": "TXS_LARGE_TRADE_DATA",
    "data": {
        "blockUnixTime": 1734345250,
        "blockHumanTime": "2024-12-16T10:34:10",
        "owner": "7wWGFsrUnCjDS5mSxSZVgqqX2KBvS7muUTgAyB3pZQ4s",
        "source": "lifinity",
        "poolAddress": "Gkt4BpMRFxhhrrVMQsewM74ggriAbxyN2yUYDD9qt1NV",
        "txHash": "5TDU8rdEYXzmiJmGB6xeB9VsmQGXrQvefsto65jXJfgb2dZu19zt2nWxxTuhdKUCGyHPbBfyPhyuxpDgfP5Qfd3d",
        "volumeUSD": 12903.754274606412,
        "network": "solana",
        "from": {
            "symbol": "SOL",
            "decimals": 9,
            "address": "So11111111111111111111111111111111111111112",
            "uiAmount": 59.283968522,
            "price": null,
            "nearestPrice": 217.64374028102003,
            "uiChangeAmount": -59.283968522
        },
        "to": {
            "symbol": "USDC",
            "decimals": 6,
            "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",
            "uiAmount": 12904.206438,
            "price": null,
            "nearestPrice": 0.99996496,
            "uiChangeAmount": 12904.206438
        }
    }
}
```

### Explanation:   [Skip link to Explanation:](https://docs.birdeye.so/reference/track-large-transactions\#explanation)

`type`: Indicates the type of data (TXS\_LARGE\_TRADE\_DATA).

`data`: Contains detailed transaction information.
`blockUnixTime` and `blockHumanTime`: Block timestamp in UNIX and human-readable formats.
`owner`: Address of the trader executing the transaction.
`source`: Source of the trade (e.g., liquidity provider or protocol).
`poolAddress`: Address of the trading pool.
`txHash`: Transaction hash for tracking.
`volumeUSD`: Trade volume in USD.
`network`: Blockchain network where the trade occurred.
`from` and `to`: Details of the traded assets, including symbols, addresses, amounts, and pricing information.

Updated 24 days ago

* * *

Did this page help you?

Yes

No

Updated 24 days ago

* * *

Did this page help you?

Yes

No
