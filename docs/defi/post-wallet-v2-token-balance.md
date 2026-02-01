
- `data[<index>]`:

  - `address`: Token mint address on Solana.
  - `decimals`: Number of decimal places used by the token.
  - `price`: Current token price in USD.
  - `balance`: Raw balance in base units (string).
  - `amount`: Human-readable balance (normalized using `10^-decimals`).
  - `network`: Blockchain network (e.g., `solana`).
  - `name`: Token name (e.g., BIGIFTRUE).
  - `symbol`: Token ticker.
  - `value`: USD value of the wallet’s holdings (`amount * price`).

wallet

string

token\_addresses

array of strings

token\_addresses
ADD string

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

     --url https://public-api.birdeye.so/wallet/v2/token-balance \

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
      "address": "8i42ZVsjEGVhZ6spj4Z5aB36Msh9Vq4nnBaw5kq4pump",\
\
      "decimals": 9,\
\
      "price": 0.0020303701828560256,\
\
      "balance": "4998929789571623824",\
\
      "amount": 4998929789.571624,\
\
      "network": "solana",\
\
      "name": "BIGIFTRUE",\
\
      "symbol": "BIGIFTRUE",\
\
      "logo_uri": "https://ipfs.io/ipfs/bafkreihgbhs4sumfhvdcquud7mvggjjbidfuoisytxqnpafrx6ukrh4hlm",\
\
      "value": "10149677.99093697"\
\
    }\
\
  ]

}
```

* * *

