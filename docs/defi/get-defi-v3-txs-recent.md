| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Returns latest V3 DEX transactions (swaps) for a given chain.
- Only includes transactions from the **last 24 hours** or the **most recent ~50,000 blocks**, whichever is shorter.
- Does not support custom time or block range filtering.
- Parameters:
  - `chain`: required (e.g. `solana`, `bsc`, `eth`)
  - `dex`: optional (filter by specific DEX)
  - `page`, `limit`: for pagination
- Results are ordered by descending `block_time`.
- Each item includes trade details: `tx_hash`, `block_time`, tokens, amounts, and `price_usd`.

Ideas 💡

- Track the latest DEX trades for a specific token across all supported DEXes.
- Ideal for analyzing token activity, trading momentum, or unusual volume spikes.
- Supports pagination for building continuous trade history views.
- Great for use in token detail pages, bots, and DeFi monitoring tools.

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

tx\_type

string

enum

Defaults to swap

swapaddremoveall

Allowed:

`swap``add``remove``all`

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

     --url 'https://public-api.birdeye.so/defi/v3/txs/recent?offset=0&limit=100&tx_type=swap&ui_amount_mode=scaled' \

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
