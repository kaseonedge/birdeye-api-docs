
- Starter
- Premium
- Business
- Enterprise

address

string

required

The address of the token contract.

sort\_by

string

enum

required

Defaults to block\_time

Specify the sort order for mint/burn transactions. Filter for records with sort order equal to the specified sort order.

block\_time

Allowed:

`block_time`

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

type

string

enum

required

Defaults to all

Specify the type of mint/burn transactions. Filter for records with type equal to the specified type.

allmintburn

Allowed:

`all``mint``burn`

after\_time

integer

Specify the lower bound of time. Filter for records with time greater than the specified after time value, excluding those with time equal to the specified after time.

before\_time

integer

Specify the upper bound of time. Filter for records with time less than the specified before time value, excluding those with time equal to the specified before time.

offset

integer

0 to 10000

Defaults to 0

Pagination start position. offset + limit <= 10000

limit

integer

1 to 100

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

# `` 200      JSON object containing a list of mint/burn transactions

object

success

boolean

required

data

object

required

items

array of objects

items

object

amount

string

block\_human\_time

string

block\_time

number

common\_type

string

decimals

number

mint

string

program\_id

string

slot

number

tx\_hash

string

ui\_amount

number

ui\_amount\_string

string

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

     --url 'https://public-api.birdeye.so/defi/v3/token/mint-burn-txs?sort_by=block_time&sort_type=desc&type=all&offset=0&limit=100' \

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
        "amount": "870",\
\
        "block_human_time": "2024-11-08T07:28:18.000Z",\
\
        "block_time": 1731050898,\
\
        "common_type": "burn",\
\
        "decimals": 0,\
\
        "mint": "fueL3hBZjLLLJHiFH9cqZoozTG3XQZ53diwFPwbzNim",\
\
        "program_id": "TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA",\
\
        "slot": 300145960,\
\
        "tx_hash": "TyqmrBiZaW6bXsm6fV1owkVL2ea3PF2rbHPNZQtQrLYiZVThHEmkcD4QHKw37W43nyUdrFSdNr2xxTPZkPBY3pZ",\
\
        "ui_amount": 870,\
\
        "ui_amount_string": "870"\
\
      }\
\
    ]

  }

}
```

* * *

