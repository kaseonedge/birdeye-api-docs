
- Lite
- Starter
- Premium
- Business
- Enterprise

sort\_by

required

Defaults to rank

Specify the sort field.

rankvolumeUSDliquidity

`rank` `volumeUSD` `liquidity`

interval

Defaults to 24h

Specify the interval of trending.

1h4h24h

`1h` `4h` `24h`

sort\_type

required

Defaults to asc

Specify the sort order.

ascdesc

`asc` `desc`

offset

integer

Defaults to 0

Specify the offset for pagination. Filter for records with offset greater than the specified offset value, including those with offset equal to the specified offset.

limit

integer

1 to 20

Defaults to 20

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

**200** ✅ -      JSON object containing a list of trending tokens


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

liquidity

logoURI

name

symbol

volume24hUSD

volume24hChangePercent

rank

integer

price

price24hChangePercent

fdv

marketcap

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/token_trending?sort_by=rank&interval=24h&sort_type=asc&offset=0&limit=20&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "updateUnixTime": 1726681733,

    "updateTime": "2024-09-18T17:48:53",

    "tokens": [\
\
      {\
\
        "address": "HJXh1XULVe2Mdp6mTKd5K7of1uFqBTbmcWzvBv6cpump",\
\
        "decimals": 6,\
\
        "liquidity": 34641.80933146691,\
\
        "logoURI": "https://ipfs.io/ipfs/QmR7QnPaYcfwoG8oymK5JRDsB9GSgHr71mJmL2MuJ7Qk3x",\
\
        "name": "AVOCATO",\
\
        "symbol": "ATO",\
\
        "volume24hUSD": 1202872.3148187269,\
\
        "volume24hChangePercent": 33,\
\
        "rank": 1,\
\
        "price": 0.00010551649518689046,\
\
        "price24hChangePercent": 210,\
\
        "fdv": 17028232129,\
\
        "marketcap": 28232129\
\
      },\
\
      {\
\
        "address": "HYFDwieKWth1kzKbtLFMtgMVwukyvyWNYFxyQDcWpump",\
\
        "decimals": 6,\
\
        "liquidity": 73874.80948083404,\
\
        "logoURI": "https://ipfs.io/ipfs/QmUxhHFAugzzWmTMCMCky1QjaJNjtpBNhC2iRELb77Vqfw",\
\
        "name": "The Liquidator",\
\
        "symbol": "LIQUIDATOR",\
\
        "volume24hUSD": 920580.3615402475,\
\
        "volume24hChangePercent": 5,\
\
        "rank": 2,\
\
        "price": 0.0006106216453936813,\
\
        "price24hChangePercent": 12,\
\
        "fdv": 1495237953,\
\
        "marketcap": 5425292\
\
      }\
\
    ],

    "total": 1000

  }

}
` `

StripeM-Inner
