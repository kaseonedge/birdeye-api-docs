
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Useful for generating candlestick charts (Open, High, Low, Close, Volume).
- Ideal for visualizing token price trends across time intervals.
- Supports custom granularity (1m, 5m, 1h, 1d) for different chart types.
- Great for technical analysis tools, trading dashboards, or historical backtesting.

address

string

required

The address of the token contract.

type

string

enum

required

OHLCV time frame.

1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

Show 15 enum values

currency

string

enum

Defaults to usd

Currency in which OHLCV data is presented. Choose between usd or native token.

usdnative

Allowed:

`usd``native`

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

# `` 200      JSON object containing list of ohlcv data of a token

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

v

number

required

address

string

required

type

string

required

unixTime

integer

required

currency

string

required

scaledO

number

scaledH

number

scaledL

number

scaledC

number

scaledV

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

     --url 'https://public-api.birdeye.so/defi/ohlcv?type=1m&currency=usd&ui_amount_mode=raw' \

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
        "o": 128.27328370924414,\
\
        "h": 128.6281001340782,\
\
        "l": 127.91200927364626,\
\
        "c": 127.97284640184616,\
\
        "v": 58641.16636665621,\
\
        "unixTime": 1726670700,\
\
        "address": "So11111111111111111111111111111111111111112",\
\
        "type": "15m",\
\
        "currency": "usd"\
\
      },\
\
      {\
\
        "o": 127.97284640184616,\
\
        "h": 128.49450996585105,\
\
        "l": 127.89354285873108,\
\
        "c": 128.04188346328968,\
\
        "v": 47861.13031539581,\
\
        "unixTime": 1726671600,\
\
        "address": "So11111111111111111111111111111111111111112",\
\
        "type": "15m",\
\
        "currency": "usd"\
\
      }\
\
    ]

  }

}
```

* * *

