
- Lite
- Starter
- Premium
- Business
- Enterprise

required

The address of a pair contract

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

SVM networks only.

solanafogo

`solana` `fogo`


## Responses

**200**✅ - JSON object containing pair(market) overview data of a specific pair


success

required

data

required

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/pair/overview/single?ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "address": "4DoNfFBfF7UokCC2FQzriy7yHK6DY6NVdYpuekQ5pRgg",

    "base": {

      "address": "So11111111111111111111111111111111111111112",

      "decimals": 9,

      "icon": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",

      "symbol": "SOL",

      "is_scaled_ui_token": false,

      "multiplier": 1

    },

    "created_at": "2023-02-28T03:00:02.253Z",

    "name": "SOL-USDC",

    "quote": {

      "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",

      "decimals": 6,

      "icon": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v/logo.png",

      "symbol": "USDC",

      "is_scaled_ui_token": false,

      "multiplier": 1

    },

    "source": "Phoenix",

    "liquidity": 2798754.646440928,

    "liquidity_change_percentage_24h": null,

    "price": 185.2259461756374,

    "trade_24h": 1088,

    "trade_24h_change_percent": -16.628352490421456,

    "trade_history_24h": 1305,

    "unique_wallet_24h": 183,

    "unique_wallet_24h_change_percent": -39.40397350993378,

    "volume_24h": 3960934.260889339,

    "volume_24h_base": 21735.928,

    "volume_24h_change_percentage_24h": null,

    "volume_24h_quote": 3961073.7718080003,

    "volume_12h": 2371020.4454601924,

    "volume_12h_base": 12961.386,

    "volume_12h_quote": 2371101.2224080004,

    "volume_1h": 167126.90920284906,

    "volume_1h_base": 902.8530000000001,

    "volume_1h_quote": 167127.603103,

    "volume_2h": 528203.5824244855,

    "volume_2h_base": 2859.9010000000003,

    "volume_2h_quote": 528219.775809,

    "volume_30m": 111882.67078251604,

    "volume_30m_base": 604.808,

    "volume_30m_quote": 111883.36210299999,

    "volume_4h": 848002.9830474032,

    "volume_4h_base": 4613.238,

    "volume_4h_quote": 848022.866258,

    "volume_8h": 2042469.7997546664,

    "volume_8h_base": 11160.507,

    "volume_8h_quote": 2042534.6387080003,

    "trade_12h": 531,

    "trade_12h_change_percent": -4.838709677419355,

    "trade_1h": 33,

    "trade_1h_change_percent": -62.06896551724138,

    "trade_2h": 120,

    "trade_2h_change_percent": 118.18181818181819,

    "trade_30m": 9,

    "trade_30m_change_percent": -60.86956521739131,

    "trade_4h": 175,

    "trade_4h_change_percent": -16.666666666666664,

    "trade_8h": 385,

    "trade_8h_change_percent": 41.02564102564102,

    "trade_history_12h": 558,

    "trade_history_1h": 87,

    "trade_history_2h": 55,

    "trade_history_30m": 23,

    "trade_history_4h": 210,

    "trade_history_8h": 273,

    "unique_wallet_12h": 112,

    "unique_wallet_12h_change_percent": 19.148936170212767,

    "unique_wallet_1h": 14,

    "unique_wallet_1h_change_percent": -44,

    "unique_wallet_2h": 30,

    "unique_wallet_2h_change_percent": 57.89473684210527,

    "unique_wallet_30m": 4,

    "unique_wallet_30m_change_percent": -66.66666666666666,

    "unique_wallet_4h": 39,

    "unique_wallet_4h_change_percent": -29.09090909090909,

    "unique_wallet_8h": 83,

    "unique_wallet_8h_change_percent": 29.6875

  }

}
` `

