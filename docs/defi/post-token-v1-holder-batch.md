
- Business
- Enterprise

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

wallets

array of strings

required

wallets\*
ADD string

token\_address

required

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200**✅ - JSON object containing held of list owner


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



curl --request POST \

     --url 'https://public-api.birdeye.so/token/v1/holder/batch?ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "items": [\
\
      {\
\
        "balance": "2039280",\
\
        "decimals": 9,\
\
        "mint": "So11111111111111111111111111111111111111112",\
\
        "owner": "2fgUSSpZFi8PjyhbrETSeLutJpFsuCfWsk2H6gb3Reye",\
\
        "amount": 0.00203928\
\
      },\
\
      {\
\
        "balance": "1563400084419",\
\
        "decimals": 9,\
\
        "mint": "So11111111111111111111111111111111111111112",\
\
        "owner": "CZY9M9BywshFAFjPw7uLgXw9yGtNL26YypLCJdewiHo",\
\
        "amount": 1563.400084419\
\
      },\
\
      {\
\
        "balance": "4961135742857367",\
\
        "decimals": 9,\
\
        "mint": "So11111111111111111111111111111111111111112",\
\
        "owner": "5Q544fKrFoe6tsEbD7S8EmxGTJYAKtTVhAW5Q5pge4j1",\
\
        "amount": 4961135.742857367\
\
      }\
\
    ]

  },

  "success": true

}
` `

