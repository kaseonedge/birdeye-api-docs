
- Lite
- Starter
- Premium
- Business
- Enterprise

type

required

Defaults to 1W

Specify the type of top gainers/losers. Filter for records with type equal to the specified type.

yesterdaytoday1W

`yesterday` `today` `1W`

sort\_by

required

Defaults to PnL

Specify the sort field.

PnL

`PnL`

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

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

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui


## Responses

**200** ✅ -      JSON object containing a list of top gainer loser traders


success

required

data

required

items

array of objects

items

network

address

pnl

volume

trade\_count

integer

**400** ⚠️ -      Bad Request


**401** ⚠️ -      Unauthorized. API key is missing or invalid


**403** ⚠️ -      Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ -      Too Many Requests. Rate limit reached


**500** ⚠️ -      Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/trader/gainers-losers?type=1W&sort_by=PnL&sort_type=desc&offset=0&limit=10' \

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
        "network": "solana",\
\
        "address": "FciNKwZAvSzepKH1nFEGeejzbP4k87dJiP9BAzGt2Sm3",\
\
        "pnl": 675542.1369220349,\
\
        "trade_count": 74194,\
\
        "volume": 1372626.717443506\
\
      },\
\
      {\
\
        "network": "solana",\
\
        "address": "Habp5bncMSsBC3vkChyebepym5dcTNRYeg2LVG464E96",\
\
        "pnl": 175542.1369220349,\
\
        "trade_count": 20,\
\
        "volume": 1372626.717443506\
\
      }\
\
    ]

  }

}
` `

