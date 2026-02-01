# Subscribing to Real-Time token new listing (SUBSCRIBE\_WALLET\_TXS)   [Skip link to Subscribing to Real-Time token new listing (SUBSCRIBE_WALLET_TXS)](https://docs.birdeye.so/reference/wallet-transactions\#subscribing-to-real-time-token-new-listing-subscribe_wallet_txs)

The SUBSCRIBE\_WALLET\_TXS event allows you to receive real-time updates for transactions involving a specific wallet address. This subscription is useful for tracking all token transactions related to a provided address.

The instructions for each type of objects are described below.

## WebSocket URL:   [Skip link to WebSocket URL:](https://docs.birdeye.so/reference/wallet-transactions\#websocket-url)

```undefined
wss://public-api.birdeye.so/socket/solana?x-api-key=YOUR-API-KEY
```

### Header   [Skip link to Header](https://docs.birdeye.so/reference/wallet-transactions\#header)

| Key | Value |
| --- | --- |
| `Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Protocol` | echo-protocol |

### Message   [Skip link to Message](https://docs.birdeye.so/reference/wallet-transactions\#message)

**Subscription**

JSON

```json
{
    "type": "SUBSCRIBE_WALLET_TXS",
    "data": {
        "address": "0xae2Fc483527B8EF99EB5D9B44875F005ba1FaE13"
    }
}
```

For EVM addresses (Ethereum, BSC, etc.), the address can be provided in any format (checksum, lowercase, uppercase).

For Solana, a valid address is required (e.g., 9SeRj4LjgENeKQujfxRNkGbXYPM3X2vr9C37Jg9AARfg).

**Unsubscription**

JSON

```json
{
  "type": "UNSUBSCRIBE_WALLET_TXS"
}
```

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/wallet-transactions\#output-example)

JSON

```json
{
    "type": "WALLET_TXS_DATA",
    "data": {
        "type": "mint_add_liquidity",
        "blockUnixTime": 1733821667,
        "blockHumanTime": "2024-12-10T09:07:47",
        "owner": "0xae2Fc483527B8EF99EB5D9B44875F005ba1FaE13",
        "source": "0x0A0b2c28470bF68A6144DF04b08360559fb4aAf1",
        "txHash": "0xd80eaabb9c185313c8258ac54eea8bd75eadfb904dec85f887b7f47c58bdb59e",
        "volumeUSD": 2635.811230294149,
        "network": "ethereum",
        "base": {
            "symbol": "WETH",
            "decimals": 18,
            "address": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
            "uiAmount": 0.09992862476596062
        },
        "quote": {
            "symbol": "TRVL",
            "decimals": 18,
            "address": "0xd47bDF574B4F76210ed503e0EFe81B58Aa061F3d",
            "uiAmount": 39214.96224535667
        }
    }
}
```

**Response Parameters:**

| Key | Data Type | Details | Example |
| --- | --- | --- | --- |
| `type` | string | Type of transaction (e.g., mint\_add\_liquidity, swap, etc.) | "mint\_add\_liquidity" |
| `blockUnixTime` | integer | Unix timestamp for when the transaction was processed | 1733821667 |
| `blockHumanTime` | string | Human-readable timestamp for when the transaction was processed | "2024-12-10T09:07:47" |
| `owner` | string | The wallet address associated with the transaction | "0xae2Fc483527B8EF99EB5D9B44875F005ba1FaE13" |
| `source` | string | The source address initiating the transaction | "0x0A0b2c28470bF68A6144DF04b08360559fb4aAf1" |
| `txHash` | string | The transaction hash | "0xd80eaabb9c185313c8258ac54eea8bd75eadfb904dec85f887b7f47c58bdb59e" |
| `volumeUSD` | number | The total transaction volume in USD | 2635.811230294149 |
| `network` | string | The network where the transaction occurred (e.g., ethereum, bsc) | "ethereum" |
| `base` | object | The base token involved in the transaction, with symbol, address, and amount | `{ "symbol": "WETH", "address": "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2", "uiAmount": 0.09992862476596062 }` |
| `quote` | object | The quote token involved in the transaction, with symbol, address, and amount | `{ "symbol": "TRVL", "address": "0xd47bDF574B4F76210ed503e0EFe81B58Aa061F3d", "uiAmount": 39214.96224535667 }` |

**Key Notes:**

- Only transactions with the specified owner address will be filtered and returned in the response.
- Supported blockchains: EVM compatible chains, Solana, etc.
- For EVM addresses (Ethereum, BSC, etc.), the address can be in any case (lowercase, uppercase, checksum format).
- For Solana, the address must be provided in the correct format.

**Sample code** [https://github.com/TheNang2710/bds-public/blob/main/ws-wallet.js](https://github.com/TheNang2710/bds-public/blob/main/ws-wallet.js)

* * *

* * *

