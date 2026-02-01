
- Business
- Enterprise

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

list\_address

required

Defaults to So11111111111111111111111111111111111111112,DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263

type

Defaults to 24h

1h2h4h8h24h

`1h` `2h` `4h` `8h` `24h`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200** ✅ -      JSON object containing price and volume with changes data of multiple tokens


success

required

data

required

A hashmap with token addresses as keys and the price volume object as value

View Additional Properties

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request POST \

     --url 'https://public-api.birdeye.so/defi/price_volume/multi?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'content-type: application/json' \

     --header 'x-chain: solana' \

     --data '

{

  "list_address": "So11111111111111111111111111111111111111112,DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263",

  "type": "24h"

}

'
` `

` `



{

  "success": true,

  "data": {

    "So11111111111111111111111111111111111111112": {

      "isScaledUiToken": false,

      "price": 128.94722473832456,

      "updateUnixTime": 1726678893,

      "updateHumanTime": "2024-09-18T17:01:33",

      "volumeUSD": 754317820.7943375,

      "volumeChangePercent": -6.2958716685581955,

      "priceChangePercent": -2.618887600381405

    },

    "DezXAZ8z7PnrnRJjz3wXBoRgixCa6xjnB7YaB1pPB263": {

      "isScaledUiToken": false,

      "price": 0.00001602442261925,

      "updateUnixTime": 1726678874,

      "updateHumanTime": "2024-09-18T17:01:14",

      "volumeUSD": 3196948.7086882377,

      "volumeChangePercent": -10.538000381034182,

      "priceChangePercent": -3.4737068687710613

    }

  }

}
` `

