
- Insights in the responses
- `counts`:

  - `total_buy`: Total number of buy trades.
  - `total_sell`: Total number of sell trades.
  - `total_trade`: Combined total of buys and sells.
  - `total_win`: Total trades have profit.
  - `total_loss`: Total trades in loss.
  - `win_rate`: Winning rate
- `cashflow_usd`:

  - `total_invested`: USD spent on all buys.
  - `total_sold`: USD received from sales.
  - `current_value`: Current position value in USD.
- `pnl`:

  - `realized_profit_usd`: Profit/loss from completed trades.
  - `realized_profit_percent`: % gain/loss relative to sold cost basis.
  - `unrealized_usd`: Profit/loss of current holdings (mark-to-market).
  - `total_usd`: Sum of realized + unrealized profit in USD.
  - `avg_profit_per_trade_usd`: Average profit/loss per trade.

wallet

string

required

The wallet of the account.

duration

string

enum

Defaults to all

Duration of wallet pnl

all90d30d7d24h

Allowed:

`all``90d``30d``7d``24h`

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing a wallet’s PnL

object

success

boolean

required

data

object

required

# `` 400      Bad Request

# `` 401      Unauthorized. API key is missing or invalid

# `` 403      Forbidden. Request is blacklisted or not whitelisted

# `` 429      Too Many Requests. Rate limit reached

# `` 500      Internal Server Error

* * *

ShellPythonJavaScriptGo

```

xxxxxxxxxx

curl --request GET \

     --url 'https://public-api.birdeye.so/wallet/v2/pnl/summary?duration=all' \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "summary": {

      "unique_tokens": 2,

      "counts": {

        "total_buy": 11,

        "total_sell": 3,

        "total_trade": 14,

        "total_win": 0,

        "total_loss": 0,

        "win_rate": 0

      },

      "cashflow_usd": {

        "total_invested": 175666.37823969766,

        "total_sold": 87670.81375594059

      },

      "pnl": {

        "realized_profit_usd": 6045.934178885913,

        "realized_profit_percent": 0.07406974699642274,

        "unrealized_usd": -74830.62425247866,

        "total_usd": -68784.69007359275,

        "avg_profit_per_trade_usd": -4913.192148113768

      }

    }

  }

}
```

* * *

