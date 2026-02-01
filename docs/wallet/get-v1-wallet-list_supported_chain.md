| Time | Status | User Agent |  |
| :-- | :-- | :-- | :-- |
| Make a request to see history. |

#### URL Expired

The URL for this request expired after 30 days.

- Standard
- Lite
- Starter
- Premium
- Business
- Enterprise

# `` 200      A list of supported networks for wallet APIs

object

success

boolean

required

data

array of strings

required

data\*

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

     --url https://public-api.birdeye.so/v1/wallet/list_supported_chain \

     --header 'accept: application/json'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": [\
\
    "solana"\
\
  ]

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
