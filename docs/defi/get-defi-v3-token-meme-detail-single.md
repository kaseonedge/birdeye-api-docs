
- Returns: Detailed token metrics such as:
  - Price, 24h volume, market cap
  - Price change, popularity score
  - Listing timestamp and token metadata
- Data Availability:
  - pump\_dot\_fun, moonshot, raydium\_launchlab: From 2025/06/20
  - meteora\_dynamic\_bonding\_curve: From 2025/09/20
  - four.meme: From 2025/11/20
  - nad.fun: From 2025/11/17

address

required

Defaults to HHuLN58RAJoyNxwYte8NdEyV7dhQzDCLXDmTraHspump

Address of a meme token

x-chain

Defaults to solana

Meme networks support.

solanabscmonad

`solana` `bsc` `monad`


## Responses

**200** ✅ - OK


success

required

data

required

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url 'https://public-api.birdeye.so/defi/v3/token/meme/detail/single?address=HHuLN58RAJoyNxwYte8NdEyV7dhQzDCLXDmTraHspump' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "data": {

    "address": "6R3LxpHiE8RjTL7HnvKWtoQCHVA76CR1ebF9MYk61wzS",

    "name": "RekaAI",

    "symbol": "RekaAI",

    "decimals": 6,

    "extensions": {

      "twitter": "https://x.com/FusionLab_Inc",

      "website": "https://reka.ai",

      "description": "Multimodal AI you can deploy anywhere"

    },

    "logo_uri": "https://ipfs.io/ipfs/QmXuk2dXxM5hYARaxoPyoryJm5UQHdTkEhXrtsFFU7Siay",

    "price": 0.001,

    "liquidity": 0.2919295560985348,

    "circulating_supply": 1000000000,

    "market_cap": 1000000,

    "total_supply": 1000000000,

    "fdv": 1000000,

    "meme_info": {

      "source": "pump_dot_fun",

      "platform_id": "6EF8rrecthR5Dkzon8Nwu78hRvfCKubJ14M5uBEwF6P",

      "created_at": {

        "tx_hash": "25CRJJs4B5NVTgu6Sv1mMVpnXYMT5HG7LcfmvXTV5Tkp1GN8ajXDTjW59NTFN1UsHkXjkfCeUs7gKQAzTufCjpnw",

        "slot": 330948137,

        "block_time": 1743653081

      },

      "creation_time": 1743653081,

      "creator": "2suZVbGzdD1jdMFgyojG35TR6XWKFtSbprvjnTFAg8Ru",

      "updated_at": {

        "tx_hash": "25CRJJs4B5NVTgu6Sv1mMVpnXYMT5HG7LcfmvXTV5Tkp1GN8ajXDTjW59NTFN1UsHkXjkfCeUs7gKQAzTufCjpnw",

        "slot": 330948137

      },

      "graduated_at": {

        "slot": null,

        "tx_hash": null,

        "block_time": null

      },

      "graduated": false,

      "graduated_time": null,

      "pool": {

        "address": "2T6KViNFRuQb1MiFbmEtM4cA1mK2ayHKJTZHJ9K7aNw4",

        "real_sol_reserves": "0",

        "real_token_reserves": "793100000000000",

        "token_total_supply": "1000000000000000",

        "virtual_token_reserves": "1073000000000000"

      },

      "progress_percent": 0,

      "address": "6R3LxpHiE8RjTL7HnvKWtoQCHVA76CR1ebF9MYk61wzS"

    }

  },

  "success": true

}
` `

