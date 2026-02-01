
- Lite
- Starter
- Premium
- Business
- Enterprise

address

required

The address of the token contract.

time\_frame

required

Defaults to 24h

30m1h2h4h6h8h12h24h

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

sort\_by

required

Defaults to volume

Specify the sort field.

volumetrade

`volume` `trade`

offset

integer

0 to 10000

Defaults to 0

Pagination start position. offset + limit <= 10000

limit

integer

1 to 10

Defaults to 10

Number of items per page.

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

**200** ✅ - JSON object containing a list of top traded tokens


success

required

data

required

items

array of objects

items

tokenAddress

owner

tags

array

tags

type

volume

trade

integer

tradeBuy

integer

tradeSell

integer

volumeBuy

volumeSell

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v2/tokens/top_traders?time_frame=24h&sort_type=desc&sort_by=volume&offset=0&limit=10&ui_amount_mode=scaled' \

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
        "tokenAddress": "So11111111111111111111111111111111111111112",\
\
        "owner": "MfDuWeqSHEqTFVYZ7LoexgAK9dxk7cy4DFJWjWMGVWa",\
\
        "tags": [],\
\
        "type": "24h",\
\
        "volume": 1649180.8809921234,\
\
        "trade": 195729,\
\
        "tradeBuy": 101729,\
\
        "tradeSell": 94000,\
\
        "volumeBuy": 827695.1022708704,\
\
        "volumeSell": 821485.7787212529,\
\
        "isScaledUiToken": false,\
\
        "multiplier": null\
\
      }\
\
    ]

  }

}
` `

