
- Lite
- Starter
- Premium
- Business
- Enterprise

x-chain

Defaults to solana

A chain name listed in supported networks.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantlesui

# 200      JSON object containing the block number of the latest transaction on a chain

success

required

data

required

block\_number

integer

required

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/defi/v3/txs/latest-block \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "block_number": 22236994

  },

  "success": true

}
` `

