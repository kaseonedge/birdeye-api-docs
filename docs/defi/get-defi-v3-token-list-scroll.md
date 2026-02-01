
  - Do not include the scroll\_id parameter.
  - A next\_scroll\_id will be returned in the response.
- Subsequent Requests:
  - Must include the scroll\_id parameter, using the next\_scroll\_id from the previous response.
  - If scroll\_id is missing after the initial request, atfer 30 seconds, the API will return HTTP 400 (Bad Request).
- Scroll ID Rules:
  - Only one active scroll\_id per account is allowed every 30 seconds.
  - A scroll\_id expires 30 seconds after its last use.
  - A scroll\_id also expires if `items` returns empty.
  - Once expired, start over with a new initial request to generate a fresh scroll\_id.

limit

integer

1 to 5000

Defaults to 5000

Number of items per page.

scroll\_id

Assign scroll\_id to continue fetching data from previous scroll request

sort\_by

required

Defaults to liquidity

Specify the sort field.

liquiditymarket\_capfdvrecent\_listing\_timelast\_trade\_unix\_timeholdervolume\_1h\_usdvolume\_2h\_usdvolume\_4h\_usdvolume\_8h\_usdvolume\_24h\_usdvolume\_7d\_usdvolume\_30d\_usdvolume\_1h\_change\_percentvolume\_2h\_change\_percentvolume\_4h\_change\_percentvolume\_8h\_change\_percentvolume\_24h\_change\_percentvolume\_7d\_change\_percentvolume\_30d\_change\_percentprice\_change\_1h\_percentprice\_change\_2h\_percentprice\_change\_4h\_percentprice\_change\_8h\_percentprice\_change\_24h\_percentprice\_change\_7d\_percentprice\_change\_30d\_percenttrade\_1h\_counttrade\_2h\_counttrade\_4h\_counttrade\_8h\_counttrade\_24h\_counttrade\_7d\_counttrade\_30d\_count

sort\_type

required

Defaults to desc

Specify the sort order.

descasc

`desc` `asc`

min\_liquidity

Specify the lower bound of liquidity. Filter for records with liquidity greater than the minimum liquidity value, including those with liquidity equal to the minimum.

max\_liquidity

Specify the upper bound of liquidity. Filter for records with liquidity less than the maximum liquidity value, including those with liquidity equal to the maximum.

min\_market\_cap

Specify the lower bound of market cap. Filter for records with market cap greater than the minimum market cap value, including those with market cap equal to the minimum.

max\_market\_cap

Specify the upper bound of market cap. Filter for records with market cap less than the maximum market cap value, including those with market cap equal to the maximum.

min\_fdv

Specify the lower bound of FDV. Filter for records with FDV greater than the minimum FDV value, including those with FDV equal to the minimum.

max\_fdv

Specify the upper bound of FDV. Filter for records with FDV less than the maximum FDV value, including those with FDV equal to the maximum.

min\_recent\_listing\_time

integer

1 to 10000000000

Specify the lower bound of recent listing time. Filter for records with recent listing time greater than the minimum recent listing time value, including those with recent listing time equal to the minimum.

max\_recent\_listing\_time

integer

1 to 10000000000

Specify the upper bound of recent listing time. Filter for records with recent listing time less than the maximum recent listing time value, including those with recent listing time equal to the maximum.

min\_last\_trade\_unix\_time

integer

1 to 10000000000

Specify the lower bound of last trade time. Filter for records with last trade time greater than the minimum last trade time value, including those with last trade time equal to the minimum.

max\_last\_trade\_unix\_time

integer

1 to 10000000000

Specify the upper bound of last trade time. Filter for records with last trade time less than the maximum last trade time value, including those with last trade time equal to the maximum.

min\_holder

integer

Specify the minimum number of holders. Filter for records with holder count greater than the minimum holder count value, including those with holder count equal to the minimum.

min\_volume\_1h\_usd

Specify the minimum volume in the last hour. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_2h\_usd

Specify the minimum volume in the last two hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_4h\_usd

Specify the minimum volume in the last four hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_8h\_usd

Specify the minimum volume in the last eight hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_24h\_usd

Specify the minimum volume in the last 24 hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_7d\_usd

Specify the minimum volume in the last 7 days. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_30d\_usd

Specify the minimum volume in the last 30 days. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_1h\_change\_percent

Specify the minimum volume change percentage in the last hour. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_2h\_change\_percent

Specify the minimum volume change percentage in the last two hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_4h\_change\_percent

Specify the minimum volume change percentage in the last four hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_8h\_change\_percent

Specify the minimum volume change percentage in the last eight hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_24h\_change\_percent

Specify the minimum volume change percentage in the last 24 hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_7d\_change\_percent

Specify the minimum volume change percentage in the last 7 days. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_30d\_change\_percent

Specify the minimum volume change percentage in the last 30 days. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_price\_change\_1h\_percent

Specify the minimum price change percentage in the last hour. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_2h\_percent

Specify the minimum price change percentage in the last two hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_4h\_percent

Specify the minimum price change percentage in the last four hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_8h\_percent

Specify the minimum price change percentage in the last eight hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_24h\_percent

Specify the minimum price change percentage in the last 24 hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_7d\_percent

