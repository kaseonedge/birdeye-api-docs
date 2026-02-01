# Subscribing to Real-Time token new listing (SUBSCRIBE\_TOKEN\_NEW\_LISTING)   [Skip link to Subscribing to Real-Time token new listing (SUBSCRIBE_TOKEN_NEW_LISTING)](https://docs.birdeye.so/reference/new-token-listing\#subscribing-to-real-time-token-new-listing-subscribe_token_new_listing)

The "SUBSCRIBE\_TOKEN\_NEW\_LISTING" event allows you to receive real-time updates about new token listings. This subscription is useful for tracking new tokens being added on a requested blockchain.

The instructions for each type of objects are described below.

## WebSocket URL:   [Skip link to WebSocket URL:](https://docs.birdeye.so/reference/new-token-listing\#websocket-url)

```undefined
wss://public-api.birdeye.so/socket/solana?x-api-key=YOUR-API-KEY
```

### Header   [Skip link to Header](https://docs.birdeye.so/reference/new-token-listing\#header)

| Key | Value |
| --- | --- |
| `Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Origin` | ws://public-api.birdeye.so |
| `Sec-WebSocket-Protocol` | echo-protocol |

### Message   [Skip link to Message](https://docs.birdeye.so/reference/new-token-listing\#message)

JSON

```json
{
    "type": "SUBSCRIBE_TOKEN_NEW_LISTING"
}
```

Or:

JSON

```json
{
    "type": "SUBSCRIBE_TOKEN_NEW_LISTING",
    "meme_platform_enabled": true,
    "min_liquidity": 5000,
    "max_liquidity": 10000,
		"sources": ["pump_dot_fun", "meteora_dynamic_bonding_curve"],
}
```

**Key Notes:**

- The `min_liquidity` parameter is **optional** but user must set higher than system value which is `0`.
- The `max_liquidity` parameter is **optional** but must be higher than `min_volume` when provided.
- The `meme_platform_enabled` parameter is **optional**, value `true` means that you want to receive new meme token listing from meme platform such as pump.fun. If no message, it means no listing from meme platform.
- The `sources` parameter is **optional**, it enables filtering newly listed meme tokens based on their originating source.

### Output Example   [Skip link to Output Example](https://docs.birdeye.so/reference/new-token-listing\#output-example)

JSON

```json
{
    "type": "TOKEN_NEW_LISTING_DATA",
    "data": {
        "address": "BkQfwVktcbWmxePJN5weHWJZgReWbiz8gzTdFa2w7Uds",
        "decimals": 6,
        "name": "Worker Cat",
        "symbol": "$MCDCAT",
        "liquidity": "12120.155172280874",
        "liquidityAddedAt": 1720155863
    }
}
```

**Response Parameters:**

| Key | Data Type | Details | Example |
| --- | --- | --- | --- |
| `address` | string | The token address. | "BkQfwVktcbWmxePJN5weHWJZgReWbiz8gzTdFa2w7Uds" |
| `decimals` | integer | The number of decimal places for the token. | 6 |
| `name` | string | The name of the token. | "Worker Cat" |
| `symbol` | string | The symbol of the token. | "$MCDCAT" |
| `liquidity` | string | The current liquidity of the token. | "12120.155172280874" |
| `liquidityAddedAt` | integer | The Unix timestamp when liquidity was added. | 1720155863 |

**Supported meme sources:**

| Source | Value |
| --- | --- |
| RAYDIUM | raydium |
| RAYDIUM | raydium\_clamm |
| RAYDIUM | raydium\_cp |
| ORCA | orca |
| ALDRIN | aldrin |
| STEP | step |
| SAROS | saros |
| SAROS | saros\_dlmm |
| CROPPER | cropper |
| TESSERAV | tesserav |
| CROPPER | cropper\_dlmm |
| CREMA | crema |
| LIFINITY | lifinity |
| PANCAKESWAP | pancakeswap\_v3 |
| SABER | saber |
| SWAP | swap\_program |
| SENCHA | sencha |
| MERCURIAL | mercurial |
| SERUM | serum |
| OPENBOOK | openbook |
| HUMIDIFI | humidifi |
| OPENBOOK | openbook\_swap |
| SERUM | serum\_swap |
| PENGUIN | penguin |
| TOKEN | token |
| WHIRLPOOL | whirlpool |
| ONEMOON | onemoon |
| CYKURA | cykura |
| SWIM | swim |
| DOOAR | dooar |
| MARINADE | marinade |
| MANGO | mango |
| SYMMETRY | symmetry |
| METEORA | meteora |
| INVARIANT | invariant |
| MARCOPOLO | marcopolo |
| OASIS | oasis |
| GOOSEFX | goosefx |
| SOLANAX | solanax |
| DELTAFI | deltafi |
| DRADEX | dradex\_swap |
| CREMA | crema\_clamm |
| BALANSOL | balansol |
| JUPITER | jupiter\_limit\_order |
| JUPITER | jupiter\_dca |
| JUPITER | jupiter\_perp |
| FUSION | fusion\_amm |
| PHOENIX | phoenix |
| STAKE | stake\_pool |
| SOCEAN | socean |
| LIDO | lido |
| ZETA | zeta |
| BONKSWAP | bonkswap |
| LP | lp\_finance |
| FLUXBEAM | fluxbeam |
| SNOWFLAKE | snowflake |
| METEORA | meteora\_dlmm |
| TINY | tiny |
| DEXLAB | dexlab |
| SANCTUM | sanctum |
| OPENBOOK | openbook\_v2 |
| ONE | 1intro |
| GUACAMOLE | guacamole |
| CLONE | clone\_protocol |
| PUMP | pump\_dot\_fun |
| STABBLE | stabble |
| MANIFEST | manifest |
| JUPITERZ | jupiterz |
| MOONSHOT | moonshot |
| SOLFI | solfi |
| SOLFI\_V2 | solfi\_v2 |
| NUMERAIRE | numeraire |
| ZEROFI | zerofi |
| DAOSFUN | daosfun |
| SOLANAFUN | solanafun\_snapper |
| SOLANAFUN | solanafun\_fomo |
| PUMP | pump\_amm |
| VIRTUALS | virtuals\_io |
| SUPER | super\_exchange |
| METEORA | meteora\_damm\_v2 |
| METEORA | meteora\_virtual\_curve |
| RAYDIUM | raydium\_launchlab |
| METEORA | meteora\_dynamic\_bonding\_curve |
| PLASMA | plasma |
| VERTIGO | vertigo |
| WAVEBREAK | wavebreak |
| BYREAL | byreal |
| HEAVEN | heaven |
| UNISWAP | uniswap |
| KYBERSWAP | kyber |
| ONEINCH | oneinch |
| SUSHISWAP | sushiswap |
| BALANCER | balancer |
| BALANCER | balancerV2 |
| BALANCER | balancerV3 |
| TOKEN | token |
| PANCAKESWAP | pancakeswap |
| PANCAKE | pancakeStableSwap |
| DODO | dodoV2 |
| PANCAKESWAP | pancakeswapInfinityCLAMM |
| PANCAKESWAP | pancakeswapInfinityLBAMM |
| CURVE | Curve.fi |
| MAVERICK | maverickV2 |
| UNISWAPV | uniswapV4 |
| WOOFI | woofi |
| EKUBO | ekubo |
| ONDO | OndoFinance |
| FLUID | fluid |

* * *

* * *

StripeM-Inner
