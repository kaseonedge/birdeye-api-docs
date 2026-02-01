
- Starter
- Premium
- Business
- Enterprise

address

required

The address of the token contract.

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200**✅ - JSON object containing metadata of a specific token


success

required

data

required

address

required

symbol

required

name

required

decimals

integer

required

extensions

required

extensions object

logo\_uri

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/defi/v3/token/meta-data/single \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



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
` `

