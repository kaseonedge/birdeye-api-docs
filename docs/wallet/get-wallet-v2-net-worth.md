
  - Example: `count`=5 with `type`=1d returns five days of data (either backward or forward).
- `type`: Defines the time unit for `count`. Accepts: 1h (hourly) or 1d (daily).

  - Example: `type=1h` means `count=5` covers five hours.
- `direction`: Determines how `count` is applied:

  - `back`: Retrieves the last N intervals before time.
  - `forward`: Retrieves the next N intervals starting from time.

    - Example: If `direction=back`, `count=3`, `type=1d`, and `time=2025-07-31 23:59:59`, you'll get daily net worth for: July 28 → July 29 → July 30.
- `time`: Base timestamp in ISO 8601 UTC format (`YYYY-MM-DD HH:MM:SS`).

wallet

required

The wallet of the account.

count

integer

1 to 30

Defaults to 7

direction

Defaults to back

backforward

`back` `forward`

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

x-chain

Defaults to solana

Solana network only.

solana

`solana`

# 200      JSON object containing net worth of an address

success

required

data

required

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/wallet/v2/net-worth?count=7&direction=back&type=1d&sort_type=desc' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "wallet_address": "HV1KXxWFaSeriyFvXyx48FqG9BoFbfinB8njCJonqP7K",

    "currency": "usd",

    "current_timestamp": "2025-07-31T23:59:59Z",

    "past_timestamp": "2025-07-01T23:59:59Z",

    "history": [\
\
      {\
\
        "timestamp": "2025-07-30T23:59:59Z",\
\
        "net_worth": 13210463.21,\
\
        "net_worth_change": 1971274.94,\
\
        "net_worth_change_percent": 17.54\
\
      },\
\
      {\
\
        "timestamp": "2025-07-29T23:59:59Z",\
\
        "net_worth": 11839478.54,\
\
        "net_worth_change": 600290.26,\
\
        "net_worth_change_percent": 5.35\
\
      }\
\
    ]

  }

}
` `

