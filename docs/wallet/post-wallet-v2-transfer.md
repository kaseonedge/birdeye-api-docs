
- When passing `cursor` param with other params, only `cursor` is in effect.
- Support 4 transfer types: mint, burn, transfer and set\_authority

wallet

required

token\_address

flow

time\_from

time\_to

from\_amount

to\_amount

from\_value

to\_value

from\_wallet

to\_wallet

cursor

limit

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200**✅ - JSON object containing list transfer


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

     --url https://public-api.birdeye.so/wallet/v2/transfer \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": [\
\
    {\
\
      "time": "2025-11-18T04:32:26Z",\
\
      "block_number": 380819945,\
\
      "unix_time": 1763440346,\
\
      "token_address": "9TR9Ge75PMHfoKBAzo88XpDhvhjsirETEuPtRS4VtrpJ",\
\
      "from_address": "HLnpSz9h2S4hiLQ43rnSD9XkcUThA7B8hQMKmDaiTLcC",\
\
      "to_address": "FCgMrWxuY5mWgFn55czYLysfGi3QFsZm3W7sJ7wTDQpz",\
\
      "from_token_account": "5JAZp6t5eSNXbdEwu3pMbB8uKV1e9cf2yg8E4Yq56WZa",\
\
      "to_token_account": "FKtWCwxFKdc7g7ymxVgyBSbwzGMNGWe7HtbKkum99f9C",\
\
      "amount": "14213245095",\
\
      "ui_amount": 14213.245095,\
\
      "price": 0.000029247096468293907,\
\
      "value": 0.4156961504209702,\
\
      "tx_hash": "2vLYZuCrKARicrXRDf2eGnzaKR9PP6qFFuzgPCHUNAnwepcqvFQ8WiPRuZjBNihNsNoxxQ5bLVLX7Wu6i6h5tmuP",\
\
      "flow": "out",\
\
      "token_info": {\
\
        "address": "9TR9Ge75PMHfoKBAzo88XpDhvhjsirETEuPtRS4VtrpJ",\
\
        "decimals": 6,\
\
        "symbol": "NYAN",\
\
        "name": "Nyan Cat",\
\
        "logo_uri": "https://wsrv.nl/?w=128&h=128&default=1&url=https://rs.debot.ai/logo/CMx7yon2cLzHcXqgHsKJhuU3MmME6noWLQk2rAycBAGS.gif"\
\
      },\
\
      "action": "transfer"\
\
    }\
\
  ]

}
` `

