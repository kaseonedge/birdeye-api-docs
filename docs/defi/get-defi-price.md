
- Solana and EVM chains will have different response schemas.
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

Specify the liquidity value to check.

include\_liquidity

Specify whether to include liquidity in the response.

truefalse

`true` `false`

address

required

The address of the token contract.

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      JSON object containing price value and update time of a token

success

required

data

required

value

required

updateUnixTime

integer

required

updateHumanTime

required

priceChange24h

required

priceInNative

liquidity

isScaledUiToken

scaledValue

multiplier

scaledPriceInNative

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/price?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "isScaledUiToken": false,

    "value": 0.38622452197470425,

    "updateUnixTime": 1745058945,

    "updateHumanTime": "2025-04-19T10:35:45",

    "priceChange24h": 1.933391934259418,

    "priceInNative": 0.0027761598581298626,

    "liquidity": 10854103.37938592

  },

  "success": true

}
` `

