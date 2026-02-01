#### URL Expired

The URL for this request expired after 30 days.

# `` 200      A list of supported networks

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

     --url https://public-api.birdeye.so/defi/networks \

     --header 'accept: application/json'
```

```

xxxxxxxxxx



{

  "success": true,

  "data": [\
\
    "solana",\
\
    "ethereum",\
\
    "arbitrum",\
\
    "avalanche",\
\
    "bsc",\
\
    "optimism",\
\
    "polygon",\
\
    "base",\
\
    "zksync",\
\
    "monad",\
\
    "hyperevm",\
\
    "aptos",\
\
    "fogo",\
\
    "mantle",\
\
    "sui"\
\
  ]

}
```

Updated 24 days ago

* * *

Did this page help you?

Yes

No
