
- Lite
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Generates OHLCV data (Open, High, Low, Close, Volume) for a specific token pair.
- Perfect for candlestick visualizations and pair-based price tracking.
- Useful for DEX-specific analytics, pair monitoring, and market depth analysis.
- Ideal for building custom charts, trade history tools, or price movement alerts.

address

string

required

The address of a pair contract

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

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing list of ohlcv data of a pair

object

success

boolean

required

data

object

required

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

     --url 'https://public-api.birdeye.so/defi/ohlcv/pair?type=1m' \

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
        "address": "Czfq3xZZDmsdGdUyrNLtRhGc47cXcZtLG4crryfu44zE",\
\
        "c": 131.98629958196778,\
\
        "h": 132.23482213379438,\
\
        "l": 131.51590533656915,\
\
        "o": 131.51590533656915,\
\
        "type": "15m",\
\
        "unixTime": 1726700400,\
\
        "v": 6156.155046497001\
\
      },\
\
      {\
\
        "address": "Czfq3xZZDmsdGdUyrNLtRhGc47cXcZtLG4crryfu44zE",\
\
        "c": 132.7284,\
\
        "h": 132.81605139774013,\
\
        "l": 131.95800580371125,\
\
        "o": 131.98629958196778,\
\
        "type": "15m",\
\
        "unixTime": 1726701300,\
\
        "v": 7401.823317684\
\
      }\
\
    ]

  }

}
```

* * *

