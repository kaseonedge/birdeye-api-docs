| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |


##

The URL for this request expired after 30 days.

token\_address

string

required

Token contract address.

address\_type

string

enum

Defaults to wallet

Return holder distribution by wallet or token account address.

wallettoken\_account

Allowed:

`wallet``token_account`

mode

string

enum

Defaults to top

Holder filter mode (percent = by supply % range, top = top holders by supply %).

percenttop

Allowed:

`percent``top`

top\_n

integer

1 to 10000

Defaults to 10

Number of top holders to return (used only when mode = top).

min\_percent

number

0 to 100

Minimum % of total supply a holder must have (used only when mode = percent).

max\_percent

number

0 to 100

Maximum % of total supply a holder can have (used only when mode = percent).

include\_list

boolean

Defaults to true

Return holder list (true / false).

truefalse

offset

integer

0 to 10000

Defaults to 0

Pagination start position. offset + limit <= 10000

limit

integer

1 to 50

Defaults to 50

Number of items per page.

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing token holder distribution details

object

success

boolean

required

data

object

required

token\_address

string

required

mode

string

enum

required

`percent`

range

object

required

range object

pagination

object

required

pagination object

summary

object

required

summary object

holders

array of objects

required

holders\*

object

wallet

string

holding

string

percent\_of\_supply

number

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error



* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/holder/v1/distribution?address_type=wallet&mode=top&top_n=10&include_list=true&offset=0&limit=50' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": {

    "token_address": "11111Zxp8hv4GVzZTWcgcFTcFCfPzW8YmbwvGahTBP",

    "mode": "percent",

    "range": {

      "min_percent": 0,

      "max_percent": 1

    },

    "pagination": {

      "limit": 50,

      "offset": 0,

      "total": 2

    },

    "summary": {

      "wallet_count": 2,

      "total_holding": "0.007374018405092705",

      "percent_of_supply": 0.0000017374018405092703

    },

    "holders": [\
\
      {\
\
        "wallet": "aXG7W1eYYHN3SyAp515Dqu595wzNJxdGtcG5sjLVky1",\
\
        "holding": "0.000017910381239401126",\
\
        "percent_of_supply": 0.0000017910381239401128\
\
      },\
\
      {\
\
        "wallet": "aXG7W1wjjgiNnu8emgqJsTqbN86B8KEeKhN4J4JChqd",\
\
        "holding": "0.0000007910381239401126",\
\
        "percent_of_supply": 0.0000017910381239401128\
\
      }\
\
    ]

  }

}
```



* * *

Did this page help you?

Yes

No
