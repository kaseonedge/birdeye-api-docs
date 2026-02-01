
- Enterprise

required

Defaults to 24h

Time interval (Example: '24h')

1m5m30m1h2h4h8h24h3d7d14d30d90d180d1yalltime

list\_address

required

A list of token addresses in string separated by commas (,)

ui\_amount\_mode

Defaults to raw

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaledboth

`raw` `scaled` `both`

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      OK

data

array of objects

data

address

total\_volume

total\_volume\_usd

volume\_buy\_usd

volume\_sell\_usd

volume\_buy

volume\_sell

total\_trade

buy

sell

success

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request POST \

     --url 'https://public-api.birdeye.so/defi/v3/all-time/trades/multiple?time_frame=24h&ui_amount_mode=raw' \

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
      "total_volume": 158766463.26959822,\
\
      "total_volume_usd": 20188521260.405678,\
\
      "volume_buy_usd": 20188521260.405678,\
\
      "volume_sell_usd": 20188521260.405678,\
\
      "volume_buy": 78227859.16098201,\
\
      "volume_sell": 80538604.1086162,\
\
      "total_trade": 258522892,\
\
      "buy": 87829497,\
\
      "sell": 170693395\
\
    }\
\
  ],

  "success": true

}
` `

