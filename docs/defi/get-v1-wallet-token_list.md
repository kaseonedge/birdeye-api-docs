
- Starter
- Premium
- Business
- Enterprise

wallet

required

The address of a wallet.

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

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/v1/wallet/token_list?ui_amount_mode=scaled' \

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
        "decimals": 9,\
\
        "balance": 130718,\
\
        "uiAmount": 0.000130718,\
\
        "chainId": "solana",\
\
        "name": "Wrapped SOL",\
\
        "symbol": "SOL",\
\
        "icon": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
        "logoURI": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
        "priceUsd": 186.35315787784225,\
\
        "valueUsd": 0.02435971209147578,\
\
        "isScaledUiToken": false,\
\
        "multiplier": null\
\
      },\
\
      {\
\
        "address": "J1toso1uCk3RLmjorhTtrVwY9HJ7X8V9yYac6Y7kGCPn",\
\
        "decimals": 9,\
\
        "balance": 20280,\
\
        "uiAmount": 0.00002028,\
\
        "chainId": "solana",\
\
        "name": "Jito Staked SOL",\
\
        "symbol": "JitoSOL",\
\
        "icon": "https://storage.googleapis.com/token-metadata/JitoSOL-256.png",\
\
        "logoURI": "https://storage.googleapis.com/token-metadata/JitoSOL-256.png",\
\
        "priceUsd": 227.7398265331134,\
\
        "valueUsd": 0.0046185636820915395,\
\
        "isScaledUiToken": false,\
\
        "multiplier": null\
\
      },\
\
      {\
\
        "address": "J3NKxxXZcnNiMjKw9hYb2K4LUxgwB6t1FtPtQVsv3KFr",\
\
        "decimals": 8,\
\
        "balance": 3159,\
\
        "uiAmount": 0.00003159,\
\
        "chainId": "solana",\
\
        "name": "SPX6900 (Wormhole)",\
\
        "symbol": "SPX",\
\
        "icon": "https://i.postimg.cc/w3Yq0dHf/2023-12-21-17-19-37.jpg",\
\
        "logoURI": "https://i.postimg.cc/w3Yq0dHf/2023-12-21-17-19-37.jpg",\
\
        "priceUsd": 1.9727875449629464,\
\
        "valueUsd": 0.00006232035854537948,\
\
        "isScaledUiToken": false,\
\
        "multiplier": null\
\
      }\
\
    ]

  }

}
` `

