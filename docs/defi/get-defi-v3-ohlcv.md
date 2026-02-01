
  - Sub-minute intervals data starts from` May 2, 2025 16:30 UTC`
- Ethereum, BSC, Base:
  - Sub-minute intervals data starts from` May 9, 2025 00:00 UTC`
- Empty candles are not displayed
- Data retention for new intervals
  - `1s`: Up to 2 weeks
  - `15s` and `30s`: Up to 3 months

address

required

The address of the token contract.

type

required

OHLCV V3 time frame.

1s15s30s1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

currency

Defaults to usd

Currency in which OHLCV data is presented. Choose between usd or native token.

usdnative

`usd` `native`

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

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

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

x-chain

Defaults to solana

Solana, Base, BSC, Ethereum, Monad network only.

solanaethereumbscbasemonad

`solana` `ethereum` `bsc` `base` `monad`


## Responses

**200** ✅ -      JSON object containing list of ohlcv data of a token


success

required

data

required

is\_scaled\_ui\_token

multiplier

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

scaled\_o

scaled\_h

scaled\_l

scaled\_c

scaled\_v

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/ohlcv?type=1s&currency=usd&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "is_scaled_ui_token": false,

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
        "v_usd": 7506048,\
\
        "unix_time": 1726670700,\
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
        "v_usd": 7506048,\
\
        "unix_time": 1726671600,\
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
` `

