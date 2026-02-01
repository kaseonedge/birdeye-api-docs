
- Lite
- Starter
- Premium
- Business
- Enterprise

time\_to

integer

1 to 10000000000

Specify the end time using unix timestamps in seconds

limit

integer

1 to 20

Defaults to 10

Number of items per page.

meme\_platform\_enabled

Defaults to false

Enable to receive token new listing from meme platforms (eg: pump.fun). This filter only supports Solana.

truefalse

`true` `false`

x-chain

Defaults to solana

A chain name listed in supported networks except Sui.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantle

# 200      JSON object containing a list of newly listed tokens

success

required

data

required

items

array of objects

items

address

symbol

name

source

liquidityAddedAt

logoURI

liquidity

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v2/tokens/new_listing?limit=10&meme_platform_enabled=false' \

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
        "address": "6Zk9e3nfXdYLXHYu5NvDiPHGMcjujVBv6gWRr7ckSdhP",\
\
        "symbol": "TOPCAT",\
\
        "name": "TOPCAT",\
\
        "decimals": 9,\
\
        "source": "raydium",\
\
        "liquidityAddedAt": "2024-09-18T17:59:23",\
\
        "logoURI": null,\
\
        "liquidity": 15507.41635596545\
\
      },\
\
      {\
\
        "address": "DsWUsiseYxAHZXEvq5cVcymYaohk8Gpe8E4otsjFpump",\
\
        "symbol": "Onigiri",\
\
        "name": "Onigiri",\
\
        "decimals": 6,\
\
        "source": "raydium",\
\
        "liquidityAddedAt": "2024-09-18T17:57:14",\
\
        "logoURI": "https://ipfs.io/ipfs/QmfXbLtRVuTTkazYqQix4R8FYW4Xkj2ZEnWKhLpGugaLQr",\
\
        "liquidity": 32994.397007045525\
\
      }\
\
    ]

  }

}
` `

StripeM-Inner
