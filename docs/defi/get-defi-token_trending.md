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

sort\_by

string

enum

required

Defaults to rank

Specify the sort field.

rankvolumeUSDliquidity

Allowed:

`rank``volumeUSD``liquidity`

interval

string

enum

Defaults to 24h

Specify the interval of trending.

1h4h24h

Allowed:

`1h``4h``24h`

sort\_type

string

enum

required

Defaults to asc

Specify the sort order.

ascdesc

Allowed:

`asc``desc`

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 20

Defaults to 20

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

# `` 200      JSON object containing a list of trending tokens

object

success

boolean

required

data

object

required

updateUnixTime

integer

updateTime

string

total

number

tokens

array of objects

tokens

object

address

string

decimals

integer

liquidity

number

logoURI

string

name

string

symbol

string

volume24hUSD

number

volume24hChangePercent

number

rank

integer

price

number

price24hChangePercent

number

fdv

number

marketcap

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

     --url 'https://public-api.birdeye.so/defi/token_trending?sort_by=rank&interval=24h&sort_type=asc&offset=0&limit=20&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "updateUnixTime": 1726681733,

    "updateTime": "2024-09-18T17:48:53",

    "tokens": [\
\
      {\
\
        "address": "HJXh1XULVe2Mdp6mTKd5K7of1uFqBTbmcWzvBv6cpump",\
\
        "decimals": 6,\
\
        "liquidity": 34641.80933146691,\
\
        "logoURI": "https://ipfs.io/ipfs/QmR7QnPaYcfwoG8oymK5JRDsB9GSgHr71mJmL2MuJ7Qk3x",\
\
        "name": "AVOCATO",\
\
        "symbol": "ATO",\
\
        "volume24hUSD": 1202872.3148187269,\
\
        "volume24hChangePercent": 33,\
\
        "rank": 1,\
\
        "price": 0.00010551649518689046,\
\
        "price24hChangePercent": 210,\
\
        "fdv": 17028232129,\
\
        "marketcap": 28232129\
\
      },\
\
      {\
\
        "address": "HYFDwieKWth1kzKbtLFMtgMVwukyvyWNYFxyQDcWpump",\
\
        "decimals": 6,\
\
        "liquidity": 73874.80948083404,\
\
        "logoURI": "https://ipfs.io/ipfs/QmUxhHFAugzzWmTMCMCky1QjaJNjtpBNhC2iRELb77Vqfw",\
\
        "name": "The Liquidator",\
\
        "symbol": "LIQUIDATOR",\
\
        "volume24hUSD": 920580.3615402475,\
\
        "volume24hChangePercent": 5,\
\
        "rank": 2,\
\
        "price": 0.0006106216453936813,\
\
        "price24hChangePercent": 12,\
\
        "fdv": 1495237953,\
\
        "marketcap": 5425292\
\
      }\
\
    ],

    "total": 1000

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No

StripeM-Inner
