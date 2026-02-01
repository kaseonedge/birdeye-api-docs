
- We use cursor for pagination. On the first request, pass the necessary filters except `cursor`. It will return a field called `next_cursor` for pagination. On the next request, pass this `next_cursor` value into the param `cursor`.
- When passing `cursor` param with other params, only `cursor` is in effect.

token\_address

string

required

time\_from

number

time\_to

number

from\_amount

number

to\_amount

number

from\_value

number

to\_value

number

from\_wallet

string

to\_wallet

string

cursor

string

limit

number

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing list transfer

object

success

boolean

required

data

object

required

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request POST \

     --url https://public-api.birdeye.so/token/v1/transfer \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

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
```

* * *

