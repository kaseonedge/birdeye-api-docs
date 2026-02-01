| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Lite
- Starter
- Premium
- Business
- Enterprise

address

string

required

The address of the token contract.

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

# `` 200      JSON object containing metadata of a specific token

object

success

boolean

required

data

object

required

address

string

required

symbol

string

required

name

string

required

decimals

integer

required

extensions

object

required

extensions object

logo\_uri

string

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

     --url https://public-api.birdeye.so/defi/v3/token/meta-data/single \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "data": {

    "address": "So11111111111111111111111111111111111111112",

    "symbol": "SOL",

    "name": "Wrapped SOL",

    "decimals": 9,

    "extensions": {

      "coingecko_id": "solana",

      "website": "https://solana.com/",

      "twitter": "https://twitter.com/solana",

      "discord": "https://discordapp.com/invite/pquxPsq",

      "medium": "https://medium.com/solana-labs"

    },

    "logo_uri": "https://img.fotofolio.xyz/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fsolana-labs%2Ftoken-list%2Fmain%2Fassets%2Fmainnet%2FSo11111111111111111111111111111111111111112%2Flogo.png"

  },

  "success": true

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
