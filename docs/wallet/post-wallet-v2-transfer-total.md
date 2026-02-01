| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

⚠️ Solana data is available from epoch 257 (11/12/2021)

wallet

string

required

token\_address

string

flow

string

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

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing a total transfer

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

     --url https://public-api.birdeye.so/wallet/v2/transfer/total \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "total": 10

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
