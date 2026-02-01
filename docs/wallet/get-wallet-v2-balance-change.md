
- Lite
- Starter
- Premium
- Business
- Enterprise

address

required

The address of the account.

token\_address

The address of the token contract.

time\_from

integer

0 to 10000000000

Specify the start time using unix timestamps in seconds

time\_to

integer

0 to 10000000000

Specify the end time using unix timestamps in seconds

type

SOLSPL

`SOL` `SPL`

change\_type

increasedecrease

`increase` `decrease`

offset

integer

0 to 10000

Defaults to 0

Make sure offset <= 10000

limit

integer

1 to 100

Defaults to 20

ui\_amount\_mode

Defaults to scaled

Indicate whether to use the scaled amount for scaled ui amount tokens. Only support solana

rawscaled

`raw` `scaled`

x-chain

Defaults to solana

Solana network only.

solana

`solana`


## Responses

**200**✅ - JSON object containing a list of balance changes of an address


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

     --url 'https://public-api.birdeye.so/wallet/v2/balance-change?offset=0&limit=20&ui_amount_mode=scaled' \

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
        "time": "2025-08-01T08:55:58Z",\
\
        "block_number": 357129280,\
\
        "block_unix_time": 1754038558,\
\
        "address": "51dEMNojjd2hZKrMeDWBRMPmhDS5QH1eCQWCdtR7CYKp",\
\
        "token_account": "ATgjegWTEidtsDniCfVJp5Py86fi5X8nzRyzndfimr59",\
\
        "tx_hash": "mBxrLzapLZtcdPsKSr6EkUUXgFJDyXJs7bJcwQ58xh7JXhN7nsz9ELNspxsnG6TxVaJdzsbrkvhjgrX8QArrp4h",\
\
        "pre_balance": "257629693",\
\
        "post_balance": "293106471",\
\
        "amount": "35476777",\
\
        "token_info": {\
\
          "address": "4a79c1TRehFCpHxQ7niHAiBAvHRJRWey3UkWuMDREKL7",\
\
          "decimals": 9,\
\
          "symbol": "",\
\
          "name": "",\
\
          "logo_uri": "",\
\
          "is_scaled_ui_token": true,\
\
          "multiplier": 1.5\
\
        },\
\
        "type": 2,\
\
        "type_text": "SPL",\
\
        "change_type": 1,\
\
        "change_type_text": "INCR"\
\
      }\
\
    ]

  }

}
` `

