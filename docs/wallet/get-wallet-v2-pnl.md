
- `meta`:

  - `address`: Wallet address.
  - `currency`: The currency in which PnL is calculated (e.g., usd).
- `tokens[<token_address>]`:

  - `symbol`: Token ticker (e.g., SOL, ...).
  - `decimals`: Number of decimal places the token uses.
  - `counts`:

    - `total_buy`: Total number of buy trades.
    - `total_sell`: Total number of sell trades.
    - `total_trade`: Combined total of buys and sells.
  - `quantity`: **Note: values are already normalized by`10^-decimals`**
    - `total_bought_amount`: Total token units purchased.
    - `total_sold_amount`: Total token units sold.
    - `holding`: Current balance (net holdings still in wallet).
  - `cashflow_usd`:

    - `total_invested`: USD spent on all buys.
    - `cost_of_quantity_sold`: USD cost basis of the tokens already sold.
    - `total_sold`: USD received from sales.
    - `current_value`: Current USD value of remaining holdings.
  - `pnl`:

    - `realized_profit_usd`: Profit/loss from completed trades.
    - `realized_profit_percent`: % gain/loss relative to sold cost basis.
    - `unrealized_usd`: Profit/loss of current holdings (mark-to-market).
    - `unrealized_percent`: % unrealized gain/loss.
    - `total_usd`: Sum of realized + unrealized profit in USD.
    - `total_percent`: Overall ROI % including realized and unrealized.
    - `avg_profit_per_trade_usd`: Average profit/loss per trade.
  - `pricing`:

    - `current_price`: Current market price per token in USD.
    - `avg_buy_cost`: Average buy price across trades (USD).
    - `avg_sell_cost`: Average sell price across trades (USD).

wallet

required

The wallet of the account.

token\_addresses

required

List of token address.

x-chain

Defaults to solana

Solana network only.

solana

`solana`

# 200      JSON object containing a wallet’s PnL per token

success

required

data

required

# 400      Bad Request

# 401      Unauthorized. API key is missing or invalid

# 403      Forbidden. Request is blacklisted or not whitelisted

# 429      Too Many Requests. Rate limit reached

# 500      Internal Server Error

ShellPythonJavaScriptGo

` `



curl --request GET \

     --url https://public-api.birdeye.so/wallet/v2/pnl \

     --header 'accept: application/json' \

     --header 'x-chain: solana'
` `

` `



{

  "success": true,

  "data": {

    "meta": {

      "address": "4mwReoK1x668B6KuuSAbGm2tUQULSTHGgTpCa2jUMXtD",

      "currency": "usd",

      "holding_check": false,

      "time": "2025-08-27T14:06:48.987054346Z"

    },

    "tokens": {

      "So11111111111111111111111111111111111111112": {

        "symbol": "SOL",

        "decimals": 9,

        "counts": {

          "total_buy": 236570,

          "total_sell": 236570,

          "total_trade": 473140

        },

        "quantity": {

          "total_bought_amount": 12092390.76837637,

          "total_sold_amount": 0.00047313999999776897,

          "holding": 0

        },

        "cashflow_usd": {

          "cost_of_quantity_sold": 0.07608073802599198,

          "total_invested": 1944451989.1810136,

          "total_sold": 0.07602689546632857,

          "current_value": 0

        },

        "pnl": {

          "realized_profit_usd": -0.00005384255966340998,

          "realized_profit_percent": -0.0707702909572399,

          "unrealized_usd": 523529777.302561,

          "unrealized_percent": 26.92428407777512,

          "total_usd": 523529777.30250716,

          "total_percent": 26.92428407671888,

          "avg_profit_per_trade_usd": -2.275967352724774e-10

        },

        "pricing": {

          "current_price": 204.09378209627866,

          "avg_buy_cost": 160.79963229984938,

          "avg_sell_cost": 160.6858339322126

        }

      },

      "pumpsAkNcb1nZs89Uees3DyRzUGxjqThuzF3A8LVVfn": {

        "symbol": "PUMP",

        "decimals": 9,

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
` `

