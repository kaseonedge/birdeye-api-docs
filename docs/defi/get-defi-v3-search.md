
- Starter
- Premium
- Business
- Enterprise

chain

string

enum

Defaults to all

Specify the chain.

allsolanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 16 enum values

keyword

string

target

string

enum

Defaults to all

An option to search tokens based on their expected results as token, market, or both.

alltokenmarket

Allowed:

`all``token``market`

search\_mode

string

enum

Defaults to exact

An option to search tokens with exact match or partially match.

exactfuzzy

Allowed:

`exact``fuzzy`

search\_by

string

enum

Defaults to symbol

An option to search tokens by symbol, name, or both.

combinationaddressnamesymbol

Allowed:

`combination``address``name``symbol`

sort\_by

string

enum

required

Defaults to volume\_24h\_usd

Specify the sort field.

fdvmarketcapliquiditypriceprice\_change\_24h\_percenttrade\_24htrade\_24h\_change\_percentbuy\_24hbuy\_24h\_change\_percentsell\_24hsell\_24h\_change\_percentunique\_wallet\_24hunique\_view\_24h\_change\_percentlast\_trade\_unix\_timevolume\_24h\_usdvolume\_24h\_change\_percent

Show 16 enum values

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

verify\_token

boolean

enum

A filter to retrieve tokens based on their verification status (supported on Solana).

truetruefalse

Allowed:

`true``false`

markets

string

A comma-separated list of market sources to filter results (supported on Solana). Available options: \['Raydium', 'Raydium CP', 'Raydium Clamm', 'Meteora', 'Meteora DLMM', 'Fluxbeam', 'Pump.fun', 'OpenBook', 'OpenBook V2', 'Orca'\].

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 20

Defaults to 20

Number of items per page.

ui\_amount\_mode

string

enum

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

Allowed:

`raw``scaled`

# `` 200      Search for token and market data matching keyword, tokenAddress using full-text search

object

success

boolean

required

data

object

required

items

array of objects

required

items\*

object

type

string

required

result

array

required

result\*

object

object

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

Updated 2 months ago

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/search?chain=all&target=all&search_mode=exact&search_by=symbol&sort_by=volume_24h_usd&sort_type=desc&offset=0&limit=20&ui_amount_mode=scaled' \

     --header 'accept: application/json'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "items": [\
\
      {\
\
        "type": "token",\
\
        "result": [\
\
          {\
\
            "name": "TRENDSDOTFUN",\
\
            "symbol": "",\
\
            "address": "CdsF47CkMGnXnMuGNPw9TpCbE6hxRvA4XUbxbZcLrfJ8",\
\
            "network": "solana",\
\
            "decimals": 6,\
\
            "verified": false,\
\
            "fdv": 13697.614698138917,\
\
            "market_cap": 13697.614698138917,\
\
            "liquidity": 60054.03786109897,\
\
            "price": 0.000013697614670743687,\
\
            "price_change_24h_percent": 333.97707074856015,\
\
            "sell_24h": 4088,\
\
            "sell_24h_change_percent": null,\
\
            "buy_24h": 4374,\
\
            "buy_24h_change_percent": null,\
\
            "unique_wallet_24h": 203,\
\
            "unique_wallet_24h_change_percent": null,\
\
            "trade_24h": 8462,\
\
            "trade_24h_change_percent": null,\
\
            "volume_24h_change_percent": null,\
\
            "volume_24h_usd": 1867782.2902830783,\
\
            "last_trade_unix_time": 1749490559,\
\
            "last_trade_human_time": "2025-06-09T17:35:59",\
\
            "updated_time": 1749491343,\
\
            "creation_time": "2025-06-09T17:13:02.490Z",\
\
            "is_scaled_ui_token": false,\
\
            "multiplier": null\
\
          }\
\
        ]\
\
      },\
\
      {\
\
        "type": "market",\
\
        "result": []\
\
      }\
\
    ]

  }

}
```

Updated 2 months ago

* * *

