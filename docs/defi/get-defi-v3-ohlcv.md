| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Solana:
  - Sub-minute intervals data starts from` May 2, 2025 16:30 UTC`
- Ethereum, BSC, Base:
  - Sub-minute intervals data starts from` May 9, 2025 00:00 UTC`
- Empty candles are not displayed
- Data retention for new intervals
  - `1s`: Up to 2 weeks
  - `15s` and `30s`: Up to 3 months

address

string

required

The address of the token contract.

type

string

enum

required

OHLCV V3 time frame.

1s15s30s1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

Show 18 enum values

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

mode

string

enum

Select either range (time range) or count (number of candles). If mode is count, time\_from and time\_to params must exist but not both. Default: range

rangecount

Allowed:

`range``count`

count\_limit

integer

0 to 5000

Specify the maximum candles returned. Only used with mode "count". Default: 5000

padding

boolean

enum

Indicate whether to use padding on empty candles. Default: false

truefalse

Allowed:

`true``false`

outlier

boolean

enum

Indicate whether to allow outliers exist in the results. Default: true

truefalse

Allowed:

`true``false`

x-chain

string

enum

Defaults to solana

Solana, Base, BSC, Ethereum, Monad network only.

solanaethereumbscbasemonad

Allowed:

`solana``ethereum``bsc``base``monad`

# `` 200      JSON object containing list of ohlcv data of a token

object

success

boolean

required

data

object

required

is\_scaled\_ui\_token

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

v\_usd

number

required

address

string

required

type

string

required

unix\_time

integer

required

currency

string

required

scaled\_o

number

scaled\_h

number

scaled\_l

number

scaled\_c

number

scaled\_v

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

     --url 'https://public-api.birdeye.so/defi/v3/ohlcv?type=1s&currency=usd&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



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
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
