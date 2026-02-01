
- Starter
- Premium
- Business
- Enterprise

address

required

The address of a trader.

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

**200** ✅ -      JSON object containing transactions of a trader


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

     --url 'https://public-api.birdeye.so/trader/txs/seek_by_time?offset=0&limit=100&ui_amount_mode=scaled' \

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
          "amount": 8791828613200,\
\
          "type": "split",\
\
          "type_swap": "to",\
\
          "ui_amount": 8791.8286132,\
\
          "price": 182.32478738013168,\
\
          "nearest_price": 182.32478738013168,\
\
          "change_amount": 8791828613200,\
\
          "ui_change_amount": 8791.8286132,\
\
          "is_scaled_ui_token": false,\
\
          "multiplier": null\
\
        },\
\
        "base": {\
\
          "symbol": "BNSOL",\
\
          "decimals": 9,\
\
          "address": "BNso1VUJnh4zcfpZa6986Ea66P6TCp59hvtNJ8b1X85",\
\
          "amount": 8243057055060,\
\
          "type": "burn",\
\
          "type_swap": "from",\
\
          "ui_amount": 8243.05705506,\
\
          "price": 195.07266605796318,\
\
          "nearest_price": 195.07266605796318,\
\
          "change_amount": -8243057055060,\
\
          "ui_change_amount": -8243.05705506,\
\
          "is_scaled_ui_token": false,\
\
          "multiplier": null\
\
        },\
\
        "base_price": 195.07266605796318,\
\
        "quote_price": 182.32478738013168,\
\
        "tx_hash": "3tiVFmNkAzesSgJ8RJfRMFSMSTGMbvVd8Qm23uroSCPQFSi6rqhr9tqCCRCu4nZD8u3jLVMcuh3qxmEzFnbS61rF",\
\
        "source": "stake_pool",\
\
        "block_unix_time": 1754870741,\
\
        "tx_type": "swap",\
\
        "address": "Hr9pzexrBge3vgmBNRR8u42CNQgBXdHm4UkUN2DH4a7r",\
\
        "owner": "GBJ4MZe8fqpA6UVgjh19BwJPMb79KDfMv78XnFVxgH2Q",\
\
        "block_number": 359226070,\
\
        "volume_usd": 1602968.2825842479,\
\
        "volume": 8243.05705506,\
\
        "ins_index": 2,\
\
        "inner_ins_index": 0,\
\
        "signers": [\
\
          "GBJ4MZe8fqpA6UVgjh19BwJPMb79KDfMv78XnFVxgH2Q",\
\
          "5Z4RXtFUSBzQeptBRxBT4PHFMdMqgTt6YXNwEgngcSQ7"\
\
        ],\
\
        "interacted_program_id": "bn1dUNRecofQLxcGp895mGmKEVtFLMjdvjxBjFqhFU7"\
\
      }\
\
    ],

    "hasNext": true

  }

}
` `

