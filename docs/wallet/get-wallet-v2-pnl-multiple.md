
- `token_metadata`: contains metadata of token
- `data[<wallet_address>]`: contain PnL of each wallet

token\_address

string

required

The address of the token contract.

wallets

string

required

List of wallet.

x-chain

string

enum

Defaults to solana

Solana network only.

solana

Allowed:

`solana`

# `` 200      JSON object containing multiple wallet’s PnL per token

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

     --url https://public-api.birdeye.so/wallet/v2/pnl/multiple \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
```

```

xxxxxxxxxx

{

  "success": true,

  "data": {

    "token_metadata": {

      "symbol": "PUMP",

      "decimals": 9

    },

    "data": {

      "3aLF8VXyUbEPSFyqSoQrsq6TdgKXgLmwJprE2yTfdNA2": {

        "counts": {

          "total_buy": 3,

          "total_sell": 0,

          "total_trade": 3

        },

        "quantity": {

          "total_bought_amount": 29285.756489887,

          "total_sold_amount": 0,

          "holding": 880839335.5814558

        },

        "cashflow_usd": {

          "cost_of_quantity_sold": 0,

          "total_invested": 2.6329984012898864,

          "total_sold": 0,

          "current_value": 7.5417466875590655

        },

        "pnl": {

          "realized_profit_usd": 0,

          "realized_profit_percent": 0,

          "unrealized_usd": -2.6327476566329686,

          "unrealized_percent": -99.99047683975823,

          "total_usd": -2.6327476566329686,

          "total_percent": -99.99047683975824,

          "avg_profit_per_trade_usd": 0

        },

        "pricing": {

          "current_price": 8.562000336395786e-9,

          "avg_buy_cost": 0.00008990713291627338,

          "avg_sell_cost": null

        }

      },

      "4mwReoK1x668B6KuuSAbGm2tUQULSTHGgTpCa2jUMXtD": {

        "counts": {

          "total_buy": 236570,

          "total_sell": 236570,

          "total_trade": 473140

        },

        "quantity": {

          "total_bought_amount": 1.9012623099995465,

          "total_sold_amount": 128820503932.7875,

          "holding": 880839335.5814558

        },

        "cashflow_usd": {

          "cost_of_quantity_sold": 5151221341.162621,

          "total_invested": 0.07602689546632857,

          "total_sold": 1944451989.1810136,

          "current_value": 7.5417466875590655

        },

        "pnl": {

          "realized_profit_usd": -0.04732872112474718,

          "realized_profit_percent": -62.25260262759055,

          "unrealized_usd": 0,

          "unrealized_percent": 0,

          "total_usd": -0.04732872112474718,

          "total_percent": -62.25260262759055,

          "avg_profit_per_trade_usd": -2.0006222735235735e-7

        },

        "pricing": {

          "current_price": 8.562000336395786e-9,

          "avg_buy_cost": 0.03998758880690519,

          "avg_sell_cost": 0.015094274046587626

        }

      }

    }

  }

}
```

* * *

