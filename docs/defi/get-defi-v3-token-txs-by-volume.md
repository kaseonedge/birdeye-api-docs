
- Maximum limit of 500.
- Do not support filtering by `pool_id`, `before_block_number` or `after_block_number`.
- Additional parameters:
  - `volume_type`: can be either usd or amount of token.
- `min_volume` and `max_volume` for volume-based filtering.
- Expands data sources to include meteora\_dlmm and others.

token\_address

string

required

The address of the token contract.

volume\_type

string

enum

required

Volume type value to be filtered

usdamount

Allowed:

`usd``amount`

min\_volume

number

Minimum volume value, support up to 3 decimals

max\_volume

number

Maximum volume value, support up to 3 decimals

sort\_by

string

enum

Defaults to block\_unix\_time

block\_unix\_timeblock\_number

Allowed:

`block_unix_time``block_number`

tx\_type

string

enum

Defaults to swap

swapbuyselladdremoveall

Allowed:

`swap``buy``sell``add``remove``all`

source

string

enum

Source of the liquidity (AMMs). Only support solana.

raydiumraydiumraydium\_clammraydium\_cporcalifinityfluxbeamsaberphoenixbonkswappump\_dot\_funmeteora\_dlmm

Show 11 enum values

owner

string

The address of the wallet.

before\_time

integer

1 to 10000000000

Specify the time seeked before using unix timestamps in seconds

after\_time

integer

1 to 10000000000

Specify the time seeked after using unix timestamps in seconds

ui\_amount\_mode

string

enum

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

Allowed:

`raw``scaled`

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

offset

integer

0 to 9999

Defaults to 0

Make sure offset + limit <= 10000

limit

integer

1 to 500

Defaults to 100

Number of items per page.

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing transactions of a token

object

success

boolean

required

data

object

required

items

array of objects

required

items\*

object

View Additional Properties

hasNext

boolean

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

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/txs-by-volume?volume_type=usd&sort_by=block_unix_time&tx_type=swap&ui_amount_mode=scaled&sort_type=desc&offset=0&limit=100' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "data": {

    "items": [\
\
      {\
\
        "tx_type": "buy",\
\
        "tx_hash": "3fqsirN8vbhBLHS2cVAaCXTdsCcCua75LgcBX6Z2G2yupM9cDEsmo2TP5AhXvEUBZ91xyy3KWiuDdHxoFVnp1R88",\
\
        "ins_index": 2,\
\
        "inner_ins_index": 0,\
\
        "block_unix_time": 1740380278,\
\
        "block_number": 322728531,\
\
        "volume_usd": 0.0005729458359923133,\
\
        "volume": 1733.23946,\
\
        "owner": "8bP4FJNXwN5Q4a6EybtHwsiAnxFFWb93sY38mYdo6Pr2",\
\
        "signers": [\
\
          "8bP4FJNXwN5Q4a6EybtHwsiAnxFFWb93sY38mYdo6Pr2"\
\
        ],\
\
        "source": "raydium",\
\
        "side": "buy",\
\
        "alias": null,\
\
        "price_pair": 486318591.4702581,\
\
        "from": {\
\
          "symbol": "PEPEAI",\
\
          "address": "7nM97F8takLArrKLJdT62L54jTtX1e7h7qPSjtBrsMQA",\
\
          "decimals": 6,\
\
          "price": 3.5071289483955604e-7,\
\
          "amount": "1733239460",\
\
          "ui_amount": 1733.23946,\
\
          "ui_change_amount": -1733.23946\
\
        },\
\
        "to": {\
\
          "symbol": "SOL",\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "decimals": 9,\
\
          "price": 160.7592132413898,\
\
          "amount": "3564",\
\
          "ui_amount": 0.000003564,\
\
          "ui_change_amount": 0.000003564\
\
        },\
\
        "pool_id": "8aTXVUjPcUSwSLAbUegaKTQdB6SaNosSKQkURvpbLCNC"\
\
      }\
\
    ],

    "has_next": true

  },

  "success": true

}
```

* * *

