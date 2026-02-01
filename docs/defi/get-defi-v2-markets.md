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

Defaults to liquidity

Specify the sort field.

liquidityvolume24h

Allowed:

`liquidity``volume24h`

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 20

Defaults to 10

Number of items per page.

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing a list of markets of a token

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

View Additional Properties

total

integer

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

     --url 'https://public-api.birdeye.so/defi/v2/markets?time_frame=24h&sort_type=desc&sort_by=liquidity&offset=0&limit=10' \

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
        "address": "Jito4APyf642JPZPx3hGc6WWJ8zPKtRbRs4P815Awbb",\
\
        "base": {\
\
          "address": "J1toso1uCk3RLmjorhTtrVwY9HJ7X8V9yYac6Y7kGCPn",\
\
          "decimals": 9,\
\
          "symbol": "JitoSOL",\
\
          "icon": "https://img.fotofolio.xyz/?url=https%3A%2F%2Fstorage.googleapis.com%2Ftoken-metadata%2FJitoSOL-256.png"\
\
        },\
\
        "createdAt": "2024-05-28T07:19:22.813Z",\
\
        "liquidity": 1733225301.1348372,\
\
        "name": "JitoSOL-SOL",\
\
        "price": null,\
\
        "quote": {\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "decimals": 9,\
\
          "icon": "https://img.fotofolio.xyz/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fsolana-labs%2Ftoken-list%2Fmain%2Fassets%2Fmainnet%2FSo11111111111111111111111111111111111111112%2Flogo.png",\
\
          "symbol": "SOL"\
\
        },\
\
        "source": "Stake Pool",\
\
        "trade24h": 1021,\
\
        "trade24hChangePercent": 72.46621621621621,\
\
        "uniqueWallet24h": 382,\
\
        "uniqueWallet24hChangePercent": -13.769751693002258,\
\
        "volume24h": 7610352.270776577\
\
      }\
\
    ],

    "total": 1523

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
