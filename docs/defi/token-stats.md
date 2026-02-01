# Subscribing to Real-Time token overview data (SUBSCRIBE\_TOKEN\_STATS)   [Skip link to Subscribing to Real-Time token overview data (SUBSCRIBE_TOKEN_STATS)](https://docs.birdeye.so/reference/token-stats\#subscribing-to-real-time-token-overview-data-subscribe_token_stats)

`SUBSCRIBE_TOKEN_STATS` provides real-time updates on token overview data. This subscription is ideal for monitoring live token metrics such as price, volume, trade activity, and supply changes.

It serves as the real-time counterpart to the [GET /defi/token\_overview](https://docs.birdeye.so/update/reference/get-defi-token_overview#/) endpoint.

The instructions for each type of objects are described below.

> 🚧
>
> ### This method is currently supported only on the Solana, Base, BSC, Ethereum, Polygon, Arbitrum, Optimism, Avalanche, ZKSync networks.  `intervals` supported: \["30m","1h", "2h", "4h", "8h", "24h"\]   [Skip link to This method is currently supported only on the Solana, Base, BSC, Ethereum, Polygon, Arbitrum, Optimism, Avalanche, ZKSync networks.,[object Object], ,[object Object], supported: ["30m","1h", "2h", "4h", "8h", "24h"]](https://docs.birdeye.so/reference/token-stats\#this-method-is-currently-supported-only-on-the-solana-base-bsc-ethereum-polygon-arbitrum-optimism-avalanche-zksync-networksintervals-supported-30m1h-2h-4h-8h-24h)

## WebSocket URL:   [Skip link to WebSocket URL:](https://docs.birdeye.so/reference/token-stats\#websocket-url)

```undefined
wss://public-api.birdeye.so/socket/solana?x-api-key=YOUR-API-KEY
```

### Header   [Skip link to Header](https://docs.birdeye.so/reference/token-stats\#header)

| Key | Value |
| --- | --- |
| `Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Protocol` | echo-protocol |

### Message   [Skip link to Message](https://docs.birdeye.so/reference/token-stats\#message)

**Subscription**

JSON

```json
{
    "type": "SUBSCRIBE_TOKEN_STATS",
    "data": {
        "address": "So11111111111111111111111111111111111111112",
        "select": {
            "price": true,
            "trade_data": {
                "volume": true,
                "trade": true,
                "price_history": true,
                "volume_history": true,
                "price_change": true,
                "trade_history": true,
                "trade_change": true,
                "volume_change": true,
                "unique_wallet": true,
                "unique_wallet_change":false,
                 "intervals": ["30m","1h", "2h", "4h", "8h", "24h"]
            },
            "fdv": true,
            "marketcap": true,
            "supply": true,
            "last_trade": true,
            "liquidity": true
        }
    }
}
```

On Solana, a valid address is required (e.g., 9SeRj4LjgENeKQujfxRNkGbXYPM3X2vr9C37Jg9AARfg).

A single connection supports querying multiple token addresses in one request, with a maximum of 100 addresses per call. (e.g., `"address": ["So11111111111111111111111111111111111111112" , "JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN" , "2zMMhcVQEXDtdE6vsFS7S7D5oUodfJHE8vd1gnBouauv"`\] )

**Unsubscription**

JSON

```json
{
    "type": "UNSUBSCRIBE_TOKEN_STATS",
    "data": {
        "address": "JUPyiwrYJFskUPiHa7hkeR8VUtAeFoSYbKedZNsDvCN"
    }
}
```

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/token-stats\#output-example)

JSON

