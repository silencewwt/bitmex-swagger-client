# bitmex_swagger
## REST API for the BitMEX Trading Platform  [View Changelog](/app/apiChangelog)  ----  #### Getting Started  Base URI: [https://www.bitmex.com/api/v1](/api/v1)  ##### Fetching Data  All REST endpoints are documented below. You can try out any query right from this interface.  Most table queries accept `count`, `start`, and `reverse` params. Set `reverse=true` to get rows newest-first.  Additional documentation regarding filters, timestamps, and authentication is available in [the main API documentation](/app/restAPI).  *All* table data is available via the [Websocket](/app/wsAPI). We highly recommend using the socket if you want to have the quickest possible data without being subject to ratelimits.  ##### Return Types  By default, all data is returned as JSON. Send `?_format=csv` to get CSV data or `?_format=xml` to get XML data.  ##### Trade Data Queries  *This is only a small subset of what is available, to get you started.*  Fill in the parameters and click the `Try it out!` button to try any of these queries.  * [Pricing Data](#!/Quote/Quote_get)  * [Trade Data](#!/Trade/Trade_get)  * [OrderBook Data](#!/OrderBook/OrderBook_getL2)  * [Settlement Data](#!/Settlement/Settlement_get)  * [Exchange Statistics](#!/Stats/Stats_history)  Every function of the BitMEX.com platform is exposed here and documented. Many more functions are available.  ##### Swagger Specification  [⇩ Download Swagger JSON](swagger.json)  ----  ## All API Endpoints  Click to expand a section. 

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.2.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import bitmex_swagger 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import bitmex_swagger
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import bitmex_swagger
from bitmex_swagger.rest import ApiException
from pprint import pprint

