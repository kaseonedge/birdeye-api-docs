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

- Retrieves historical USD price at a specific timestamp — perfect for backtesting.
- Great for calculating portfolio value or token price at a specific moment.
- Can be used to track price before/after events (e.g. listings, major announcements).
- Helpful for building historical analytics, ROI calculators, and trade performance tools.

address

string

required

The address of the token contract.

address\_type

string

enum

required

tokenpair

Allowed:

`token``pair`

type

string

enum

required

OHLCV time frame.

1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

Show 15 enum values

time\_from

integer

required

0 to 10000000000

Specify the start time using unix timestamps in seconds

time\_to

integer

required

0 to 10000000000

Specify the end time using unix timestamps in seconds

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

# `` 200      JSON object containing values and unix timestamps of a token or pair

object

success

boolean

required

data

object

required

isScaledUiToken

boolean

multiplier

number

items

array of objects

required

items\*

object

unixTime

integer

value

number

scaledValue

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

     --url 'https://public-api.birdeye.so/defi/history_price?address_type=token&type=1m&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "isScaledUiToken": false,

    "items": [\
\
      {\
\
        "unixTime": 1726670700,\
\
        "value": 127.97284640184616\
\
      },\
\
      {\
\
        "unixTime": 1726671600,\
\
        "value": 128.04188346328968\
\
      },\
\
      {\
\
        "unixTime": 1726672500,\
\
        "value": 127.40223856228901\
\
      }\
\
    ]

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
