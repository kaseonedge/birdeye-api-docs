
- `token_address`: optional. Can be used to obtain first tx funded of that specific token. Default to first tx if not passed.

wallets

array of strings

required

wallets\*
ADD string

token\_address

string

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing a wallet token balance

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

     --url https://public-api.birdeye.so/wallet/v2/tx/first-funded \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "1jw5fDodwGEGBVqNXsx2eqiLgNmgMDEeXWSbrTreLCM": {

      "tx_hash": "8g5kPkNNhbxozv7veVjwHqCdJ6FB4B3zMaXBfHigZKwPprNB3A3WcVBCdEm1rfuG1m3syHEVZHeYfCZfM7BgQ6s",

      "block_unix_time": 1717292678,

      "block_number": 269344897,

      "balance_change": "7182720",

      "token_address": "So11111111111111111111111111111111111111111",

      "token_decimals": 9

    }

  }

}
```

* * *

