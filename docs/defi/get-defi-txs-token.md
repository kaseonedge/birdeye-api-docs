
- Always use the checksum contract address on supported chains.
- Supports filtering by `tx_type` for analyzing specific actions.
- Combine `offset` and `limit` for pagination over historical data.
- Useful for transaction visualizations, price tracking, or DEX analytics.
- High-frequency tokens may produce many transactions per second, so plan API usage accordingly.

required

The address of the token contract.

offset

integer

0 to 9999

Defaults to 0

Make sure offset + limit <= 10000

limit

integer

1 to 50

Defaults to 50

Number of items per page.

tx\_type

Defaults to swap

swapaddremoveall

`swap` `add` `remove` `all`

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200**✅ - JSON object containing transactions of a token


success

required

data

required

items

array of objects

required

items\*

View Additional Properties

hasNext

required

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/txs/token?offset=0&limit=50&tx_type=swap&sort_type=desc&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "items": [\
\
      {\
\
        "quote": {\
\
          "symbol": "SHIPE",\
\
          "decimals": 6,\
\
          "address": "9K78h3XEb7qqRu4XEaAEhe3qXaAeN1XyHa65bLwKXaNp",\
\
          "amount": 3000940514830,\
\
          "uiAmount": 3000940.51483,\
\
          "price": 0.00008920248678973954,\
\
          "nearestPrice": 0.00008879906452142359,\
\
          "changeAmount": 3000940514830,\
\
          "uiChangeAmount": 3000940.51483,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "base": {\
\
          "symbol": "SOL",\
\
          "decimals": 9,\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "amount": 1452043321,\
\
          "uiAmount": 1.452043321,\
\
          "price": 184.35493814782487,\
\
          "nearestPrice": 184.35493814782487,\
\
          "changeAmount": -1452043321,\
\
          "uiChangeAmount": -1.452043321,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "basePrice": 184.35493814782487,\
\
        "quotePrice": 0.00008920248678973954,\
\
        "txHash": "NLiBctRYuhibKZCJPkPxGhDKi9pCo2fx818H1UBJ82gD5DKddvufzf5DAPVKkLgejQ4EezcgE72FUrf327VQGaV",\
\
        "source": "pump_amm",\
\
        "blockUnixTime": 1754883867,\
\
        "txType": "swap",\
\
        "owner": "5V7aauQjnizwXAPGcJnjC7mbpenbiQZBfBSxW3n7NGCD",\
\
        "side": "sell",\
\
        "alias": null,\
\
        "pricePair": 2066701.7790924432,\
\
        "from": {\
\
          "symbol": "SOL",\
\
          "decimals": 9,\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "amount": 1452043321,\
\
          "uiAmount": 1.452043321,\
\
          "price": 184.35493814782487,\
\
          "nearestPrice": 184.35493814782487,\
\
          "changeAmount": -1452043321,\
\
          "uiChangeAmount": -1.452043321,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "to": {\
\
          "symbol": "SHIPE",\
\
          "decimals": 6,\
\
          "address": "9K78h3XEb7qqRu4XEaAEhe3qXaAeN1XyHa65bLwKXaNp",\
\
          "amount": 3000940514830,\
\
          "uiAmount": 3000940.51483,\
\
          "price": 0.00008920248678973954,\
\
          "nearestPrice": 0.00008879906452142359,\
\
          "changeAmount": 3000940514830,\
\
          "uiChangeAmount": 3000940.51483,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "tokenPrice": 184.35493814782487,\
\
        "poolId": "7LfK73yHk16kaSqa4FDB8t1oU445zzSsgMMC3at4eCFR"\
\
      }\
\
    ],

    "hasNext": true

  }

}
` `

