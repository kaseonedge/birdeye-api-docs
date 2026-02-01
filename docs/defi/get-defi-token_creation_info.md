
- Premium
- Business
- Enterprise

address

required

The address of the token contract.

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200** ✅ -      JSON object containing creation information of a token


success

required

data

required

txHash

slot

integer

tokenAddress

decimals

integer

owner

blockUnixTime

integer

blockHumanTime

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/defi/token_creation_info \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "txHash": "3cW2HpkUs5Hg2FBMa52iJoSMUf8MNkkzkRcGuBs1JEesQ1pnsvNwCbTmZfeJf8hTi9NSHh1Tqx6Rz5Wrr7ePDEps",

    "slot": 223012712,

    "tokenAddress": "D7rcV8SPxbv94s3kJETkrfMrWqHFs6qrmtbiu6saaany",

    "decimals": 5,

    "owner": "JEFL3KwPQeughdrQAjLo9o75qh15nYbFJ2ZDrb695qsZ",

    "blockUnixTime": 1697044029,

    "blockHumanTime": "2023-10-11T17:07:09.000Z"

  }

}
` `

