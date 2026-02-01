| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Retrieving recent requests… |

LoadingLoading…

#### URL Expired

The URL for this request expired after 30 days.

- Solana notes:
  - Transaction data includes `signers` — a list of accounts that authorize the transaction with their signatures.
- If time range and block number range are not provided:
  - If sort\_by = block\_unix\_time, default to fetching swaps within the last 7 days.
  - If sort\_by = block\_number, default to fetching swaps within the last 500,000 blocks.
- Only one type of filter is accepted: either block time range or block number range.
- If filtering by block time (after\_time, before\_time), only allow sorting by block\_unix\_time.
- If filtering by block number (after\_block\_number, before\_block\_number), only allow sorting by block\_number.
- Constraints:
  - Block time range: cannot exceed 30 days.
  - Block number range: cannot exceed 500,000 blocks.
  - If only after\_time is provided (no before\_time), it must be within the last 30 days.
  - If only after\_block\_number is provided (no before\_block\_number), it must be within the most recent 500,000 blocks.

Ideas 💡

- Track the latest DEX trades for a specific token across all supported DEXes.
- Ideal for analyzing token activity, trading momentum, or unusual volume spikes.
- Supports pagination for building continuous trade history views.
- Great for use in token detail pages, bots, and DeFi monitoring tools.

address

string

required

The address of the token contract.

offset

integer

0 to 9999

Defaults to 0

Make sure offset + limit <= 10000

limit

integer

1 to 100

Defaults to 100

Number of items per page.

sort\_by

string

enum

Defaults to block\_unix\_time

block\_unix\_timeblock\_number

Allowed:

`block_unix_time``block_number`

sort\_type

string

enum

Defaults to desc

Specify the sort order.

desc

Allowed:

`desc`

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

pool\_id

string

The address of the liquidity pool.

before\_time

integer

1 to 10000000000

Specify the time seeked before using unix timestamps in seconds

after\_time

integer

1 to 10000000000

Specify the time seeked after using unix timestamps in seconds

before\_block\_number

integer

1 to 9007199254740991

Specify the upper bound of block\_number for the filter range, excluding values equal to before\_block\_number.

after\_block\_number

integer

1 to 9007199254740991

Specify the lower bound of block\_number for the filter range, excluding values equal to after\_block\_number.

ui\_amount\_mode

string

enum

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

Allowed:

`raw``scaled`

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

Show 15 enum values

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

Updated 24 days ago

* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/txs?offset=0&limit=100&sort_by=block_unix_time&sort_type=desc&tx_type=swap&ui_amount_mode=scaled' \

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

Updated 24 days ago

* * *

Did this page help you?

Yes

No
