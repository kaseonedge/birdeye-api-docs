# Subscribing to Real-Time Token Transaction Updates (SUBSCRIBE\_TXS)   [Skip link to Subscribing to Real-Time Token Transaction Updates (SUBSCRIBE_TXS)](https://docs.birdeye.so/reference/tokenpair-transactions\#subscribing-to-real-time-token-transaction-updates-subscribe_txs)

The "SUBSCRIBE\_TXS" event allows you to receive real-time updates about token transactions. You can subscribe to transactions for individual tokens, token pairs, or a combination of both. This subscription is useful for tracking trading activities and other relevant transactions on the Birdeye platform.

You can use this Websocket to get real time transaction updates of following objects:

- Transactions of a token
- Transactions of a pair/market
- Transactions of multiple Tokens/Pairs

You can also filter the transaction type for each object, including swap, add liquidity, and remove liquidity. The instructions for each type of objects are described below.

## Code Example   [Skip link to Code Example](https://docs.birdeye.so/reference/tokenpair-transactions\#code-example)

Checkout this Github file for an example:

> [https://github.com/birdeye-so/tradingview-example-js-api/blob/main/websocket\_example.js](https://github.com/birdeye-so/tradingview-example-js-api/blob/main/websocket_example.js)

## 1 - Subscribe Token Transactions   [Skip link to 1 - Subscribe Token Transactions](https://docs.birdeye.so/reference/tokenpair-transactions\#1---subscribe-token-transactions)

To receive real-time updates about transactions for a specific token, you can use the following subscription message format:

### Input   [Skip link to Input](https://docs.birdeye.so/reference/tokenpair-transactions\#input)

JSON

```json
{
    "type": "SUBSCRIBE_TXS",
    "data": {
        "queryType": "simple",
        "address": "JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN",
				"txsType": "all"
    }
}
```

You can pass any of the following values to `txsType`: "all", "add\_remove\_liquidity", "add\_liquidity", "remove\_liquidity", "swap" to filter transaction types.
If `txsType` is not provided, the result will default to returning all transaction types, the same as when using "all".

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/tokenpair-transactions\#output-example)

JSON

```json
{
  "type": "TXS_DATA",
  "data": {
    "blockUnixTime": 1747307828,
    "owner": "Dc9jiLSNN8qwEciwd55HmZhroswZ4XvcvKeRXHWCnwbP",
    "source": "zerofi",
    "txHash": "3L4BWQxgpF7SyH13bbEH53ZXYFNdRcK5dtMXreeGviaWFKes3fod5cQWsQ3oRHXcdUaemoiEXLaUit1Syw5FdCP1",
    "side": "sell",
    "tokenAddress": "JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN",
    "alias": null,
    "isTradeOnBe": false,
    "platform": "Jupiter",
    "pricePair": 0.49898781541961984,
    "volumeUSD": 86.16813238056157,
    "from": {
      "address": "JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN",
      "amount": 172707630,
      "changeAmount": -172707630,
      "decimals": 6,
      "nearestPrice": 0.4989839116193116,
      "price": null,
      "symbol": "JUP",
      "type": "transfer",
      "typeSwap": "from",
      "uiAmount": 172.70763,
      "uiChangeAmount": -172.70763
    },
    "to": {
      "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",
      "amount": 86179003,
      "changeAmount": 86179003,
      "decimals": 6,
      "feeInfo": null,
      "nearestPrice": 0.99987386,
      "price": null,
      "symbol": "USDC",
      "type": "transfer",
      "typeSwap": "to",
      "uiAmount": 86.179003,
      "uiChangeAmount": 86.179003
    },
    "priceMark": true,
    "tokenPrice": 0.4989248730965828,
    "network": "solana",
    "poolId": "1amiJLvkVHjPz7t8dwBsWHknHitcpqwPPuuUCfHyzjB"
  }
}
```

## 2 - Subscribe Pair Transactions   [Skip link to 2 - Subscribe Pair Transactions](https://docs.birdeye.so/reference/tokenpair-transactions\#2---subscribe-pair-transactions)

To receive real-time updates about transactions for a specific token pair, you can use the following subscription message format:

### Input   [Skip link to Input](https://docs.birdeye.so/reference/tokenpair-transactions\#input-1)

JSON

```json
{
    "type": "SUBSCRIBE_TXS",
    "data": {
       "queryType": "simple",
     	 "pairAddress": "842NwDnKYcfMRWAYqsD3hoTWXKKMi28gVABtmaupFcnS",
			 "txsType":"all"
    }
}
```

You can pass any of the following values to `txsType`: "all", "add\_remove\_liquidity", "add\_liquidity", "remove\_liquidity", "swap" to filter transaction types.
If `txsType` is not provided, the result will default to returning all transaction types, the same as when using "all".

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/tokenpair-transactions\#output-example-1)

JSON

```json
 type: 'TXS_DATA',
  data: {
    blockUnixTime: 1714107255,
    owner: 'TyrZ6SDVQGdMpnYtAgKGocvi1w1mdffhZENf1knyeqy',
    source: 'raydium',
    txHash: '3XtCydTzZPJNGr9qQ83rvkKyGQHMQcUa3QpgBZoz97i3VkRGL3e8UBhM7JUnprwbcgWXeHXST74NeaEE4vjWeEME',
    alias: null,
    isTradeOnBe: false,
    platform: 'YmirFH6wUrtUMUmfRPZE7TcnszDw689YNWYrMgyB55N',
    volumeUSD: 31.569239727896086,
    from: {
      symbol: 'SOL',
      decimals: 9,
      address: 'So11111111111111111111111111111111111111112',
      amount: 219852856,
      type: 'transfer',
      typeSwap: 'from',
      uiAmount: 0.219852856,
      price: null,
      nearestPrice: 143.5925841595439,
      changeAmount: -219852856,
      uiChangeAmount: -0.219852856,
      icon: null
    },
    to: {
      symbol: 'TOM',
      decimals: 9,
      address: '2rJSfgxoWP7h3rw3hDUF7HPToY3exb6FdH9xFBg7TeQk',
      amount: 650244687263,
      type: 'transfer',
      typeSwap: 'to',
      feeInfo: null,
      uiAmount: 650.244687263,
      price: 0.048549784944459676,
      nearestPrice: 0.048420900217275124,
      changeAmount: 650244687263,
      uiChangeAmount: 650.244687263,
      icon: null
    }
  }
}
```

## 3 - Subscribe to Multiple Addresses (Limit 100)   [Skip link to 3 - Subscribe to Multiple Addresses (Limit 100)](https://docs.birdeye.so/reference/tokenpair-transactions\#3---subscribe-to-multiple-addresses-limit-100)

You can also subscribe to transactions for multiple addresses by using the "complex" query type.

You can get updates for maximum 100 addresses at once.

The following example demonstrates how to subscribe to transactions for either a specific token address or a specific token pair address:

### Input   [Skip link to Input](https://docs.birdeye.so/reference/tokenpair-transactions\#input-2)

JSON

```json
{
    "type": "SUBSCRIBE_TXS",
    "data": {
        "queryType": "complex",
        "query": "address = So11111111111111111111111111111111111111112 OR pairAddress = FmKAfMMnxRMaqG1c4emgA4AhaThi4LQ4m2A12hwoTibb",
				"txsType":"all"
    }
}
```

You can pass any of the following values to `txsType`: "all", "add\_remove\_liquidity", "add\_liquidity", "remove\_liquidity", "swap" to filter transaction types.
If `txsType` is not provided, the result will default to returning all transaction types, the same as when using "all".

**Output**

JSON

```json
{
    "type": "TXS_DATA",
    "data": {
        "blockUnixTime": 1692205532,
        "owner": "EkZStqj9BSwLS19uLDEsErCW6N1HHzvoGg92Ei3YYBNt",
        "source": "marinade",
        "txHash": "3GqVQTaimS2QsprgjTvpV4ArdZGUjoiacDE5Hy3baLapvAXekya7EsNjhWvMVbqdMRaJanwwAd4Bi9h8ag58vK3",
        ...
    }
}
```

The two WebSocket messages differ in their subscription type (complex vs simple), and as a result, there are key differences in the structure of the resulting **TXS\_DATA** responses.

#### Request Type Difference   [Skip link to Request Type Difference](https://docs.birdeye.so/reference/tokenpair-transactions\#request-type-difference)

**First WebSocket Request (COMPLEX Query)**

JSON

```json
{
    "type": "SUBSCRIBE_TXS",
    "data": {
        "queryType": "complex",
        "query": "address = 0x539bdE0d7Dbd336b79148AA742883198BBF60342 OR address = 0x2f2a2543B76A4166549F7aaB2e75Bef0aefC5B0f",
				"txsType":"all"
    }
}
```

**Query**:

- Logical OR statement, tracking multiple addresses.
- Returns all transactions involving these addresses, including swap, add liquidity and remove liquidity.

**Second WebSocket Request (SIMPLE Query)**

JSON

```json
{
    "type": "SUBSCRIBE_TXS",
    "data": {
        "queryType": "simple",
        "address": "0x539bdE0d7Dbd336b79148AA742883198BBF60342"
				"txsType":"all"
    }
}
```

**Query**:

- Tracks only this specific address.
- Optimized for this token address being a main asset in the transaction.

#### Response Structural Differences   [Skip link to Response Structural Differences](https://docs.birdeye.so/reference/tokenpair-transactions\#response-structural-differences)

| Field | COMPLEX Response | SIMPLE response |
| --- | --- | --- |
| side | swap | buy / sell |
| tokenAddress | ❌ | ✅ |
| pricePair | ❌ | ✅ |
| priceMark / tokenPrice | ✅ | ❌ |

#### Contextual Interpretation   [Skip link to Contextual Interpretation](https://docs.birdeye.so/reference/tokenpair-transactions\#contextual-interpretation)

**COMPLEX** query is more general and is probably used for monitoring addresses (wallets or token contracts) regardless of their transaction role. It yields raw swap data and doesn't include enriched metadata like tokenAddress, pricePair, or network.

**Example:**

JSON

```json
{
    "type": "TXS_DATA",
    "data": {
        "blockUnixTime": 1750298427,
        "owner": "0x22e4668AB0c1eE4A249F3A8A975f2aD780b08444",
        "source": "0xd845f7D4f4DeB9Ff5bCf09D140Ef13718F6f6C71",
        "txHash": "0x5ce5c84cfd3ae78ac6bf7f89b539a9f9aa4210e9ea56a8d495509bdd4dd6dea9",
        "side": "swap",
        "alias": null,
        "isTradeOnBe": false,
        "platform": "0x409De6561Cfc8C14359BeD66cB668b4f33420E73",
        "volumeUSD": 547.9549194582437,
        "from": {
            "address": "0x2f2a2543B76A4166549F7aaB2e75Bef0aefC5B0f",
            "amount": 524114,
            "changeAmount": -524114,
            "decimals": 8,
            "mint": "0x2f2a2543B76A4166549F7aaB2e75Bef0aefC5B0f",
            "name": "Wrapped Bitcoin",
            "nearestPrice": 104533.06339411934,
            "price": 104548.80416440769,
            "symbol": "WBTC",
            "typeSwap": "from",
            "uiAmount": 0.00524114,
            "uiChangeAmount": -0.00524114
        },
        "to": {
            "address": "0x82aF49447D8a07e3bd95BD0d56f35241523fBab1",
            "amount": 217772242384751600,
            "changeAmount": 217772242384751600,
            "decimals": 18,
            "mint": "0x82aF49447D8a07e3bd95BD0d56f35241523fBab1",
            "name": "WETH",
            "nearestPrice": 2516.183483522836,
            "price": 2516.183483522836,
            "symbol": "WETH",
            "typeSwap": "to",
            "uiAmount": 0.21777224238475162,
            "uiChangeAmount": 0.21777224238475162
        },
        "poolId": "0xd845f7D4f4DeB9Ff5bCf09D140Ef13718F6f6C71"
    }
}
```

**SIMPLE** query is specialized for token-level tracking, likely focused on the specific token contract address as the selling/swapping asset. It gives extra fields (like tokenPrice, network, pricePair) that are useful in token-centric analytics.

**Example:**

JSON

```json
{
    "type": "TXS_DATA",
    "data": {
        "blockUnixTime": 1750234547,
        "owner": "0xcFbFeA9aE5EF502BB1Cb188993542638b4d26900",
        "source": "0xB7E50106A5bd3Cf21AF210A755F9C8740890A8c9",
        "txHash": "0x6dc1bfd71156e32ef8d8c03b9e9697e7a6446cc5c143c7915c7c6e8e3ccf3f63",
        "side": "sell",
        "tokenAddress": "0x539bdE0d7Dbd336b79148AA742883198BBF60342",
        "alias": null,
        "isTradeOnBe": false,
        "platform": "0xaaaaaaae92Cc1cEeF79a038017889fDd26D23D4d",
        "pricePair": 0.00006240110207123055,
        "volumeUSD": 6.747140220183636,
        "from": {
            "address": "0x539bdE0d7Dbd336b79148AA742883198BBF60342",
            "amount": 42518663000000000000,
            "changeAmount": -42518663000000000000,
            "decimals": 18,
            "mint": "0x539bdE0d7Dbd336b79148AA742883198BBF60342",
            "name": "Magic",
            "nearestPrice": 0.1595716148388752,
            "price": 0.1586865565406804,
            "symbol": "MAGIC",
            "typeSwap": "from",
            "uiAmount": 42.518663000000004,
            "uiChangeAmount": -42.518663000000004
        },
        "to": {
            "address": "0x82aF49447D8a07e3bd95BD0d56f35241523fBab1",
            "amount": 2653211429795254,
            "changeAmount": 2653211429795254,
            "decimals": 18,
            "mint": "0x82aF49447D8a07e3bd95BD0d56f35241523fBab1",
            "name": "WETH",
            "nearestPrice": 2543.008877624316,
            "price": 2543.008877624316,
            "symbol": "WETH",
            "typeSwap": "to",
            "uiAmount": 0.002653211429795254,
            "uiChangeAmount": 0.002653211429795254
        },
        "priceMark": false,
        "tokenPrice": 0.1586865565406804,
        "network": "arbitrum",
        "poolId": "0xB7E50106A5bd3Cf21AF210A755F9C8740890A8c9"
    }
}
```

* * *

* * *