# Configure API key authorization: apiKey
bitmex_swagger.configuration.api_key['api-key'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# bitmex_swagger.configuration.api_key_prefix['api-key'] = 'Bearer'
# Configure API key authorization: apiNonce
bitmex_swagger.configuration.api_key['api-nonce'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# bitmex_swagger.configuration.api_key_prefix['api-nonce'] = 'Bearer'
# Configure API key authorization: apiSignature
bitmex_swagger.configuration.api_key['api-signature'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# bitmex_swagger.configuration.api_key_prefix['api-signature'] = 'Bearer'
# create an instance of the API class
api_instance = bitmex_swagger.APIKeyApi()
api_key_id = 'api_key_id_example' # str | API Key ID (public component).

try:
    # Disable an API Key.
    api_response = api_instance.a_pi_key_disable(api_key_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling APIKeyApi->a_pi_key_disable: %s\n" % e)

```

## Documentation for API Endpoints

All URIs are relative to *https://localhost/api/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIKeyApi* | [**a_pi_key_disable**](docs/APIKeyApi.md#a_pi_key_disable) | **POST** /apiKey/disable | Disable an API Key.
*APIKeyApi* | [**a_pi_key_enable**](docs/APIKeyApi.md#a_pi_key_enable) | **POST** /apiKey/enable | Enable an API Key.
*APIKeyApi* | [**a_pi_key_get**](docs/APIKeyApi.md#a_pi_key_get) | **GET** /apiKey | Get your API Keys.
*APIKeyApi* | [**a_pi_key_new**](docs/APIKeyApi.md#a_pi_key_new) | **POST** /apiKey | Create a new API Key.
*APIKeyApi* | [**a_pi_key_remove**](docs/APIKeyApi.md#a_pi_key_remove) | **DELETE** /apiKey | Remove an API Key.
*AnnouncementApi* | [**announcement_get**](docs/AnnouncementApi.md#announcement_get) | **GET** /announcement | Get site announcements.
*AnnouncementApi* | [**announcement_get_urgent**](docs/AnnouncementApi.md#announcement_get_urgent) | **GET** /announcement/urgent | Get urgent (banner) announcements.
*ChatApi* | [**chat_get**](docs/ChatApi.md#chat_get) | **GET** /chat | Get chat messages.
*ChatApi* | [**chat_get_channels**](docs/ChatApi.md#chat_get_channels) | **GET** /chat/channels | Get available channels.
*ChatApi* | [**chat_get_connected**](docs/ChatApi.md#chat_get_connected) | **GET** /chat/connected | Get connected users.
*ChatApi* | [**chat_new**](docs/ChatApi.md#chat_new) | **POST** /chat | Send a chat message.
*ExecutionApi* | [**execution_get**](docs/ExecutionApi.md#execution_get) | **GET** /execution | Get all raw executions for your account.
*ExecutionApi* | [**execution_get_trade_history**](docs/ExecutionApi.md#execution_get_trade_history) | **GET** /execution/tradeHistory | Get all balance-affecting executions. This includes each trade, insurance charge, and settlement.
*FundingApi* | [**funding_get**](docs/FundingApi.md#funding_get) | **GET** /funding | Get funding history.
*InstrumentApi* | [**instrument_get**](docs/InstrumentApi.md#instrument_get) | **GET** /instrument | Get instruments.
*InstrumentApi* | [**instrument_get_active**](docs/InstrumentApi.md#instrument_get_active) | **GET** /instrument/active | Get all active instruments and instruments that have expired in &lt;24hrs.
*InstrumentApi* | [**instrument_get_active_and_indices**](docs/InstrumentApi.md#instrument_get_active_and_indices) | **GET** /instrument/activeAndIndices | Helper method. Gets all active instruments and all indices. This is a join of the result of /indices and /active.
*InstrumentApi* | [**instrument_get_active_intervals**](docs/InstrumentApi.md#instrument_get_active_intervals) | **GET** /instrument/activeIntervals | Return all active contract series and interval pairs.
*InstrumentApi* | [**instrument_get_composite_index**](docs/InstrumentApi.md#instrument_get_composite_index) | **GET** /instrument/compositeIndex | Show constituent parts of an index.
*InstrumentApi* | [**instrument_get_indices**](docs/InstrumentApi.md#instrument_get_indices) | **GET** /instrument/indices | Get all price indices.
*InsuranceApi* | [**insurance_get**](docs/InsuranceApi.md#insurance_get) | **GET** /insurance | Get insurance fund history.
*LeaderboardApi* | [**leaderboard_get**](docs/LeaderboardApi.md#leaderboard_get) | **GET** /leaderboard | Get current leaderboard.
*LeaderboardApi* | [**leaderboard_get_name**](docs/LeaderboardApi.md#leaderboard_get_name) | **GET** /leaderboard/name | Get your alias on the leaderboard.
*LiquidationApi* | [**liquidation_get**](docs/LiquidationApi.md#liquidation_get) | **GET** /liquidation | Get liquidation orders.
*NotificationApi* | [**notification_get**](docs/NotificationApi.md#notification_get) | **GET** /notification | Get your current notifications.
*OrderApi* | [**order_amend**](docs/OrderApi.md#order_amend) | **PUT** /order | Amend the quantity or price of an open order.
*OrderApi* | [**order_amend_bulk**](docs/OrderApi.md#order_amend_bulk) | **PUT** /order/bulk | Amend multiple orders for the same symbol.
*OrderApi* | [**order_cancel**](docs/OrderApi.md#order_cancel) | **DELETE** /order | Cancel order(s). Send multiple order IDs to cancel in bulk.
*OrderApi* | [**order_cancel_all**](docs/OrderApi.md#order_cancel_all) | **DELETE** /order/all | Cancels all of your orders.
*OrderApi* | [**order_cancel_all_after**](docs/OrderApi.md#order_cancel_all_after) | **POST** /order/cancelAllAfter | Automatically cancel all your orders after a specified timeout.
*OrderApi* | [**order_close_position**](docs/OrderApi.md#order_close_position) | **POST** /order/closePosition | Close a position. [Deprecated, use POST /order with execInst: &#39;Close&#39;]
*OrderApi* | [**order_get_orders**](docs/OrderApi.md#order_get_orders) | **GET** /order | Get your orders.
*OrderApi* | [**order_new**](docs/OrderApi.md#order_new) | **POST** /order | Create a new order.
*OrderApi* | [**order_new_bulk**](docs/OrderApi.md#order_new_bulk) | **POST** /order/bulk | Create multiple new orders for the same symbol.
*OrderBookApi* | [**order_book_get_l2**](docs/OrderBookApi.md#order_book_get_l2) | **GET** /orderBook/L2 | Get current orderbook in vertical format.
*PositionApi* | [**position_get**](docs/PositionApi.md#position_get) | **GET** /position | Get your positions.
*PositionApi* | [**position_isolate_margin**](docs/PositionApi.md#position_isolate_margin) | **POST** /position/isolate | Enable isolated margin or cross margin per-position.
*PositionApi* | [**position_transfer_isolated_margin**](docs/PositionApi.md#position_transfer_isolated_margin) | **POST** /position/transferMargin | Transfer equity in or out of a position.
*PositionApi* | [**position_update_leverage**](docs/PositionApi.md#position_update_leverage) | **POST** /position/leverage | Choose leverage for a position.
*PositionApi* | [**position_update_risk_limit**](docs/PositionApi.md#position_update_risk_limit) | **POST** /position/riskLimit | Update your risk limit.
*QuoteApi* | [**quote_get**](docs/QuoteApi.md#quote_get) | **GET** /quote | Get Quotes.
*QuoteApi* | [**quote_get_bucketed**](docs/QuoteApi.md#quote_get_bucketed) | **GET** /quote/bucketed | Get previous quotes in time buckets.
*SchemaApi* | [**schema_get**](docs/SchemaApi.md#schema_get) | **GET** /schema | Get model schemata for data objects returned by this API.
*SchemaApi* | [**schema_websocket_help**](docs/SchemaApi.md#schema_websocket_help) | **GET** /schema/websocketHelp | Returns help text &amp; subject list for websocket usage.
*SettlementApi* | [**settlement_get**](docs/SettlementApi.md#settlement_get) | **GET** /settlement | Get settlement history.
*StatsApi* | [**stats_get**](docs/StatsApi.md#stats_get) | **GET** /stats | Get exchange-wide and per-series turnover and volume statistics.
*StatsApi* | [**stats_history**](docs/StatsApi.md#stats_history) | **GET** /stats/history | Get historical exchange-wide and per-series turnover and volume statistics.
*StatsApi* | [**stats_history_usd**](docs/StatsApi.md#stats_history_usd) | **GET** /stats/historyUSD | Get a summary of exchange statistics in USD.
*TradeApi* | [**trade_get**](docs/TradeApi.md#trade_get) | **GET** /trade | Get Trades.
*TradeApi* | [**trade_get_bucketed**](docs/TradeApi.md#trade_get_bucketed) | **GET** /trade/bucketed | Get previous trades in time buckets.
*UserApi* | [**user_cancel_withdrawal**](docs/UserApi.md#user_cancel_withdrawal) | **POST** /user/cancelWithdrawal | Cancel a withdrawal.
*UserApi* | [**user_check_referral_code**](docs/UserApi.md#user_check_referral_code) | **GET** /user/checkReferralCode | Check if a referral code is valid.
*UserApi* | [**user_confirm**](docs/UserApi.md#user_confirm) | **POST** /user/confirmEmail | Confirm your email address with a token.
*UserApi* | [**user_confirm_enable_tfa**](docs/UserApi.md#user_confirm_enable_tfa) | **POST** /user/confirmEnableTFA | Confirm two-factor auth for this account. If using a Yubikey, simply send a token to this endpoint.
*UserApi* | [**user_confirm_withdrawal**](docs/UserApi.md#user_confirm_withdrawal) | **POST** /user/confirmWithdrawal | Confirm a withdrawal.
*UserApi* | [**user_disable_tfa**](docs/UserApi.md#user_disable_tfa) | **POST** /user/disableTFA | Disable two-factor auth for this account.
*UserApi* | [**user_get**](docs/UserApi.md#user_get) | **GET** /user | Get your user model.
*UserApi* | [**user_get_affiliate_status**](docs/UserApi.md#user_get_affiliate_status) | **GET** /user/affiliateStatus | Get your current affiliate/referral status.
*UserApi* | [**user_get_commission**](docs/UserApi.md#user_get_commission) | **GET** /user/commission | Get your account&#39;s commission status.
*UserApi* | [**user_get_deposit_address**](docs/UserApi.md#user_get_deposit_address) | **GET** /user/depositAddress | Get a deposit address.
*UserApi* | [**user_get_margin**](docs/UserApi.md#user_get_margin) | **GET** /user/margin | Get your account&#39;s margin status. Send a currency of \&quot;all\&quot; to receive an array of all supported currencies.
*UserApi* | [**user_get_wallet**](docs/UserApi.md#user_get_wallet) | **GET** /user/wallet | Get your current wallet information.
*UserApi* | [**user_get_wallet_history**](docs/UserApi.md#user_get_wallet_history) | **GET** /user/walletHistory | Get a history of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | [**user_get_wallet_summary**](docs/UserApi.md#user_get_wallet_summary) | **GET** /user/walletSummary | Get a summary of all of your wallet transactions (deposits, withdrawals, PNL).
*UserApi* | [**user_logout**](docs/UserApi.md#user_logout) | **POST** /user/logout | Log out of BitMEX.
*UserApi* | [**user_logout_all**](docs/UserApi.md#user_logout_all) | **POST** /user/logoutAll | Log all systems out of BitMEX. This will revoke all of your account&#39;s access tokens, logging you out on all devices.
*UserApi* | [**user_min_withdrawal_fee**](docs/UserApi.md#user_min_withdrawal_fee) | **GET** /user/minWithdrawalFee | Get the minimum withdrawal fee for a currency.
*UserApi* | [**user_request_enable_tfa**](docs/UserApi.md#user_request_enable_tfa) | **POST** /user/requestEnableTFA | Get secret key for setting up two-factor auth.
*UserApi* | [**user_request_withdrawal**](docs/UserApi.md#user_request_withdrawal) | **POST** /user/requestWithdrawal | Request a withdrawal to an external wallet.
*UserApi* | [**user_save_preferences**](docs/UserApi.md#user_save_preferences) | **POST** /user/preferences | Save user preferences.
*UserApi* | [**user_update**](docs/UserApi.md#user_update) | **PUT** /user | Update your password, name, and other attributes.


## Documentation For Models

 - [APIKey](docs/APIKey.md)
 - [AccessToken](docs/AccessToken.md)
 - [Affiliate](docs/Affiliate.md)
 - [Announcement](docs/Announcement.md)
 - [Chat](docs/Chat.md)
 - [ChatChannel](docs/ChatChannel.md)
 - [ConnectedUsers](docs/ConnectedUsers.md)
 - [Error](docs/Error.md)
 - [ErrorError](docs/ErrorError.md)
 - [Execution](docs/Execution.md)
 - [Funding](docs/Funding.md)
 - [IndexComposite](docs/IndexComposite.md)
 - [InlineResponse200](docs/InlineResponse200.md)
 - [InlineResponse2001](docs/InlineResponse2001.md)
 - [Instrument](docs/Instrument.md)
 - [InstrumentInterval](docs/InstrumentInterval.md)
 - [Insurance](docs/Insurance.md)
 - [Leaderboard](docs/Leaderboard.md)
 - [Liquidation](docs/Liquidation.md)
 - [Margin](docs/Margin.md)
 - [Notification](docs/Notification.md)
 - [Order](docs/Order.md)
 - [OrderBookL2](docs/OrderBookL2.md)
 - [Position](docs/Position.md)
 - [Quote](docs/Quote.md)
 - [Settlement](docs/Settlement.md)
 - [Stats](docs/Stats.md)
 - [StatsHistory](docs/StatsHistory.md)
 - [StatsUSD](docs/StatsUSD.md)
 - [Trade](docs/Trade.md)
 - [TradeBin](docs/TradeBin.md)
 - [Transaction](docs/Transaction.md)
 - [User](docs/User.md)
 - [UserCommission](docs/UserCommission.md)
 - [UserPreferences](docs/UserPreferences.md)
 - [Wallet](docs/Wallet.md)
 - [XAny](docs/XAny.md)


## Documentation For Authorization


## apiKey

- **Type**: API key
- **API key parameter name**: api-key
- **Location**: HTTP header

## apiNonce

- **Type**: API key
- **API key parameter name**: api-nonce
- **Location**: HTTP header

## apiSignature

- **Type**: API key
- **API key parameter name**: api-signature
- **Location**: HTTP header


## Author

support@bitmex.com

