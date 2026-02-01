
- Lite
- Starter
- Premium
- Business
- Enterprise

required

Defaults to v24hUSD

Specify the sort field.

mcv24hUSDv24hChangePercentliquidity

`mc` `v24hUSD` `v24hChangePercent` `liquidity`

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 50

Defaults to 50

Number of items per page.

min\_liquidity

≥ 0

Defaults to 100

Specify the lower bound of liquidity. Filter for records with liquidity greater than the minimum liquidity value, excluding those with liquidity equal to the minimum.

max\_liquidity

Specify the upper bound of liquidity. Filter for records with liquidity less than the maximum liquidity value, excluding those with liquidity equal to the maximum.

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

**200** ✅ -      JSON object containing a list of tokens with certain fields


success

required

data

required

updateUnixTime

integer

updateTime

total

tokens

array of objects

tokens

address

decimals

integer

lastTradeUnixTime

integer

liquidity

logoURI

mc

name

symbol

v24hChangePercent

v24hUSD

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/tokenlist?sort_by=v24hUSD&sort_type=desc&offset=0&limit=50&min_liquidity=100&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "updateUnixTime": 1754885276,

    "updateTime": "2025-08-11T04:07:56.945Z",

    "tokens": [\
\
      {\
\
        "isScaledUiToken": false,\
\
        "multiplier": null,\
\
        "address": "So11111111111111111111111111111111111111112",\
\
        "decimals": 9,\
\
        "price": 185.45023454574132,\
\
        "lastTradeUnixTime": 1754885221,\
\
        "liquidity": 23349538049.2037,\
\
        "logoURI": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
        "mc": 100058305776.50261,\
\
        "name": "Wrapped SOL",\
\
        "symbol": "SOL",\
\
        "v24hChangePercent": -1.4820129368250423,\
\
        "v24hUSD": 9515832024.915321\
\
      }\
\
    ],

    "total": 298068

  }

}
` `

