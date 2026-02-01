
- Lite
- Starter
- Premium
- Business
- Enterprise

required

The address of the token contract.

address\_type

required

tokenpair

`token` `pair`

type

required

OHLCV time frame.

1m3m5m15m30m1H2H4H6H8H12H1D3D1W1M

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

**200**✅ - JSON object containing values and unix timestamps of a token or pair


success

required

data

required

isScaledUiToken

multiplier

items

array of objects

required

items\*

unixTime

integer

value

scaledValue

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/history_price?address_type=token&type=1m&ui_amount_mode=raw' \

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
` `

