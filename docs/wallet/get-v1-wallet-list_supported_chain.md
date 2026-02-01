
- Lite
- Starter
- Premium
- Business
- Enterprise


## Responses

**200** ✅ - A list of supported networks for wallet APIs


success

required

data

array of strings

required

data\*

**400** ⚠️ - Bad Request


**401** ⚠️ - Unauthorized. API key is missing or invalid


**403** ⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429** ⚠️ - Too Many Requests. Rate limit reached


**500** ⚠️ - Internal Server Error


ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/v1/wallet/list_supported_chain \

     --header 'accept: application/json'
` `

` `



{

  "success": true,

  "data": [\
\
    "solana"\
\
  ]

}
` `

