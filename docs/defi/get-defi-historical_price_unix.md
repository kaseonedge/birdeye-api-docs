
- Starter
- Premium
- Business
- Enterprise

required

The address of the token contract.

unixtime

integer

0 to 10000000000

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

x-chain

Defaults to solana

Solana network only.

solana

`solana`

# 200      JSON object containing list of a token's transactions

json

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/historical_price_unix?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "isScaledUiToken": false,

    "value": 128.09276765626564,

    "updateUnixTime": 1726675897,

    "priceChange24h": -4.924324221890145

  }

}
` `