```json
{
    "type": "TOKEN_STATS_DATA",
	  "data": {
				"address": "So11111111111111111111111111111111111111112",
        "price": 0.6124911619717852,
        "last_trade_human_time": "2025-07-21T10:47:21",
        "last_trade_unix_time": 1753094841,
        "circulating_supply": 3266503718.5056014,
        "total_supply": 6999203720.020869,
        "volume_30m_usd": 1366829.3607375324,
        "volume_30m": 2257825.6924440004,
        "volume_buy_30m": 1172585.030456,
        "volume_buy_30m_usd": 706769.6257229962,
        "volume_sell_30m": 1085240.6619880004,
        "volume_sell_30m_usd": 660059.7350145361,
        "trade_30m": 6961,
        "buy_30m": 3542,
        "sell_30m": 3419,
        "volume_history_30m": 1891967.984917,
        "volume_history_30m_usd": 1151063.2560477327,
        "volume_sell_history_30m_usd": 542627.1883311641,
        "volume_buy_history_30m_usd": 608436.0677165686,
        "price_change_30m_percent": 0.7034451034089814,
        "trade_history_30m": 7300,
        "buy_history_30m": 3746,
        "sell_history_30m": 3554,
        "trade_30m_change_percent": -4.6438356164383565,
        "buy_30m_change_percent": -5.445808862786973,
        "sell_30m_change_percent": -3.7985368598761955,
        "volume_30m_change_percent": 19.337415349713254,
        "volume_buy_30m_change_percent": 17.355263289649308,
        "volume_sell_30m_change_percent": 21.555755870562802,
        "unique_wallet_30m": 872,
        "volume_1h_usd": 2369309.1928942692,
        "volume_1h": 3905591.9729770003,
        "volume_buy_1h": 2029821.3635070003,
        "volume_buy_1h_usd": 1228939.4449818023,
        "volume_sell_1h": 1875770.60947,
        "volume_sell_1h_usd": 1140369.747912467,
        "trade_1h": 13196,
        "buy_1h": 6707,
        "sell_1h": 6489,
        "price_history_1h": 0.6075207638046215,
        "volume_history_1h": 3429726.1670990004,
        "volume_history_1h_usd": 2069932.9901114453,
        "volume_sell_history_1h_usd": 1165869.7367246232,
        "volume_buy_history_1h_usd": 904063.2533868221,
        "price_change_1h_percent": 0.8181445743576581,
        "trade_history_1h": 14402,
        "buy_history_1h": 7085,
        "sell_history_1h": 7317,
        "trade_1h_change_percent": -8.373836967087904,
        "buy_1h_change_percent": -5.335215243472124,
        "sell_1h_change_percent": -11.31611316113161,
        "volume_1h_change_percent": 13.874746341061572,
        "volume_buy_1h_change_percent": 35.2236520680655,
        "volume_sell_1h_change_percent": -2.7413593498410695,
        "unique_wallet_1h": 1437,
        "volume_2h_usd": 4282810.684122546,
        "volume_2h": 7075705.237234001,
        "volume_buy_2h": 3381695.0129840006,
        "volume_buy_2h_usd": 2043334.5141576885,
        "volume_sell_2h": 3694010.2242500004,
        "volume_sell_2h_usd": 2239476.169964857,
        "trade_2h": 26434,
        "buy_2h": 13180,
        "sell_2h": 13254,
        "price_history_2h": 0.6063547767506245,
        "volume_history_2h": 6893303.0001610005,
        "volume_history_2h_usd": 4123204.444135809,
        "volume_sell_history_2h_usd": 2037755.113346662,
        "volume_buy_history_2h_usd": 2085449.330789147,
        "price_change_2h_percent": 1.0120123492792037,
        "trade_history_2h": 25113,
        "buy_history_2h": 12719,
        "sell_history_2h": 12394,
        "trade_2h_change_percent": 5.260223788476088,
        "buy_2h_change_percent": 3.624498781350735,
        "sell_2h_change_percent": 6.938841374858802,
        "volume_2h_change_percent": 2.6460789126597266,
        "volume_buy_2h_change_percent": -2.9357435862631585,
        "volume_sell_2h_change_percent": 8.350117024740069,
        "unique_wallet_2h": 2596,
        "volume_4h_usd": 8379552.950957207,
        "volume_4h": 13933793.270382997,
        "volume_buy_4h": 7004135.598874,
        "volume_buy_4h_usd": 4209740.317892926,
        "volume_sell_4h": 6929657.671508998,
        "volume_sell_4h_usd": 4169812.6330642807,
        "trade_4h": 51847,
        "buy_4h": 26168,
        "sell_4h": 25679,
        "price_history_4h": 0.594915673250481,
        "volume_history_4h": 16115181.340853006,
        "volume_history_4h_usd": 9400106.00755909,
        "volume_sell_history_4h_usd": 4587212.788573528,
        "volume_buy_history_4h_usd": 4812893.218985564,
        "price_change_4h_percent": 2.9542823481647114,
        "trade_history_4h": 49996,
        "buy_history_4h": 25441,
        "sell_history_4h": 24555,
        "trade_4h_change_percent": 3.7022961836946955,
        "buy_4h_change_percent": 2.8575920757831845,
        "sell_4h_change_percent": 4.57747912848707,
        "volume_4h_change_percent": -13.536230367697147,
        "volume_buy_4h_change_percent": -15.010809488066545,
        "volume_sell_4h_change_percent": -11.992878440021276,
        "unique_wallet_4h": 4308,
        "volume_8h_usd": 17066532.375205405,
        "volume_8h": 28848660.361253,
        "volume_buy_8h": 14787909.828942003,
        "volume_buy_8h_usd": 8750498.560481448,
        "volume_sell_8h": 14060750.532311,
        "volume_sell_8h_usd": 8316033.8147239555,
        "trade_8h": 97640,
        "buy_8h": 49559,
        "sell_8h": 48081,
        "price_history_8h": 0.5606825478432808,
        "volume_history_8h": 13735997.243788,
        "volume_history_8h_usd": 7559098.0860442305,
        "volume_sell_history_8h_usd": 3840717.6276782625,
        "volume_buy_history_8h_usd": 3718380.458365968,
        "price_change_8h_percent": 9.240275861588927,
        "trade_history_8h": 55056,
        "buy_history_8h": 27497,
        "sell_history_8h": 27559,
        "trade_8h_change_percent": 77.34670154024992,
        "buy_8h_change_percent": 80.23420736807651,
        "sell_8h_change_percent": 74.46569178852643,
        "volume_8h_change_percent": 110.02232199995225,
        "volume_buy_8h_change_percent": 119.7829466686531,
        "volume_sell_8h_change_percent": 100.65053861899014,
        "unique_wallet_8h": 7487,
        "volume_24h_usd": 31377795.460723132,
        "volume_24h": 55157979.26257999,
        "volume_buy_24h": 28179370.839522,
        "volume_buy_24h_usd": 16042723.31421147,
        "volume_sell_24h": 26978608.423057996,
        "volume_sell_24h_usd": 15335072.146511663,
        "trade_24h": 198565,
        "buy_24h": 99895,
        "sell_24h": 98670,
        "price_history_24h": 0.5538567946828037,
        "volume_history_24h": 27728845.630605005,
        "volume_history_24h_usd": 14724976.832732132,
        "volume_sell_history_24h_usd": 7198790.159741187,
        "volume_buy_history_24h_usd": 7526186.672990945,
        "price_change_24h_percent": 10.586557364988488,
        "trade_history_24h": 109364,
        "buy_history_24h": 54904,
        "sell_history_24h": 54460,
        "trade_24h_change_percent": 81.56340294795362,
        "buy_24h_change_percent": 81.94484919131575,
        "sell_24h_change_percent": 81.1788468600808,
        "volume_24h_change_percent": 98.9191327954193,
        "volume_buy_24h_change_percent": 99.50077053786998,
        "volume_sell_24h_change_percent": 98.31521783016066,
        "unique_wallet_24h": 14036,
        "fdv": 4286950419.3528237,
        "marketcap": 2000704658.132653,
        "liquidity": 14376190.7797803
    }
}
```

