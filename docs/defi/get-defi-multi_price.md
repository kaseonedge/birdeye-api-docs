| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Always use the checksum contract address on supported chains.
- Solana and EVM chains will have different response schemas.
- Separate token addresses in string by commas (,)
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

Ideas 💡

- Efficiently fetch prices for multiple tokens in one request.
- Ideal for portfolio trackers, token lists, or price comparison tools.
- Combine with multi-volume and liquidity endpoints for full token overviews.
- Useful for minimizing API calls when displaying multiple assets.

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

list\_address

string

required

A list of token addresses in string separated by commas (,)

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

# `` 200      JSON object containing price values and update time of multiple tokens

object

success

boolean

required

data

object

required

A hashmap with token addresses as keys and the price object as value

View Additional Properties

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

     --url 'https://public-api.birdeye.so/defi/multi_price?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "So11111111111111111111111111111111111111112": {

      "isScaledUiToken": false,

      "value": 127.32916175338693,

      "updateUnixTime": 1726673192,

      "updateHumanTime": "2024-09-18T15:26:32",

      "priceInNative": 1,

      "priceChange24h": -5.833510393308625,

      "liquidity": 7026264396

    },

    "DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263": {

      "isScaledUiToken": false,

      "value": 0.00001598090539282,

      "updateUnixTime": 1726673185,

      "updateHumanTime": "2024-09-18T15:26:25",

      "priceInNative": 1.2583e-7,

      "priceChange24h": -4.766925300538944,

      "liquidity": 1234414

    }

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
