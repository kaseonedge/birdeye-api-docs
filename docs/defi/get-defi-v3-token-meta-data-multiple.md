
- Business
- Enterprise

list\_address

required

A list of token addresses in string separated by commas (,)

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200**✅ - JSON object containing metadata of multiple tokens


success

required

data

required

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/defi/v3/token/meta-data/multiple \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "So11111111111111111111111111111111111111112": {

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

    "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v": {

      "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",

      "decimals": 6,

      "symbol": "USDC",

      "name": "USD Coin",

      "extensions": {

        "coingecko_id": "usd-coin",

        "website": "https://www.circle.com/en/usdc",

        "twitter": "https://twitter.com/circle",

        "medium": "https://medium.com/centre-blog",

        "discord": "https://discord.com/invite/buildoncircle"

      },

      "logo_uri": "https://img.fotofolio.xyz/?url=https%3A%2F%2Fraw.githubusercontent.com%2Fsolana-labs%2Ftoken-list%2Fmain%2Fassets%2Fmainnet%2FEPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v%2Flogo.png"

    }

  },

  "success": true

}
` `

