
  - Example: `type=1h` means `count=5` covers five hours.
- `time`: Base timestamp in ISO 8601 UTC format (`YYYY-MM-DD HH:MM:SS`).

  - Example: `2025-07-31 23:59:59`.

**Response fields:**

- `balance`: Raw on-chain balance (before decimal adjustment).
- `price`: Current price per token in USD.
- `value`: Token balance × price (adjusted for decimals).

wallet

required

The wallet of the account.

time

Time get net worth. Default is current time.

type

Defaults to 1d

1h1d

`1h` `1d`

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

**200** ✅ -      JSON object containing list assets of an address at a specific time


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

     --url 'https://public-api.birdeye.so/wallet/v2/net-worth-details?type=1d&sort_type=desc&limit=20&offset=0' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "wallet_address": "HV1KXxWFaSeriyFvXyx48FqG9BoFbfinB8njCJonqP7K",

    "currency": "usd",

    "net_worth": 11839478.53162622,

    "requested_timestamp": "2025-07-31T04:50:06.303258803Z",

    "resolved_timestamp": "2025-07-31T04:50:06.475623209Z",

    "net_assets": [\
\
      {\
\
        "symbol": "Salute",\
\
        "token_address": "49aR46Zgvh3w7cLnM3nZRC4DSVV2A25tYV1fVxYbjtb4",\
\
        "decimal": 4,\
\
        "balance": "50000000000",\
\
        "price": 1.931249899999106,\
\
        "value": 9656249.49999553\
\
      },\
\
      {\
\
        "symbol": "SOL",\
\
        "token_address": "So11111111111111111111111111111111111111112",\
\
        "decimal": 9,\
\
        "balance": "7316581866484",\
\
        "price": 181.4958586895311,\
\
        "value": 1327929.3085297658\
\
      }\
\
    ]

  },

  "pagination": {

    "limit": 100,

    "offset": 0,

    "total": 2

  }

}
` `