Specify the minimum price change percentage in the last 7 days. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_30d\_percent

Specify the minimum price change percentage in the last 30 days. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_trade\_1h\_count

integer

Specify the minimum number of trades in the last hour. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_2h\_count

integer

Specify the minimum number of trades in the last two hours. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_4h\_count

integer

Specify the minimum number of trades in the last four hours. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_8h\_count

integer

Specify the minimum number of trades in the last eight hours. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_24h\_count

integer

Specify the minimum number of trades in the last 24 hours. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_7d\_count

integer

Specify the minimum number of trades in the last 7 days. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

min\_trade\_30d\_count

integer

Specify the minimum number of trades in the last 30 days. Filter for records with trade count greater than the minimum trade count value, including those with trade count equal to the minimum.

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

Solana, Base, BSC, Ethereum, Monad network.

solanabasebscethereummonad

`solana` `base` `bsc` `ethereum` `monad`


## Responses

**200**✅ - JSON object containing a list of token


success

required

data

required

next\_scroll\_id

scroll\_time

items

array of objects

items

address

name

symbols

decimals

integer

logo\_uri

market\_cap

fdv

liquidity

price

holder

integer

volume\_1h\_usd

volume\_1h\_change\_percent

price\_change\_1h\_percent

trade\_1h\_count

integer

volume\_2h\_usd

volume\_2h\_change\_percent

price\_change\_2h\_percent

trade\_2h\_count

integer

volume\_4h\_usd

volume\_4h\_change\_percent

price\_change\_4h\_percent

trade\_4h\_count

integer

volume\_8h\_usd

volume\_8h\_change\_percent

price\_change\_8h\_percent

trade\_8h\_count

integer

volume\_24h\_usd

volume\_24h\_change\_percent

price\_change\_24h\_percent

trade\_24h\_count

integer

recent\_listing\_time

integer

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/list/scroll?limit=5000&sort_by=liquidity&sort_type=desc&ui_amount_mode=scaled' \

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
        "address": "So11111111111111111111111111111111111111112",\
\
        "logo_uri": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
        "name": "Wrapped SOL",\
\
        "symbol": "SOL",\
\
        "decimals": 9,\
\
        "extensions": {\
\
          "coingecko_id": "solana",\
\
          "serum_v3_usdc": "9wFFyRfZBsuAha4YcuxcXLKwMxJR43S7fPfQLusDBzvT",\
\
          "serum_v3_usdt": "HWHvQhFmJB3NUcu1aihKmrKegfVxBEHzwVX6yZCKEsi1",\
\
          "website": "https://solana.com/",\
\
          "telegram": null,\
\
          "twitter": "https://twitter.com/solana",\
\
          "description": "Wrapped Solana ",\
\
          "discord": "https://discordapp.com/invite/pquxPsq",\
\
          "medium": "https://medium.com/solana-labs"\
\
        },\
\
        "market_cap": 100119664431.51688,\
\
        "fdv": 112672175707.38792,\
\
        "total_supply": 607331645.8349773,\
\
        "circulating_supply": 539665463.3820738,\
\
        "liquidity": 23353595552.52654,\
\
        "last_trade_unix_time": 1754885383,\
\
        "volume_1h_usd": 443688491.34178054,\
\
        "volume_1h_change_percent": -1.714504394496686,\
\
        "volume_2h_usd": 861291542.4427114,\
\
        "volume_2h_change_percent": -3.5864189799692134,\
\
        "volume_4h_usd": 1747234746.548523,\
\
        "volume_4h_change_percent": -8.826330954721023,\
\
        "volume_8h_usd": 3423287365.9121313,\
\
        "volume_8h_change_percent": 8.888103083472839,\
\
        "volume_24h_usd": 9530159635.659721,\
\
        "volume_24h_change_percent": -1.3364377681566488,\
\
        "trade_1h_count": 1535608,\
\
        "trade_2h_count": 2948829,\
\
        "trade_4h_count": 5684776,\
\
        "trade_8h_count": 11119027,\
\
        "trade_24h_count": 31542138,\
\
        "buy_24h": 13941877,\
\
        "buy_24h_change_percent": -2.1854401371296177,\
\
        "volume_buy_24h_usd": 4728527789.759392,\
\
        "volume_buy_24h_change_percent": -1.6920149268570155,\
\
        "sell_24h": 17600261,\
\
        "sell_24h_change_percent": -3.143992919930877,\
\
        "volume_sell_24h_usd": 4801631845.900329,\
\
        "volume_sell_24h_change_percent": -0.9837807096207587,\
\
        "unique_wallet_24h": 1262031,\
\
        "unique_wallet_24h_change_percent": -26.286938857043396,\
\
        "price": 185.56395800803165,\
\
        "price_change_1h_percent": 0.4114972388399392,\
\
        "price_change_2h_percent": 0.4575777911423116,\
\
        "price_change_4h_percent": 1.8680908355708248,\
\
        "price_change_8h_percent": 1.3798037663979583,\
\
        "price_change_24h_percent": 0.5817906810497413,\
\
        "holder": 3472550,\
\
        "recent_listing_time": null,\
\
        "is_scaled_ui_token": false,\
\
        "multiplier": null\
\
      }\
\
    ],

    "hasNext": true

  }

}
` `

