
- Response may be `null` or missing data if the token is unknown or unsupported.
- Cache or throttle requests to avoid hitting rate limits.

address

required

The address of the token contract.

x-chain

Defaults to base

Base network only.

base

`base`


## Responses

**200** ✅ - OK


success

required

data

required

token

required

exit\_liquidity

required

liquidity

required

price

required

price object

currency

required

address

required

name

required

symbol

required

decimals

required

extensions

required

logo\_uri

required

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/defi/v3/token/exit-liquidity \

     --header 'accept: application/json' \

     --header 'x-chain: base'
` `

` `



{

  "data": {

    "token": "0x60a3E35Cc302bFA44Cb288Bc5a4F316Fdb1adb42",

    "exit_liquidity": 6787432.938612048,

    "liquidity": 10355070.125772206,

    "price": {

      "value": 1.1515311597782227,

      "update_unix_time": 1750385475,

      "update_human_time": "2025-06-20T02:11:15",

      "update_in_slot": 31798064

    },

    "currency": "USD",

    "address": "0x60a3E35Cc302bFA44Cb288Bc5a4F316Fdb1adb42",

    "name": "EURC",

    "symbol": "EURC",

    "decimals": 6,

    "extensions": {

      "twitter": "https://twitter.com/circlepay",

      "website": "https://www.circle.com",

      "telegram": null

    },

    "logo_uri": "https://coin-images.coingecko.com/coins/images/26045/small/euro.png?1696525125"

  },

  "success": true

}
` `

StripeM-Inner
