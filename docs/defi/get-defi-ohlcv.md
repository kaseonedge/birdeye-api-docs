
- Starter
- Premium
- Business
- Enterprise

required

The address of the token contract.

type

required

OHLCV time frame.

1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

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

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200** ✅ -      JSON object containing list of ohlcv data of a token


success

required

data

required

isScaledUiToken

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

address

required

type

required

unixTime

integer

required

currency

required

scaledO

scaledH

scaledL

scaledC

scaledV

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/ohlcv?type=1m&currency=usd&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



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
` `

