
- Starter
- Premium
- Business
- Enterprise

list\_timeframe

A list of time frames seprated by comma (,). List of supported time frames: 1m, 5m, 30m, 1h, 2h, 4h, 8h, 24h, 2d, 3d, 7d

address

required

The address of the token contract.

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      JSON object containing list of price stats of tokens

success

required

Indicates if the request was successful

data

array of objects

required

Array of token data with price information for multiple timeframes

data\*

address

required

The address of the token contract.

is\_scaled\_ui\_token

multiplier

Multiplier used to scale the token price

data

array of objects

required

Price data for a timeframe

data\*

unix\_time\_update\_price

integer

required

Unix timestamp of when the data was updated

time\_frame

required

Time period for the data (e.g., '24h', '2d', '3d')

price

required

Current token price

price\_change\_percent

required

Percentage change in price over the specified timeframe

high

required

Highest price during the timeframe

low

required

Lowest price during the timeframe

scaled\_price

Current token scaled price

scaled\_high

Highest scaled price during the timeframe

scaled\_low

Lowest scaled price during the timeframe

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/price/stats/single?ui_amount_mode=raw' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": [\
\
    {\
\
      "address": "So11111111111111111111111111111111111111112",\
\
      "is_scaled_ui_token": false,\
\
      "data": [\
\
        {\
\
          "unix_time_update_price": 1751419434,\
\
          "time_frame": "1m",\
\
          "price": 147.37122560933628,\
\
          "price_change_percent": -0.023923362896247174,\
\
          "high": 147.48709093365915,\
\
          "low": 147.31438207414254\
\
        },\
\
        {\
\
          "unix_time_update_price": 1751419434,\
\
          "time_frame": "5m",\
\
          "price": 147.37122560933628,\
\
          "price_change_percent": 0.8046203174783053,\
\
          "high": 147.55458435764513,\
\
          "low": 146.0332035916541\
\
        }\
\
      ]\
\
    }\
\
  ],

  "success": true

}
` `

