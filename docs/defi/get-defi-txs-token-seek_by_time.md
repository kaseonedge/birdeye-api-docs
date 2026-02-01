
- Starter
- Premium
- Business
- Enterprise

required

The address of the token contract.

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

**200** ✅ -      JSON object containing transactions of a token


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

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/txs/token/seek_by_time?offset=0&limit=100&tx_type=swap&ui_amount_mode=scaled' \

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
          "symbol": "SOL",\
\
          "decimals": 9,\
\
          "address": "So11111111111111111111111111111111111111112",\
\
          "amount": "83",\
\
          "uiAmount": 8.3e-8,\
\
          "price": 133.58588874466795,\
\
          "changeAmount": 83,\
\
          "uiChangeAmount": 8.3e-8,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "base": {\
\
          "symbol": "Poppy",\
\
          "decimals": 6,\
\
          "address": "7Am9kVe9qymLGzLu9LnGFT6pX43DAuMYBLveSRijpump",\
\
          "amount": "2999999",\
\
          "uiAmount": 2.999999,\
\
          "price": 0.000003840642989117913,\
\
          "changeAmount": -2999999,\
\
          "uiChangeAmount": -2.999999,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "basePrice": 0.000003840642989117913,\
\
        "quotePrice": 133.58588874466795,\
\
        "txHash": "2rfQEtcrKmbCrwLet9REvUMWd6PoKjRV5fjUhYfmUjdS3ECkwF12s2bmswi8VGYxX1zp96nTfFxeSafjxDmASH6q",\
\
        "source": "pump_dot_fun",\
\
        "blockUnixTime": 1741531132,\
\
        "txType": "swap",\
\
        "owner": "J8RsYYa1CSsRi77aThfy48YPc7K5gwaepQDdvz2E3UoM",\
\
        "side": "buy",\
\
        "alias": null,\
\
        "pricePair": 36144566.26506024,\
\
        "from": {\
\
          "symbol": "Poppy",\
\
          "decimals": 6,\
\
          "address": "7Am9kVe9qymLGzLu9LnGFT6pX43DAuMYBLveSRijpump",\
\
          "amount": "2999999",\
\
          "uiAmount": 2.999999,\
\
          "price": 0.000003840642989117913,\
\
          "changeAmount": -2999999,\
\
          "uiChangeAmount": -2.999999,\
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
          "amount": "83",\
\
          "uiAmount": 8.3e-8,\
\
          "price": 133.58588874466795,\
\
          "changeAmount": 83,\
\
          "uiChangeAmount": 8.3e-8,\
\
          "isScaledUiToken": false,\
\
          "multiplier": null\
\
        },\
\
        "tokenPrice": 133.58588874466795,\
\
        "poolId": "2qPLBXMp8YvQyM1SDQ4QoYF314jcLzM86NpMUF6Wni6H"\
\
      }\
\
    ],

    "hasNext": true

  }

}
` `

