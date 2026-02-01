
- Starter
- Premium
- Business
- Enterprise

wallet

required

The wallet of the account.

filter\_value

A parameter used to filter assets, returning only those whose value is greater than or equal to the specified filter\_value.

sort\_by

Defaults to value

Specify the sort field.

value

`value`

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

limit

integer

1 to 100

Defaults to 20

offset

integer

0 to 10000

Defaults to 0

Make sure offset <= 10000

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200** ✅ -      JSON object containing portfolio of an address


success

required

data

required

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/wallet/v2/current-net-worth?sort_by=value&sort_type=desc&limit=20&offset=0' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "wallet_address": "8X35rQUK2u9hfn8rMPwwr6ZSEUhbmfDPEapp589XyoM1",

    "currency": "usd",

    "total_value": "0.010349446772590722",

    "current_timestamp": "2025-05-19T04:47:19.414327725Z",

    "items": [\
\
      {\
\
        "address": "cCpv5Z3nqKbKohYqgY7rxFebjMjvU7SBhwgYbCipump",\
\
        "decimals": 6,\
\
        "price": 0.00014999198221145974,\
\
        "balance": "69000000",\
\
        "amount": 69,\
\
        "network": "solana",\
\
        "name": "Smellow",\
\
        "symbol": "SMLO",\
\
        "logo_uri": "https://pump.mypinata.cloud/ipfs/QmcCjKS4MMeji11PqnNhqDSXd6gD4iGj1nC6zjyfaekuQZ",\
\
        "value": "0.010349446772590722"\
\
      }\
\
    ]

  },

  "pagination": {

    "limit": 100,

    "offset": 0,

    "total": 1

  }

}
` `

