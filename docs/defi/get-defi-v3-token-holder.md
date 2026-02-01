
- Lite
- Starter
- Premium
- Business
- Enterprise

address

required

The address of the token contract.

offset

integer

0 to 10000

Defaults to 0

Pagination start position. offset + limit <= 10000

limit

integer

1 to 100

Defaults to 100

Number of items per page.

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200** ✅ - JSON object containing a list of token holder


success

required

data

required

items

array of objects

items

amount

decimals

integer

mint

owner

token\_account

ui\_amount

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/holder?offset=0&limit=100&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "items": [\
\
      {\
\
        "amount": "4995300410087424",\
\
        "decimals": 9,\
\
        "mint": "So11111111111111111111111111111111111111112",\
\
        "owner": "AVzP2GeRmqGphJsMxWoqjpUifPpCret7LqWhD8NWQK49",\
\
        "token_account": "BUvduFTd2sWFagCunBPLupG8fBTJqweLw9DuhruNFSCm",\
\
        "ui_amount": 4995300.410087424,\
\
        "is_scaled_ui_token": false,\
\
        "multiplier": null\
\
      }\
\
    ]

  }

}
` `

