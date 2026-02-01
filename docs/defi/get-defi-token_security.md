| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Lite
- Starter
- Premium
- Business
- Enterprise

address

string

required

The address of the token contract.

x-chain

string

enum

Defaults to solana

A chain name listed in supported networks except Sui.

solanaethereumarbitrumavalanchebscoptimismpolygonbasezksyncmonadhyperevmaptosfogomantle

Show 14 enum values

# `` 200      JSON object containing a security information of a token

object

success

boolean

required

data

object

required

Has additional fields

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

Updated 24 days ago

* * *

Did this page help you?

Yes

No

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url https://public-api.birdeye.so/defi/token_security \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx



{

  "data": {

    "creatorAddress": "9AhKqLR67hwapvG8SA2JFXaCshXc9nALJjpKaHZrsbkw",

    "creatorOwnerAddress": null,

    "ownerAddress": null,

    "ownerOfOwnerAddress": null,

    "creationTx": "2K5X6HT9QZ8dcApbWL6mzYw6WBDvL5vWndTpGrFkQuMfuStGTP5LxPNQnnn5v5KR2T6UD1zEXnfCdajzUfuCPZgS",

    "creationTime": 1670531612,

    "creationSlot": 165714665,

    "mintTx": "44Jfxh3VFp6N2h3CLMGeHHxeexdtUnHRsvQ2QXF9h9JqHiBvjt2xCbJg7G443hPVvG4y5VP95iaiSRKuLVVcadCe",

    "mintTime": 1683780182,

    "mintSlot": 193273646,

    "creatorBalance": 48343.76164,

    "ownerBalance": null,

    "ownerPercentage": null,

    "creatorPercentage": 5.44198858929173e-10,

    "metaplexUpdateAuthority": "9AhKqLR67hwapvG8SA2JFXaCshXc9nALJjpKaHZrsbkw",

    "metaplexOwnerUpdateAuthority": null,

    "metaplexUpdateAuthorityBalance": 48343.76164,

    "metaplexUpdateAuthorityPercent": 5.44198858929173e-10,

    "mutableMetadata": true,

    "top10HolderBalance": 27020571907755.746,

    "top10HolderPercent": 0.3041667404641445,

    "top10UserBalance": 27020571907755.746,

    "top10UserPercent": 0.3041667404641445,

    "isTrueToken": null,

    "fakeToken": null,

    "totalSupply": 88834735403757.8,

    "preMarketHolder": [],

    "lockInfo": null,

    "freezeable": null,

    "freezeAuthority": null,

    "transferFeeEnable": null,

    "transferFeeData": null,

    "isToken2022": false,

    "nonTransferable": null,

    "jupStrictList": true

  },

  "success": true

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
