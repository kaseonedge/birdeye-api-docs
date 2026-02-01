
- Starter
- Premium
- Business
- Enterprise

Ideas 💡

- Returns historical USD prices for a token at **multiple timestamps** in one request.
- Perfect for portfolio time series reconstruction or backtesting strategies.
- Great for generating custom charts, price annotations, and historical comparisons.
- Efficient alternative to multiple single `/history_price` calls — ideal for bulk queries.

address

string

required

The address of the token contract.

unixtime

integer

0 to 10000000000

ui\_amount\_mode

string

enum

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

Allowed:

`raw``scaled``both`

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing list of a token's transactions

json

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/historical_price_unix?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "isScaledUiToken": false,

    "value": 128.09276765626564,

    "updateUnixTime": 1726675897,

    "priceChange24h": -4.924324221890145

  }

}
```

* * *

