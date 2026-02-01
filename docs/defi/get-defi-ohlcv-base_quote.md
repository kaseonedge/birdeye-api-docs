
- Starter
- Premium
- Business
- Enterprise

required

The address of the base token.

quote\_address

required

The address of the quote token.

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

**200** ✅ - JSON object containing list of ohlc and volume of base and quote


success

required

data

required

isScaledUiTokenBase

isScaledUiTokenQuote

multiplierBase

multiplierQuote

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

vBase

vQuote

unixTime

integer

required

scaledO

scaledH

scaledL

scaledC

scaledVBase

scaledVQuote

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/ohlcv/base_quote?type=1m&ui_amount_mode=raw' \

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
` `

