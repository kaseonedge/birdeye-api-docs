
- Data Availability:
  - pump\_dot\_fun, moonshot, raydium\_launchlab: From 2025/06/20
  - meteora\_dynamic\_bonding\_curve: From 2025/09/20
  - four.meme: From 2025/11/20
  - nad.fun: From 2025/11/17

sort\_by

string

enum

required

Defaults to progress\_percent

progress\_percentgraduated\_timecreation\_timeliquiditymarket\_capfdvrecent\_listing\_timelast\_trade\_unix\_timeholdervolume\_1h\_usdvolume\_2h\_usdvolume\_4h\_usdvolume\_8h\_usdvolume\_24h\_usdvolume\_7d\_usdvolume\_30d\_usdvolume\_1h\_change\_percentvolume\_2h\_change\_percentvolume\_4h\_change\_percentvolume\_8h\_change\_percentvolume\_24h\_change\_percentvolume\_7d\_change\_percentvolume\_30d\_change\_percentprice\_change\_1h\_percentprice\_change\_2h\_percentprice\_change\_4h\_percentprice\_change\_8h\_percentprice\_change\_24h\_percentprice\_change\_7d\_percentprice\_change\_30d\_percenttrade\_1h\_counttrade\_2h\_counttrade\_4h\_counttrade\_8h\_counttrade\_24h\_counttrade\_7d\_counttrade\_30d\_count

Show 37 enum values

sort\_type

string

enum

required

Defaults to desc

Specify the sort order.

descasc

Allowed:

`desc``asc`

source

string

enum

Defaults to all

Source name of the meme token. Default to all

allpump\_dot\_funmoonshotraydium\_launchlabmeteora\_dynamic\_bonding\_curvefour.memenad.funflapsomethinglfj\_token\_mill

Show 10 enum values

creator

string

Creator of the meme token

platform\_id

string

The program address of the meme platform.

graduated

boolean

Filter meme tokens which already graduated

truefalse

min\_progress\_percent

number

0 to 100

max\_progress\_percent

number

0 to 100

min\_graduated\_time

number

0 to 10000000000

max\_graduated\_time

number

0 to 10000000000

min\_creation\_time

number

0 to 10000000000

max\_creation\_time

number

0 to 10000000000

min\_liquidity

number

Specify the lower bound of liquidity. Filter for records with liquidity greater than the minimum liquidity value, including those with liquidity equal to the minimum.

max\_liquidity

number

Specify the upper bound of liquidity. Filter for records with liquidity less than the maximum liquidity value, including those with liquidity equal to the maximum.

min\_market\_cap

number

Specify the lower bound of market cap. Filter for records with market cap greater than the minimum market cap value, including those with market cap equal to the minimum.

max\_market\_cap

number

Specify the upper bound of market cap. Filter for records with market cap less than the maximum market cap value, including those with market cap equal to the maximum.

min\_fdv

number

Specify the lower bound of FDV. Filter for records with FDV greater than the minimum FDV value, including those with FDV equal to the minimum.

max\_fdv

number

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

number

Specify the minimum volume in the last hour. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_2h\_usd

number

Specify the minimum volume in the last two hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_4h\_usd

number

Specify the minimum volume in the last four hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_8h\_usd

number

Specify the minimum volume in the last eight hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_24h\_usd

number

Specify the minimum volume in the last 24 hours. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_7d\_usd

number

Specify the minimum volume in the last 7 days. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_30d\_usd

number

Specify the minimum volume in the last 30 days. Filter for records with volume greater than the minimum volume value, including those with volume equal to the minimum.

min\_volume\_1h\_change\_percent

number

Specify the minimum volume change percentage in the last hour. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_2h\_change\_percent

number

Specify the minimum volume change percentage in the last two hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_4h\_change\_percent

number

Specify the minimum volume change percentage in the last four hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_8h\_change\_percent

number

Specify the minimum volume change percentage in the last eight hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_24h\_change\_percent

number

Specify the minimum volume change percentage in the last 24 hours. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_7d\_change\_percent

number

Specify the minimum volume change percentage in the last 7 days. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_volume\_30d\_change\_percent

number

Specify the minimum volume change percentage in the last 30 days. Filter for records with volume change percentage greater than the minimum volume change percentage value, including those with volume change percentage equal to the minimum.

min\_price\_change\_1h\_percent

number

Specify the minimum price change percentage in the last hour. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_2h\_percent

number

Specify the minimum price change percentage in the last two hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_4h\_percent

number

Specify the minimum price change percentage in the last four hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_8h\_percent

number

Specify the minimum price change percentage in the last eight hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_24h\_percent

number

Specify the minimum price change percentage in the last 24 hours. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_7d\_percent

number

Specify the minimum price change percentage in the last 7 days. Filter for records with price change percentage greater than the minimum price change percentage value, including those with price change percentage equal to the minimum.

