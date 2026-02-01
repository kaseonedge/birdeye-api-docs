
- Always use the checksum contract address on supported chains.
- Solana and EVM chains will have different response schemas.
- Separate token addresses in string by commas (,)
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

Specify the liquidity value to check.

include\_liquidity

Specify whether to include liquidity in the response.

truefalse

`true` `false`

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

list\_address

required

Defaults to So11111111111111111111111111111111111111112,DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      JSON object containing price values and update time of multiple tokens

success

required

data

required

A hashmap with token addresses as keys and the price object as value

View Additional Properties

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request POST \

     --url 'https://public-api.birdeye.so/defi/multi_price?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana' \

     --data '

{

  "list_address": "So11111111111111111111111111111111111111112,DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263"

}

'
` `

` `



{

  "success": true,

  "data": {

    "So11111111111111111111111111111111111111112": {

      "isScaledUiToken": false,

      "value": 127.32916175338693,

      "updateUnixTime": 1726673192,

      "updateHumanTime": "2024-09-18T15:26:32",

      "priceInNative": 1,

      "priceChange24h": -5.833510393308625,

      "liquidity": 7026264396

    },

    "DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263": {

      "isScaledUiToken": false,

      "value": 0.00001598090539282,

      "updateUnixTime": 1726673185,

      "updateHumanTime": "2024-09-18T15:26:25",

      "priceInNative": 1.2583e-7,

      "priceChange24h": -4.766925300538944,

      "liquidity": 1234414

    }

  }

}
` `

