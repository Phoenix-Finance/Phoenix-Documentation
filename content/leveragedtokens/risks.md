## Price slippage in purchasing and rebalancing
When FinNexus leveraged tokens are minted, due to them being backed by assets, a series of transactions need to take place with decentralized exchanges. Similarly, during rebalancing, necessary transactions need to be triggered in order to maintain the targeted leverage level.

There can be price slippage when making these transactions, and the degree of slippage depends on the depth of the market liquidity in the trading pairs and the volume of the transaction. Larger orders in purchase or redemption, and a greater amount of transactions when rebalancing may lead to a higher price slippage, thus having a negative influence on financial performance.

The FPLT v1.0 will try to integrate dex aggregators like 1inch, who can find the best route among multiple Dexes, to minimize the slippage involved in a single transaction. Moreover, the protocol can choose to split the transactions in a number of smaller orders to lower slippages in a single trade.
## Risks associated with maintaining leverages
The fact that leveraged tokens maintain their leverage exposure to a fixed level may lead to financial performances not expected by the holders, especially compared with margin trading. From this perspective, please remember that leveraged tokens are commonly regarded as an instrument to trade rather than hold.

This is because when bull leveraged tokens have gains, they will borrow and reinvest to increase their long positions. And if bear leveraged tokens have gains, they will borrow and sell more to increase their short positions.

Let us compare ETHBULL (3x) with trading a 3x ETH position on margin: if ETH goes up one day and then up again the next, ETHBULL will do better than a standard margin position, because it will have reinvested the profits from the first day back into ETH. However, if ETH goes up and then falls back down, ETHBULL will do worse, because the reinvestment during rebalancing increased the exposure, compared with margin trading.

So it is possible that even if the underlier’s price increases, the leveraged token’s net value drops. As shown in the table below, though over two days the price of ETH rises from $2000 to $2024, the value of leveraged tokens decreases, due to the re-leveraging on day 1.
|Time|ETH Price($)|ETH Price Change|Leveraged Token($|Margin Trading($)|
| --- | --- | --- | --- | --- |
|Day0|2000||2000|2000|
|Day1|2200|10%|2600|2600|
|Day2|2024|-8%|1976|2072|
## Risks associated with transaction failure
Dexes run on public chains and there may be unexpected scenarios leading to transaction failure, like network conjunctions, volatile price movement or temporary platform misfunction. Collaboration of protocols may lead to composability of risks. If this failure happens, it may in turn cause a rebalancing failure, making the protocol unable to maintain the targeted leverage. In extreme cases, if the market makes a dramatic unfavorable movement, it can lead a value loss in the lending pool, due to the negative value in leveraged tokens.
## Smart contract risks
The audit process of Fthe PLT v1.0 is still in progress. The whole DeFi ecosystem is still in the early and experimenting stage. Please always be alert to possible smart contract risks and only invest what you can afford to lose.
## Oracle risks
FinNexus has partnered with Chainlink, the leading decentralized blockchain data provider, to bring off-chain data to smart contracts on Ethereum and other blockchains. The FPLT v1.0 applies decentralized price feeds covering cryptoasset pairs provided by ChainLink.

Chainlink is a decentralized oracle network that enables smart contracts to securely access off-chain data feeds, web APIs, and traditional bank payments. It is well known for providing highly secure and reliable oracles.

Nevertheless, oracles and external price data aggregation can be considered as a potential risk to the stability of the FPLT.
