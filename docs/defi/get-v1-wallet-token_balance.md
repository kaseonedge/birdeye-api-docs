
- Starter
- Premium
- Business
- Enterprise

wallet

required

The address of a wallet.

token\_address

required

The address of a token.

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

required

Defaults to solana

A chain name listed in supported networks.

solana

`solana`

# 200

success

required

data

required

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/v1/wallet/token_balance?ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "address": "So11111111111111111111111111111111111111112",

    "decimals": 9,

    "balance": 130718,

    "uiAmount": 0.000130718,

    "chainId": "solana-mainnet",

    "logoURI": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",

    "name": "Wrapped SOL",

    "symbol": "SOL",

    "priceUsd": 186.17611361160655,

    "valueUsd": 0.024336569219081984,

    "isScaledUiToken": false,

    "multiplier": null

  }

}
` `

