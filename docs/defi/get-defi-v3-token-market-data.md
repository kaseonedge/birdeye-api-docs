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

address

string

required

The address of the token contract.

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

# `` 200      JSON object containing market data of a specific token

object

success

boolean

required

data

object

required

address

string

required

price

number

required

liquidity

number

required

total\_supply

number

required

circulating\_supply

number

required

market\_cap

number

required

fdv

number

required

holder

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

     --url 'https://public-api.birdeye.so/defi/v3/token/market-data?ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "address": "So11111111111111111111111111111111111111112",

    "price": 185.74132384799458,

    "liquidity": 23338480211.61425,

    "total_supply": 607187823.0928401,

    "circulating_supply": 539542621.8877238,

    "fdv": 112779870085.64606,

    "market_cap": 100215360861.8438,

    "holder": 3498897,

    "is_scaled_ui_token": false,

    "multiplier": null

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
