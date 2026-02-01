
wallet

required

token\_addresses

array of strings

token\_addresses
ADD string

sort\_type

Defaults to desc

ascdesc

`asc` `desc`

sort\_by

Defaults to value

valuelast\_trade

`value` `last_trade`

limit

integer

1 to 100

Defaults to 10

offset

integer

0 to 10000

Defaults to 0

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200** ✅ - JSON object containing a wallet


success

required

data

required

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request POST \

     --url https://public-api.birdeye.so/wallet/v2/pnl/details \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana' \

     --data '

{

  "sort_type": "desc",

  "sort_by": "value",

  "limit": 10,

  "offset": 0

}

'
` `

` `



{

  "data": {

    "meta": {

      "address": "123hJZ8FGVhesDUrv5dCgorewd7KMqBkFhoGdyZNp62D",

      "currency": "usd",

      "holding_check": false,

      "time": "2025-10-31T08:38:25.295882105Z"

    },

    "tokens": [\
\
      {\
\
        "symbol": "G7",\
\
        "decimals": 6,\
\
        "address": "2VKDTnMF9hmDfCG4i7yPHsfYzYCRhLwQcgUQPxvvYKnV",\
\
        "counts": {\
\
          "total_buy": 1,\
\
          "total_sell": 1,\
\
          "total_trade": 2\
\
        },\
\
        "quantity": {\
\
          "total_bought_amount": 6152601.258849,\
\
          "total_sold_amount": 6152601.258849,\
\
          "holding": 0\
\
        },\
\
        "cashflow_usd": {\
\
          "cost_of_quantity_sold": 9.7233729560565,\
\
          "total_invested": 9.7233729560565,\
\
          "total_sold": 9.85555342050984,\
\
          "current_value": 0\
\
        },\
\
        "pnl": {\
\
          "realized_profit_usd": 0.13218046445334128,\
\
          "realized_profit_percent": 1.3594095901773329,\
\
          "unrealized_usd": 0,\
\
          "unrealized_percent": 0,\
\
          "total_usd": 0.13218046445334128,\
\
          "total_percent": 1.3594095901773329,\
\
          "avg_profit_per_trade_usd": 0.13218046445334128\
\
        },\
\
        "pricing": {\
\
          "current_price": null,\
\
          "avg_buy_cost": 0.0000015803678065552884,\
\
          "avg_sell_cost": 0.0000016018514780776761\
\
        }\
\
      }\
\
    ],

    "summary": {

      "unique_tokens": 7,

      "counts": {

        "total_buy": 19,

        "total_sell": 19,

        "total_trade": 38,

        "total_win": 4,

        "total_loss": 1,

        "win_rate": 0.5714285714285714

      },

      "cashflow_usd": {

        "total_invested": 424.183016567611,

        "total_sold": 555.080692928933,

        "current_value": 392.84271337031083

      },

      "pnl": {

        "realized_profit_usd": 130.8976763613221,

        "realized_profit_percent": 30.858773512554855,

        "unrealized_usd": 0,

        "total_usd": 130.8976763613221,

        "avg_profit_per_trade_usd": 3.444675693719003

      }

    }

  }

}
` `

