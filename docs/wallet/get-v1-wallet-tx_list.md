
- Starter
- Premium
- Business
- Enterprise

wallet

required

The address of a wallet.

limit

integer

1 to 100

Defaults to 100

Limit the number of records returned.

before

A transaction hash to traverse starting from. Only works with Solana.

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

     --url 'https://public-api.birdeye.so/v1/wallet/tx_list?limit=100&ui_amount_mode=scaled' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "solana": [\
\
      {\
\
        "txHash": "3MvG4bVz7HF76hWSGeGtcSkVAtDnLA5PmUVC97S22GPpGGvxbv7UqKEh91MVsAHJ35zSw4RkW9NBiHLfZbJm8xFn",\
\
        "blockNumber": 328889251,\
\
        "blockTime": "2025-03-24T15:06:14+00:00",\
\
        "status": true,\
\
        "from": "Gt4RRcMg2mzEN9SDtSUjEjezC9b1nXjEGDQyEVbrc7Sk",\
\
        "to": "11111111111111111111111111111111",\
\
        "fee": 80000,\
\
        "mainAction": "send",\
\
        "balanceChange": [\
\
          {\
\
            "amount": -165604794,\
\
            "symbol": "SOL",\
\
            "name": "Wrapped SOL",\
\
            "decimals": 9,\
\
            "address": "So11111111111111111111111111111111111111112",\
\
            "logoURI": "https://raw.githubusercontent.com/solana-labs/token-list/main/assets/mainnet/So11111111111111111111111111111111111111112/logo.png",\
\
            "isScaledUiToken": false,\
\
            "multiplier": null\
\
          }\
\
        ],\
\
        "contractLabel": {\
\
          "address": "11111111111111111111111111111111",\
\
          "name": "System Program",\
\
          "metadata": {\
\
            "icon": ""\
\
          }\
\
        },\
\
        "tokenTransfers": [\
\
          {\
\
            "fromTokenAccount": "Gt4RRcMg2mzEN9SDtSUjEjezC9b1nXjEGDQyEVbrc7Sk",\
\
            "toTokenAccount": "2YiHgAV2SaJYkLy63N3TMLZHKwkPKhWd3EUzAMZuay4T",\
\
            "fromUserAccount": "Gt4RRcMg2mzEN9SDtSUjEjezC9b1nXjEGDQyEVbrc7Sk",\
\
            "toUserAccount": "2YiHgAV2SaJYkLy63N3TMLZHKwkPKhWd3EUzAMZuay4T",\
\
            "tokenAmount": 0.165524794,\
\
            "mint": "So11111111111111111111111111111111111111111",\
\
            "transferNative": true,\
\
            "isScaledUiToken": false,\
\
            "multiplier": null\
\
          }\
\
        ]\
\
      }\
\
    ]

  }

}
` `