**Response Parameters:**

| **Key** | **Data Type** | **Details** | **Example** |
| --- | --- | --- | --- |
| `address` | string | Address of the token | So11111111111111111111111111111111111111112 |
| `price` | number | Current token price in USD | 0.6124911619717852 |
| `last_trade_human_time` | string | Last trade time (human-readable) | "2025-07-21T10:47:21" |
| `last_trade_unix_time` | integer | Last trade time (Unix timestamp) | 1753094841 |
| `circulating_supply` | number | Circulating supply of the token | 3,266,503,718.5056014 |
| `total_supply` | number | Total supply of the token | 6,999,203,720.020869 |
| `fdv` | number | Fully Diluted Valuation (price × total supply) | 4,286,950,419.3528237 |
| `marketcap` | number | Market capitalization (price × circulating supply) | 2,000,704,658.132653 |
| `liquidity` | number | Total token liquidity in USD | 14,376,190.7797803 |
| `volume_30m_usd` | number | Total 30-minute volume in USD | 1,366,829.36 |
| `volume_1h_usd` | number | Total 1-hour volume in USD | 2,369,309.19 |
| `volume_2h_usd` | number | Total 2-hour volume in USD | 4,282,810.68 |
| `volume_4h_usd` | number | Total 4-hour volume in USD | 8,379,552.95 |
| `volume_8h_usd` | number | Total 8-hour volume in USD | 17,066,532.38 |
| `volume_24h_usd` | number | Total 24-hour volume in USD | 31,377,795.46 |
| `trade_30m` | integer | Number of trades in the last 30 minutes | 6,961 |
| `trade_1h` | integer | Number of trades in the last 1 hour | 13,196 |
| `trade_2h` | integer | Number of trades in the last 2 hours | 26,434 |
| `trade_4h` | integer | Number of trades in the last 4 hours | 51,847 |
| `trade_8h` | integer | Number of trades in the last 8 hours | 97,640 |
| `trade_24h` | integer | Number of trades in the last 24 hours | 198,565 |
| `buy_24h` | integer | Number of buy trades in last 24h | 99,895 |
| `sell_24h` | integer | Number of sell trades in last 24h | 98,670 |
| `price_change_30m_percent` | number | Price change in the last 30 minutes (percent) | 0.7034% |
| `price_change_1h_percent` | number | Price change in the last 1 hour (percent) | 0.8181% |
| `price_change_2h_percent` | number | Price change in the last 2 hours (percent) | 1.0120% |
| `price_change_4h_percent` | number | Price change in the last 4 hours (percent) | 2.9543% |
| `price_change_8h_percent` | number | Price change in the last 8 hours (percent) | 9.2403% |
| `price_change_24h_percent` | number | Price change in the last 24 hours (percent) | 10.5866% |
| `unique_wallet_30m` | integer | Number of unique wallets transacting in last 30 minutes | 872 |
| `unique_wallet_1h` | integer | Number of unique wallets transacting in last 1 hour | 1,437 |
| `unique_wallet_2h` | integer | Number of unique wallets transacting in last 2 hours | 2,596 |
| `unique_wallet_4h` | integer | Number of unique wallets transacting in last 4 hours | 4,308 |
| `unique_wallet_8h` | integer | Number of unique wallets transacting in last 8 hours | 7,487 |
| `unique_wallet_24h` | integer | Number of unique wallets transacting in last 24 hours | 14,036 |

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

StripeM-Inner
