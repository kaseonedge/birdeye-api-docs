
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Returns current price and 24h volume for a specific token — essential for token snapshots.
- Useful for lightweight dashboards, widgets, and summary views.
- Ideal for tracking real-time liquidity and token momentum.
- Helpful for building monitoring tools or alert systems for token performance.

address

string

required

The address of the token contract.

type

string

enum

required

Defaults to 24h

Time frame/interval.

1h2h4h8h24h

Allowed:

`1h``2h``4h``8h``24h`

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

# `` 200      JSON object containing price and volume with changes data of a token

object

success

boolean

required

data

object

required

price

number

required

updateUnixTime

integer

required

updateHumanTime

string

required

volumeUSD

number

required

volumeChangePercent

number

required

priceChangePercent

number

required

isScaledUiToken

boolean

scaledValue

number

multiplier

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

     --url 'https://public-api.birdeye.so/defi/price_volume/single?type=24h&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "isScaledUiToken": false,

    "price": 128.70426432642992,

    "updateUnixTime": 1726678569,

    "updateHumanTime": "2024-09-18T16:56:09",

    "volumeUSD": 755004403.5277437,

    "volumeChangePercent": -6.0377419970263055,

    "priceChangePercent": -2.6091746792986936

  }

}
```

* * *