min\_price\_change\_30d\_percent

number

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

x-chain

string

enum

Defaults to solana

Meme networks support.

solanabscmonad

Allowed:

`solana``bsc``monad`

# `` 200      OK

object

success

boolean

required

data

object

required

items

array of objects

required

items\*

object

View Additional Properties

hasNext

boolean

required

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/meme/list?sort_by=progress_percent&sort_type=desc&source=all&offset=0&limit=100' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "data": {

    "items": [\
\
      {\
\
        "address": "AYKYhju2mTQtR7MQdXwiWyEwCTTYrU3oTT4zkBtkmoon",\
\
        "logo_uri": "https://imagedelivery.net/TKv7KPMH2OHcr6ck7xjakw/21a93529-e58b-4975-55af-4d41af32f500/public",\
\
        "name": "CryptoStop",\
\
        "symbol": "CST",\
\
        "decimals": 9,\
\
        "extensions": null,\
\
        "market_cap": 10029.10632246309,\
\
        "fdv": 10029.10632246309,\
\
        "liquidity": 12242.094226513347,\
\
        "last_trade_unix_time": 1753255897,\
\
        "volume_1h_usd": 235.11977278340453,\
\
        "volume_1h_change_percent": 52.37871950362558,\
\
        "volume_2h_usd": 383.10579518803587,\
\
        "volume_2h_change_percent": -25.737252324323144,\
\
        "volume_4h_usd": 931.3254995946224,\
\
        "volume_4h_change_percent": -49.354266487949076,\
\
        "volume_8h_usd": 2743.069549449229,\
\
        "volume_8h_change_percent": -97.26138638848936,\
\
        "volume_24h_usd": 102534.05700111619,\
\
        "volume_24h_change_percent": null,\
\
        "volume_7d_usd": 102534.05700111619,\
\
        "volume_7d_change_percent": null,\
\
        "volume_30d_usd": 102534.05700111619,\
\
        "volume_30d_change_percent": null,\
\
        "trade_1h_count": 4,\
\
        "trade_2h_count": 11,\
\
        "trade_4h_count": 16,\
\
        "trade_8h_count": 40,\
\
        "trade_24h_count": 1893,\
\
        "trade_7d_count": 1893,\
\
        "trade_30d_count": 1893,\
\
        "price": 0.000010058942924819541,\
\
        "price_change_1h_percent": 8.271165093090064,\
\
        "price_change_2h_percent": 2.1377057711345255,\
\
        "price_change_4h_percent": 1.4128562857622766,\
\
        "price_change_8h_percent": -34.58129190021828,\
\
        "price_change_24h_percent": -85.0011848107867,\
\
        "price_change_7d_percent": -85.0011848107867,\
\
        "price_change_30d_percent": -85.0011848107867,\
\
        "holder": 154,\
\
        "recent_listing_time": 1753043373,\
\
        "meme_info": {\
\
          "source": "moonshot",\
\
          "platform_id": "MoonCVVNZFSYkqNXP6bxHLPL6QQJiMagDL3qcqUQTrG",\
\
          "address": "AYKYhju2mTQtR7MQdXwiWyEwCTTYrU3oTT4zkBtkmoon",\
\
          "created_at": {\
\
            "tx_hash": "5FRnyAQPYnCgoF6rCdTdQUbL8E5rwdXSJFCQzQmSqjU5za5chA9oQgFSKPZmZ3KjmDW9xHs29GaQFYJx2y1HcKt2",\
\
            "slot": 354628160,\
\
            "block_time": 1753043373\
\
          },\
\
          "creation_time": 1753043373,\
\
          "creator": "HtsetQ2pGkUtTm48Z3F378ojyrbDiHWppMzrWckGhLmS",\
\
          "graduated": true,\
\
          "graduated_time": 1753214231,\
\
          "pool": {\
\
            "address": "5HjW2SwFU1JPRGQGghuGWHhfN26Y1wGRTUYK9fx4s11T",\
\
            "curve_amount": "199159017507691861",\
\
            "total_supply": "1000000000000000000",\
\
            "marketcap_threshold": "345000000000",\
\
            "coef_b": "25",\
\
            "bump": "253"\
\
          },\
\
          "progress_percent": 100,\
\
          "graduated_at": {\
\
            "block_time": 1753214231,\
\
            "slot": 355060079,\
\
            "tx_hash": "58MySb9W8vApR4UeETLrU53tdkqVSJzuV9mZ34kxUN36TFRwbYvmY3tARDX3X8mdkUdbLVRFXDDCZYGnraNGwCQ2"\
\
          }\
\
        }\
\
      },\
\
      {\
\
        "address": "AWs6cxJNiEwrVnXu71uqmXCJULe1PxZSDx7MxYQxbonk",\
\
        "logo_uri": "https://ipfs.io/ipfs/bafkreig3bgqzvlvhxhx55yl7i7tppzvl5uzpvov4rpt26cv4asrbswvaf4",\
\
        "name": "venustwofacecat",\
\
        "symbol": "Venus",\
\
        "decimals": 6,\
\
        "extensions": {\
\
          "twitter": "https://x.com/i/communities/1947448738944815245",\
\
          "website": "https://www.instagram.com/venustwofacecat",\
\
          "description": "Why fit in when you were born to stand out?"\
\
        },\
\
        "market_cap": 4914.281770113641,\
\
        "fdv": 4914.281770113641,\
\
        "liquidity": 8117.992786759937,\
\
        "last_trade_unix_time": 1753255896,\
\
        "volume_1h_usd": 697.0690500797657,\
\
        "volume_1h_change_percent": 33.87172909699282,\
\
        "volume_2h_usd": 1204.417865604346,\
\
        "volume_2h_change_percent": -3.947266087241297,\
\
        "volume_4h_usd": 2446.9049222753542,\
\
        "volume_4h_change_percent": -90.86373950071808,\
\
        "volume_8h_usd": 131821.93451235816,\
\
        "volume_8h_change_percent": 21.443513195340387,\
\
        "volume_24h_usd": 327184.4163982051,\
\
        "volume_24h_change_percent": null,\
\
        "trade_1h_count": 7,\
\
        "trade_2h_count": 15,\
\
        "trade_4h_count": 32,\
\
        "trade_8h_count": 1270,\
\
        "trade_24h_count": 3076,\
\
        "price": 0.000004914473979143357,\
\
        "price_change_1h_percent": 2.2606451619729317,\
\
        "price_change_2h_percent": -0.9178555497059333,\
\
        "price_change_4h_percent": 7.005326917392453,\
\
        "price_change_8h_percent": -95.45733159513212,\
\
        "price_change_24h_percent": -86.38524988082759,\
\
        "holder": 116,\
\
        "recent_listing_time": 1753222103,\
\
        "meme_info": {\
\
          "created_at": {\
\
            "block_time": 1753222102,\
\
            "slot": 355079967,\
\
            "tx_hash": "2goMakFVCrXvzJWsMnUMTLB4x64MxxV9jHfHeH7rpjkdgNHjLF3yuMM6C6hVP4i1jSsyzj4ceQ691PVUyZGi7tc8"\
\
          },\
\
          "creator": "E8NgpMZkUCs3HiRQjEEENQbtDkdnM7RRHH7AmYbYX5r",\
\
          "address": "AWs6cxJNiEwrVnXu71uqmXCJULe1PxZSDx7MxYQxbonk",\
\
          "creation_time": 1753222102,\
\
          "graduated": true,\
\
          "pool": {\
\
            "virtual_base": "1073025605596382",\
\
            "creator": "E8NgpMZkUCs3HiRQjEEENQbtDkdnM7RRHH7AmYbYX5r",\
\
            "address": "6RZ74S934CjGCoXjcHmAMBDwig5cm5SmnrLBAuAvkjFN",\
\
            "base_decimals": 6,\
\
            "quote_mint": "So11111111111111111111111111111111111111112",\
\
            "auth_bump": 250,\
\
            "total_quote_fund_raising": "85000000000",\
\
            "supply": "1000000000000000",\
\
            "platform_fee": "4342059887",\
\
            "quote_protocol_fee": "1085515102",\
\
            "total_base_sell": "793100000000000",\
\
            "virtual_quote": "30000852951",\
\
            "base_mint": "AWs6cxJNiEwrVnXu71uqmXCJULe1PxZSDx7MxYQxbonk",\
\
            "base_vault": "5itDwpj1RUDR23b6Tb2wmjPeqp53biy9NEBW192etjRQ",\
\
            "platform_config": "FfYek5vEz23cMkWsdJwG2oa6EphsvXSHrGpdALN4g6W1",\
\
            "quote_decimals": 9,\
\
            "real_quote": "85000000171",\
\
            "quote_vault": "bbNEvCqSTAKFEBiaiCeXAuBnU2kqXx1XEEqKUXoDqNh",\
\
            "real_base": "793100000000000",\
\
            "status": 2\
\
          },\
\
          "progress_percent": 100,\
\
          "source": "raydium_launchlab",\
\
          "platform_id": "FfYek5vEz23cMkWsdJwG2oa6EphsvXSHrGpdALN4g6W1",\
\
          "graduated_time": 1753224598,\
\
          "graduated_at": {\
\
            "block_time": 1753224598,\
\
            "slot": 355086236,\
\
            "tx_hash": "3mM6ws8a961scPFAP9uandudmzvwhxR37GFwdpVsUC6cE38Ei8v6XZfNUnJj8AkF5jxNyKbpuSz9ZfmqjACEzW1M"\
\
          }\
\
        }\
\
      }\
\
    ],

    "has_next": true

  },

  "success": true

}
```

* * *

