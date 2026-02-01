| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Business
- Enterprise

Ideas 💡

- Great for ranking tokens by trading activity and popularity.
- Helps detect high-performing or high-interest tokens.
- Use to analyze token traction over time, especially for DeFi token analytics.
- Ideal for token dashboards, analytics tools, and alert systems.

time\_frame

string

enum

required

Defaults to 24h

Time interval (Example: '24h')

1m5m30m1h2h4h8h24h3d7d14d30d90d180d1yalltime

Show 16 enum values

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

# `` 200      OK

object

data

array of objects

data

object

address

string

total\_volume

number

total\_volume\_usd

number

volume\_buy\_usd

number

volume\_sell\_usd

number

volume\_buy

number

volume\_sell

number

total\_trade

number

buy

number

sell

number

success

boolean

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

curl --request POST \

     --url 'https://public-api.birdeye.so/defi/v3/all-time/trades/multiple?time_frame=24h&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "data": [\
\
    {\
\
      "address": "So11111111111111111111111111111111111111112",\
\
      "total_volume": 158766463.26959822,\
\
      "total_volume_usd": 20188521260.405678,\
\
      "volume_buy_usd": 20188521260.405678,\
\
      "volume_sell_usd": 20188521260.405678,\
\
      "volume_buy": 78227859.16098201,\
\
      "volume_sell": 80538604.1086162,\
\
      "total_trade": 258522892,\
\
      "buy": 87829497,\
\
      "sell": 170693395\
\
    }\
\
  ],

  "success": true

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
