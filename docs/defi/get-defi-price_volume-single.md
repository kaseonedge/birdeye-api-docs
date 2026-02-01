
- Starter
- Premium
- Business
- Enterprise

required

The address of the token contract.

type

required

Defaults to 24h

Time frame/interval.

1h2h4h8h24h

`1h` `2h` `4h` `8h` `24h`

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200** ✅ - JSON object containing price and volume with changes data of a token


success

required

data

required

price

required

updateUnixTime

integer

required

updateHumanTime

required

volumeUSD

required

volumeChangePercent

required

priceChangePercent

required

isScaledUiToken

scaledValue

multiplier

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/price_volume/single?type=24h&ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "isScaledUiToken": false,

    "price": 128.70426432642992,

    "updateUnixTime": 1726678569,

    "updateHumanTime": "2024-09-18T16:56:09",

    "volumeUSD": 755004403.5277437,

    "volumeChangePercent": -6.0377419970263055,

    "priceChangePercent": -2.6091746792986936

  }

}
` `

