| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Retrieving recent requests… |

LoadingLoading…

#### URL Expired

The URL for this request expired after 30 days.

address

string

required

The address of a pair contract

offset

integer

0 to 9999

Defaults to 0

Make sure offset + limit <= 10000

limit

integer

1 to 50

Defaults to 50

Number of items per page.

tx\_type

string

enum

Defaults to swap

swapaddremoveall

Allowed:

`swap``add``remove``all`

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

ui\_amount\_mode

string

enum

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

Allowed:

`raw``scaled`

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing transactions of a pair

object

success

boolean

required

data

object

required

items

array of objects

required

items\*

object

View Additional Properties

hasNext

boolean

required

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

     --url 'https://public-api.birdeye.so/defi/txs/pair?offset=0&limit=50&tx_type=swap&sort_type=desc&ui_amount_mode=scaled' \

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
        "txHash": "2s27V8t3HANqUA572KLqBNXFvGyqvYobFX2Cn3c5puoWbHSNCebjT6PDX7gixe5HjdNhuG7SuHpDroJXFrBpAFn1",\
\
        "source": "phoenix",\
\
        "blockUnixTime": 1754882843,\
\
        "txType": "swap",\
\
        "address": "4DoNfFBfF7UokCC2FQzriy7yHK6DY6NVdYpuekQ5pRgg",\
\
        "owner": "MfDuWeqSHEqTFVYZ7LoexgAK9dxk7cy4DFJWjWMGVWa",\
\
        "from": {\
\
          "symbol": "USDC",\
\
          "decimals": 6,\
\
          "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",\
\
          "amount": 4000129768,\
\
          "type": "log",\
\
          "typeSwap": "from",\
\
          "uiAmount": 4000.129768,\
\
          "price": 0.99986,\
\
          "nearestPrice": 0.99986,\
\
          "changeAmount": -4000129768,\
\
          "uiChangeAmount": -4000.129768,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "to": {\
\
          "symbol": "SOL",\
\
          "decimals": 9,\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "amount": 21638000000,\
\
          "type": "log",\
\
          "typeSwap": "to",\
\
          "uiAmount": 21.638,\
\
          "price": 184.67395202659998,\
\
          "nearestPrice": 184.67395202659998,\
\
          "changeAmount": 21638000000,\
\
          "uiChangeAmount": 21.638,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        }\
\
      }\
\
    ],

    "hasNext": true

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
