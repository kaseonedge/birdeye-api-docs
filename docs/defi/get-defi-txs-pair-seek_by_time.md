
- Starter
- Premium
- Business
- Enterprise

required

The address of a pair contract

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

tx\_type

Defaults to swap

swapaddremoveall

`swap` `add` `remove` `all`

before\_time

integer

1 to 10000000000

Specify the time seeked before using unix timestamps in seconds

after\_time

integer

1 to 10000000000

Specify the time seeked after using unix timestamps in seconds

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

**200**✅ - JSON object containing transactions of a pair


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

     --url 'https://public-api.birdeye.so/defi/txs/pair/seek_by_time?offset=0&limit=50&tx_type=swap&ui_amount_mode=scaled' \

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
        "txHash": "3zyGYe6NVJeFVPrsg2tvTdSxRoKGAiedcEqhuxhqUopdGoaAj69r4svfiePAstmogGoU8dkrfWnUj5PuMf4PCGie",\
\
        "source": "phoenix",\
\
        "blockUnixTime": 1741078031,\
\
        "txType": "swap",\
\
        "address": "4DoNfFBfF7UokCC2FQzriy7yHK6DY6NVdYpuekQ5pRgg",\
\
        "owner": "4yDvNjJxLCb5nznyowT8cgNwMs4i36eZaCyAgT6ZwPwv",\
\
        "from": {\
\
          "symbol": "USDC",\
\
          "decimals": 6,\
\
          "address": "EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v",\
\
          "amount": 92762810,\
\
          "typeSwap": "from",\
\
          "uiAmount": 92.76281,\
\
          "price": 0.99991,\
\
          "changeAmount": -92762810,\
\
          "uiChangeAmount": -92.76281,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "to": {\
\
          "symbol": "SOL",\
\
          "decimals": 9,\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "amount": 677000000,\
\
          "typeSwap": "to",\
\
          "uiAmount": 0.677,\
\
          "price": 136.96359554514504,\
\
          "changeAmount": 677000000,\
\
          "uiChangeAmount": 0.677,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        }\
\
      }\
\
    ],

    "hasNext": true

  }

}
` `

