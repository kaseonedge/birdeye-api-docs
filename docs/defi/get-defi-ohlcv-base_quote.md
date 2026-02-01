
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Retrieves OHLCV data across **multiple pairs** sharing the same base and quote tokens.
- Great for analyzing aggregate price trends across different DEXs for a token pair.
- Ideal for building more accurate, multi-source candlestick charts.
- Useful in trading platforms that want to consolidate data from all available liquidity pools.

base\_address

string

required

The address of the base token.

quote\_address

string

required

The address of the quote token.

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

# `` 200      JSON object containing list of ohlc and volume of base and quote

object

success

boolean

required

data

object

required

isScaledUiTokenBase

boolean

isScaledUiTokenQuote

boolean

multiplierBase

number

multiplierQuote

number

items

array of objects

items

object

o

number

required

h

number

required

l

number

required

c

number

required

vBase

number

vQuote

number

unixTime

integer

required

scaledO

number

scaledH

number

scaledL

number

scaledC

number

scaledVBase

number

scaledVQuote

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

     --url 'https://public-api.birdeye.so/defi/ohlcv/base_quote?type=1m&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
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
        "o": 128.2848293438851,\
\
        "c": 127.98180512820512,\
\
        "h": 128.64650816293124,\
\
        "l": 127.91584674904873,\
\
        "vBase": 58641.16636665621,\
\
        "vQuote": 4362436.09417201,\
\
        "unixTime": 1726670700\
\
      },\
\
      {\
\
        "o": 127.98180512820512,\
\
        "c": 128.0549796460581,\
\
        "h": 128.51250171609132,\
\
        "l": 127.89610078074669,\
\
        "vBase": 47861.13031539581,\
\
        "vQuote": 3913815.120231004,\
\
        "unixTime": 1726671600\
\
      }\
\
    ],

    "baseAddress": "So11111111111111111111111111111111111111112",

    "quoteAddress": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",

    "isScaledUiTokenBase": false,

    "isScaledUiTokenQuote": false,

    "type": "15m"

  }

}
```

* * *

