| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

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

- Get recent DEX trades across all tokens and pairs on a specific chain.
- Useful for building real-time trade feeds or monitoring on-chain activity.
- Filter by DEX or chain to spot volume spikes or new trading patterns.
- Ideal for dashboards, bots, or alert systems watching market flow.

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

swapaddremoveall

Allowed:

`swap``add``remove``all`

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

# `` 200      JSON object containing trades

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

     --url 'https://public-api.birdeye.so/defi/v3/txs?offset=0&limit=100&sort_by=block_unix_time&sort_type=desc&tx_type=swap&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "items": [\
\
      {\
\
        "base": {\
\
          "symbol": "CLIPPY",\
\
          "address": "GCLTmivKZfxYi8SV17FrpqH8HZtJauoePQPRHxJxBAGS",\
\
          "decimals": 9,\
\
          "price": 0.00026036603447282113,\
\
          "amount": "24285885836773",\
\
          "ui_amount": 24285.885836773,\
\
          "ui_change_amount": 24285.885836773,\
\
          "type_swap": "to",\
\
          "is_scaled_ui_token": false,\
\
          "multiplier": null\
\
        },\
\
        "quote": {\
\
          "symbol": "SOL",\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "decimals": 9,\
\
          "price": 185.6186502639611,\
\
          "amount": "34118151",\
\
          "ui_amount": 0.034118151,\
\
          "ui_change_amount": -0.034118151,\
\
          "type_swap": "from",\
\
          "is_scaled_ui_token": false,\
\
          "multiplier": null\
\
        },\
\
        "tx_type": "swap",\
\
        "tx_hash": "4z62PXFvbo52qY66XAMhsaKSfNH9MoBinFQtsjoZcjRTc2gCGP2o86yTUdaHpnYozHxNkiATX3KRGPfFb7CyjoPW",\
\
        "ins_index": 0,\
\
        "inner_ins_index": 3,\
\
        "block_unix_time": 1754885184,\
\
        "block_number": 359262879,\
\
        "volume_usd": 6.332965138122014,\
\
        "volume": 24285.885836773,\
\
        "owner": "7dGrdJRYtsNR8UYxZ3TnifXGjGc9eRYLq9sELwYpuuUu",\
\
        "signers": [\
\
          "7dGrdJRYtsNR8UYxZ3TnifXGjGc9eRYLq9sELwYpuuUu"\
\
        ],\
\
        "source": "meteora_dlmm",\
\
        "interacted_program_id": "King7ki4SKMBPb3iupnQwTyjsq294jaXsgLmJo8cb7T",\
\
        "pool_id": "6LR2pDMBbYZNhj1iF86b4X5zRYyX7BNrhpzRDEZYNam9"\
\
      }\
\
    ],

    "hasNext": true

  }

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
