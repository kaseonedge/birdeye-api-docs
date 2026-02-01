
- When `time_from` and `time_to` are passed but are not within the current cycle, the `remaining`, `overage_usage`, `overage_cost` will be `null`

time\_from

integer

0 to 10000000000

Specify the start time using unix timestamps in seconds

time\_to

integer

0 to 10000000000

Specify the end time using unix timestamps in seconds


## Responses

**200**✅ - JSON object containing the credits usage


success

required

data

required

start\_time

integer

required

end\_time

integer

required

usage

required

usage object

remaining

remaining object

overage\_usage

overage\_usage object

overage\_cost

overage\_cost object

**400**⚠️ - Bad Request


**401**⚠️ - Unauthorized. API key is missing or invalid


**403**⚠️ - Forbidden. Request is blacklisted or not whitelisted


**429**⚠️ - Too Many Requests. Rate limit reached


**500**⚠️ - Internal Server Error


Updated 2 months ago

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/utils/v1/credits \

     --header 'accept: application/json'
` `

` `



{

  "data": {

    "start_time": 1758367608,

    "end_time": 1760959608,

    "usage": {

      "total": 1176300,

      "api": 1162912,

      "ws": 13388

    },

    "remaining": {

      "api": 1498837088,

      "ws": 49986612,

      "total": 1548823700

    },

    "overage_usage": {

      "api": 0,

      "ws": 0,

      "total": 0

    },

    "overage_cost": {

      "api": 0,

      "ws": 0,

      "total": 0

    }

  },

  "success": true

}
` `

Updated 2 months ago

