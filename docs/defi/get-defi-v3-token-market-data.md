
- Lite
- Starter
- Premium
- Business
- Enterprise

address

required

The address of the token contract.

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      JSON object containing market data of a specific token

success

required

data

required

address

required

price

required

liquidity

required

total\_supply

required

circulating\_supply

required

market\_cap

required

fdv

required

holder

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/market-data?ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "address": "So11111111111111111111111111111111111111112",

    "price": 185.74132384799458,

    "liquidity": 23338480211.61425,

    "total_supply": 607187823.0928401,

    "circulating_supply": 539542621.8877238,

    "fdv": 112779870085.64606,

    "market_cap": 100215360861.8438,

    "holder": 3498897,

    "is_scaled_ui_token": false,

    "multiplier": null

  }

}
` `

