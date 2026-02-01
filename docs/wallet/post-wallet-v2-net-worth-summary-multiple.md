
wallets

array of strings

required

wallets\*
ADD string

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200** ✅ - JSON object containing summary networth


success

required

data

required

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request POST \

     --url https://public-api.birdeye.so/wallet/v2/net-worth-summary/multiple \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "currency": "usd",

    "current_timestamp": "2025-10-30T03:33:40.980036224Z",

    "wallets": {

      "5Q544fKrFoe6tsEbD7S8EmxGTJYAKtTVhAW5Q5pge4j1": {

        "value": "1764819473.530063"

      },

      "WLHv2UAZm6z4KyaaELi5pjdbJh6RESMva1Rnn8pJVVh": {

        "value": "3508619230.707581"

      }

    }

  },

  "success": true

}
` `

