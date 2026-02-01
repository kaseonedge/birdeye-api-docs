
- Solana and EVM chains will have different response schemas.
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

Ideas 💡

- Fetch real-time token prices across supported chains.
- Use in charts, widgets, or portfolio dashboards for up-to-date price feeds.
- Combine with volume and liquidity endpoints to show token health.
- Essential for bots, alerts, or price-based analytics triggers.

check\_liquidity

number

Specify the liquidity value to check.

include\_liquidity

boolean

enum

Specify whether to include liquidity in the response.

truefalse

Allowed:

`true``false`

address

string

required

The address of the token contract.

ui\_amount\_mode

string

enum

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

Allowed:

`raw``scaled``both`

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing price value and update time of a token

object

success

boolean

required

data

object

required

value

number

required

updateUnixTime

integer

required

updateHumanTime

string

required

priceChange24h

number

required

priceInNative

number

liquidity

number

isScaledUiToken

boolean

scaledValue

number

multiplier

number

scaledPriceInNative

number

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/price?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "data": {

    "isScaledUiToken": false,

    "value": 0.38622452197470425,

    "updateUnixTime": 1745058945,

    "updateHumanTime": "2025-04-19T10:35:45",

    "priceChange24h": 1.933391934259418,

    "priceInNative": 0.0027761598581298626,

    "liquidity": 10854103.37938592

  },

  "success": true

}
```

* * *

