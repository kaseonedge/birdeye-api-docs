| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Standard
- Lite
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Returns a comprehensive list of supported tokens with metadata.
- Useful as a **token registry** for symbol, name, logo URI, and decimal info.
- Ideal for auto-complete search bars, dropdown selectors, or asset explorers.
- Can be cached for improving performance across token-based interfaces.

sort\_by

string

enum

required

Defaults to v24hUSD

Specify the sort field.

mcv24hUSDv24hChangePercentliquidity

Allowed:

`mc``v24hUSD``v24hChangePercent``liquidity`

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 50

Defaults to 50

Number of items per page.

min\_liquidity

number

≥ 0

Defaults to 100

Specify the lower bound of liquidity. Filter for records with liquidity greater than the minimum liquidity value, excluding those with liquidity equal to the minimum.

max\_liquidity

number

Specify the upper bound of liquidity. Filter for records with liquidity less than the maximum liquidity value, excluding those with liquidity equal to the maximum.

ui\_amount\_mode

string

enum

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

Allowed:

`raw``scaled`

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing a list of tokens with certain fields

object

success

boolean

required

data

object

required

updateUnixTime

integer

updateTime

string

total

number

tokens

array of objects

tokens

object

address

string

decimals

integer

lastTradeUnixTime

integer

liquidity

number

logoURI

string

mc

number

name

string

symbol

string

v24hChangePercent

number

v24hUSD

number

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

Updated 24 days ago

* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/tokenlist?sort_by=v24hUSD&sort_type=desc&offset=0&limit=50&min_liquidity=100&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "updateUnixTime": 1754885276,

    "updateTime": "2025-08-11T04:07:56.945Z",

    "tokens": [\
\
      {\
\
        "isScaledUiToken": false,\
\
        "multiplier": null,\
\
        "address": "So11111111111111111111111111111111111111112",\
\
        "decimals": 9,\
\
        "price": 185.45023454574132,\
\
        "lastTradeUnixTime": 1754885221,\
\
        "liquidity": 23349538049.2037,\
\
        "logoURI": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
        "mc": 100058305776.50261,\
\
        "name": "Wrapped SOL",\
\
        "symbol": "SOL",\
\
        "v24hChangePercent": -1.4820129368250423,\
\
        "v24hUSD": 9515832024.915321\
\
      }\
\
    ],

    "total": 298068

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
