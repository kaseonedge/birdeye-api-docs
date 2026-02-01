| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Always use the checksum contract address on supported chains.
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

list\_address

string

required

A list of token addresses in string separated by commas (,)

x-chain

string

enum

Defaults to base

Base network only.

base

Allowed:

`base`

# `` 200      OK

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

A list of objects containing token exit liquidity data

items\*

object

token

string

required

exit\_liquidity

number

required

liquidity

number

required

price

object

required

price object

currency

string

required

address

string

required

name

string

required

symbol

string

required

decimals

string

required

extensions

object

required

Has additional fields

logo\_uri

string

required

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

Updated 17 days ago

* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

curl --request GET \

     --url https://public-api.birdeye.so/defi/v3/token/exit-liquidity/multiple \

     --header 'accept: application/json' \

     --header 'x-chain: base'
```

```

xxxxxxxxxx



{

  "data": {

    "items": [\
\
      {\
\
        "token": "0x60a3E35Cc302bFA44Cb288Bc5a4F316Fdb1adb42",\
\
        "exit_liquidity": 6719817.16468568,\
\
        "liquidity": 10277766.97799163,\
\
        "price": {\
\
          "value": 1.1516170107394188,\
\
          "update_unix_time": 1750385591,\
\
          "update_human_time": "2025-06-20T02:13:11",\
\
          "update_in_slot": 31798122\
\
        },\
\
        "currency": "USD",\
\
        "address": "0x60a3E35Cc302bFA44Cb288Bc5a4F316Fdb1adb42",\
\
        "name": "EURC",\
\
        "symbol": "EURC",\
\
        "decimals": 6,\
\
        "extensions": {\
\
          "twitter": "https://twitter.com/circlepay",\
\
          "website": "https://www.circle.com",\
\
          "telegram": null\
\
        },\
\
        "logo_uri": "https://coin-images.coingecko.com/coins/images/26045/small/euro.png?1696525125"\
\
      },\
\
      {\
\
        "token": "0xD7eA1d4d2528fc6Ff010006694C3489f386e2532",\
\
        "exit_liquidity": 162397.14079820755,\
\
        "liquidity": 324794.2815964151,\
\
        "price": {\
\
          "value": 0.0016673684083016622,\
\
          "update_unix_time": 1750385591,\
\
          "update_human_time": "2025-06-20T02:13:11",\
\
          "update_in_slot": 31798122\
\
        },\
\
        "currency": "USD",\
\
        "address": "0xD7eA1d4d2528fc6Ff010006694C3489f386e2532",\
\
        "name": "JPmorgan Dollar",\
\
        "symbol": "JPMD",\
\
        "decimals": 18,\
\
        "extensions": {\
\
          "twitter": null,\
\
          "website": null,\
\
          "telegram": null\
\
        },\
\
        "logo_uri": "https://dd.dexscreener.com/ds-data/tokens/base/0xd7ea1d4d2528fc6ff010006694c3489f386e2532.png?size=xl"\
\
      }\
\
    ]

  },

  "success": true

}
```

Updated 17 days ago

* * *

Did this page help you?

Yes

No
