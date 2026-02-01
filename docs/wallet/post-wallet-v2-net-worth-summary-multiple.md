| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Maximum number of wallets per request: 100

wallets

array of strings

required

wallets\*
ADD string

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing summary networth

object

success

boolean

required

data

object

required

Has additional fields

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

Updated 24 days ago

* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request POST \

     --url https://public-api.birdeye.so/wallet/v2/net-worth-summary/multiple \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



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
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
