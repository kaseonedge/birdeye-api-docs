
  - Sub-minute intervals data starts from` May 2, 2025 16:30 UTC`
- Ethereum, BSC, Base:
  - Sub-minute intervals data starts from` May 9, 2025 00:00 UTC`
- Empty candles are not displayed
- Data retention for new intervals
  - `1s`: Up to 2 weeks
  - `15s` and `30s`: Up to 3 months

address

required

The address of a pair contract

type

required

OHLCV V3 time frame.

1s15s30s1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

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

mode

Select either range (time range) or count (number of candles). If mode is count, time\_from and time\_to params must exist but not both. Default: range

rangecount

`range` `count`

count\_limit

integer

0 to 5000

Specify the maximum candles returned. Only used with mode "count". Default: 5000

padding

Indicate whether to use padding on empty candles. Default: false

truefalse

`true` `false`

outlier

Indicate whether to allow outliers exist in the results. Default: true

truefalse

`true` `false`

inversion

Indicate whether to invert the base/quote on pair. Default: false

truefalse

`true` `false`

x-chain

Defaults to solana

Solana, Base, BSC, Ethereum, Monad network only.

solanaethereumbscbasemonad

`solana` `ethereum` `bsc` `base` `monad`

# 200      JSON object containing list of ohlcv data of a pair

success

required

data

required

items

array of objects

items

o

required

h

required

l

required

c

required

v

required

v\_usd

required

address

required

type

required

unix\_time

integer

required

currency

required

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/ohlcv/pair?type=1s' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "items": [\
\
      {\
\
        "address": "9wFFyRfZBsuAha4YcuxcXLKwMxJR43S7fPfQLusDBzvT",\
\
        "h": 210,\
\
        "o": 210,\
\
        "l": 210,\
\
        "c": 210,\
\
        "type": "15m",\
\
        "v": 0,\
\
        "unix_time": 1726670700,\
\
        "v_usd": 1000\
\
      },\
\
      {\
\
        "address": "9wFFyRfZBsuAha4YcuxcXLKwMxJR43S7fPfQLusDBzvT",\
\
        "h": 210,\
\
        "o": 210,\
\
        "l": 210,\
\
        "c": 210,\
\
        "type": "15m",\
\
        "v": 0,\
\
        "unix_time": 1726671600,\
\
        "v_usd": 1000\
\
      }\
\
    ]

  }

}
` `

