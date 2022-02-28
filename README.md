# decentralized-exchange
Dapp for trading tokens

This is the source code for a decentralized exchange for trading ERC20 tokens, namely DAI, DEX, BAT, REP, and ZRX. 

This decentralized exchange connects to a user's Metamask wallet, and the user can send DAI token to the exchange.

The user can select the token they want to trade using a dropdown menu.

The user can then place buy or sell limit or market orders, specifying the token and amount of the order. 

An orderbook lists all open limit orders, matches incoming market orders against existing limit orders, and removes limit orders that were executed.

The orderbook follows a price-time algorithm. When an incoming market order arrives, the orderbook will match it with the limit order that has the best price. If several limit orders have the same price, the one that was created first will be executed.

If the amount of the market order is less than the limit order, then the market order will be fully executed while the limit order will be only partially executed with the rest remaining in the orderbook.

If the amount of the market order exceeds the limit order, the limit order will be fully executed, and the orderbook will try to match the remaining order with other limit orders. 

When a market and limit order have been matched, the tokens are transferred from the seller to the buyer, while Ether is transferred from the buyer to the seller.

The image Dex_DAI.png shows the exchange at startup. Dex_BAT1.png and Dex_BAT2.png show the exchange after the user has selected to trade the BAT token. The exchange lists the user's token balance, charts prior trades of that token on the exchange, allows the user to transfer or trade tokens, and lists open orders on the exchange by all users as well as the current user.


