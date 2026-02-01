| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Standard
- Lite
- Starter
- Premium
- Business
- Enterprise

address

string

required

The address of the token contract.

time\_frame

string

enum

required

Defaults to 24h

30m1h2h4h6h8h12h24h

Show 8 enum values

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

sort\_by

string

enum

required

Defaults to volume

Specify the sort field.

volumetrade

Allowed:

`volume``trade`

offset

integer

0 to 10000

Defaults to 0

Pagination start position. offset + limit <= 10000

limit

integer

1 to 10

Defaults to 10

Number of items per page.

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

# `` 200      JSON object containing a list of top traded tokens

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

tokenAddress

string

owner

string

tags

array

tags

type

string

volume

number

trade

integer

tradeBuy

integer

tradeSell

integer

volumeBuy

number

volumeSell

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

     --url 'https://public-api.birdeye.so/defi/v2/tokens/top_traders?time_frame=24h&sort_type=desc&sort_by=volume&offset=0&limit=10&ui_amount_mode=scaled' \

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
        "tokenAddress": "So11111111111111111111111111111111111111112",\
\
        "owner": "MfDuWeqSHEqTFVYZ7LoexgAK9dxk7cy4DFJWjWMGVWa",\
\
        "tags": [],\
\
        "type": "24h",\
\
        "volume": 1649180.8809921234,\
\
        "trade": 195729,\
\
        "tradeBuy": 101729,\
\
        "tradeSell": 94000,\
\
        "volumeBuy": 827695.1022708704,\
\
        "volumeSell": 821485.7787212529,\
\
        "isScaledUiToken": false,\
\
        "multiplier": null\
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
