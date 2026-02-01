# Subscribing to Real-Time New Pairs (SUBSCRIBE\_NEW\_PAIR)   [Skip link to Subscribing to Real-Time New Pairs (SUBSCRIBE_NEW_PAIR)](https://docs.birdeye.so/reference/new-pair\#subscribing-to-real-time-new-pairs-subscribe_new_pair)

The "SUBSCRIBE\_NEW\_PAIR" event allows you to receive real-time updates about new pairs. This subscription is useful for tracking new tokens being added on a requested blockchain. However, please note that the DEX Openbook pairs are not supported. Currently, this feature supports the Solana and EVM chains.

The instructions for each type of objects are described below.

## WebSocket URL:   [Skip link to WebSocket URL:](https://docs.birdeye.so/reference/new-pair\#websocket-url)

```undefined
wss://public-api.birdeye.so/socket/solana?x-api-key=YOUR-API-KEY
```

### Header   [Skip link to Header](https://docs.birdeye.so/reference/new-pair\#header)

| Key | Value |
| --- | --- |
| `Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Protocol` | echo-protocol |

### Message   [Skip link to Message](https://docs.birdeye.so/reference/new-pair\#message)

JSON

```json
{
    "type": "SUBSCRIBE_NEW_PAIR"
}
```

Or:

JSON

```json
{
    "type": "SUBSCRIBE_NEW_PAIR",
     "min_liquidity": 100,
     "max_liquidity" : 50000
}
```

**Key Notes:**

- The `min_liquidity` parameter is **optional** but user must set higher than system value which is `0`.
- The `max_liquidity` parameter is **optional** but must be higher than `min_volume` when provided.

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/new-pair\#output-example)

JSON

```json
{
    "type": "NEW_PAIR_DATA",
    "data": {
        "address": "CXV4S8CxSppJeGzMFv8YQjsGZJif8d1Fqz9EtJRovmJY",
        "name": "$JESUSPUMP-SOL",
        "source": "pump_dot_fun",
        "base": {
            "address": "AoMBAxc82xinKTnEBGvuJaFb7occsyyBD6GmELrypump",
            "name": "JESUS PUMP",
            "symbol": "$JESUSPUMP",
            "decimals": 6
        },
        "quote": {
            "address": "So11111111111111111111111111111111111111112",
            "name": "Wrapped SOL",
            "symbol": "SOL",
            "decimals": 9
        },
        "txHash": "3CzXpuUJV9KryVDMN5nFAqH87TfueWG6sUiksbf3Akh9eqGNJW1CJtYbrELJixXC77Dyutz8CfT3eP1uJ3LP3iy5",
        "blockTime": 1720156781
    }
}
```

**Response Parameters:**

| Key | Data Type | Details | Example |
| --- | --- | --- | --- |
| `type` | string | The type of the response data. | "NEW\_PAIR\_DATA" |
| `data` | object | The main data object containing details of the new trading pair. |  |
| `data.address` | string | The address of the new trading pair. | "CXV4S8CxSppJeGzMFv8YQjsGZJif8d1Fqz9EtJRovmJY" |
| `data.name` | string | The name of the trading pair. | "$JESUSPUMP-SOL" |
| `data.source` | string | The source or platform where the trading pair is listed. | "pump\_dot\_fun" |
| `data.base` | object | The base token object containing details of the base token. |  |
| `data.base.address` | string | The address of the base token. | "AoMBAxc82xinKTnEBGvuJaFb7occsyyBD6GmELrypump" |
| `data.base.name` | string | The name of the base token. | "JESUS PUMP" |
| `data.base.symbol` | string | The symbol of the base token. | "$JESUSPUMP" |
| `data.base.decimals` | integer | The number of decimal places for the base token. | 6 |
| `data.quote` | object | The quote token object containing details of the quote token. |  |
| `data.quote.address` | string | The address of the quote token. | "So11111111111111111111111111111111111111112" |
| `data.quote.name` | string | The name of the quote token. | "Wrapped SOL" |
| `data.quote.symbol` | string | The symbol of the quote token. | "SOL" |
| `data.quote.decimals` | integer | The number of decimal places for the quote token. | 9 |
| `data.txHash` | string | The transaction hash for the creation of the trading pair. | "3CzXpuUJV9KryVDMN5nFAqH87TfueWG6sUiksbf3Akh9eqGNJW1CJtYbrELJixXC77Dyutz8CfT3eP1uJ3LP3iy5" |
| `data.blockTime` | integer | The Unix timestamp when the trading pair was created. | 1720156781 |

* * *

* * *

StripeM-Inner
