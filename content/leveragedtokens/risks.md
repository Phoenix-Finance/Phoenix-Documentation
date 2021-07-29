## Price slippage and transaction fees in purchasing and rebalancing
When Phoenix leveraged tokens are minted, as they are backed by assets, a series of transactions need to take place with decentralized exchanges. Similarly, during rebalancing, transactions need to be triggered in order to maintain the targeted leverage level.

Traders may face price slippage and transaction fees when making these transactions, with the degree of slippage and transaction costs depending on the depth of the market liquidity in the trading pairs and the volume of the transaction. Larger orders when purchasing or redeeming, and a greater volume of transactions when rebalancing may lead to a higher price slippage and transaction costs, thus having a negative influence on the tokens’ financial performance.

## Risks associated with maintaining leverages
The fact that leveraged tokens maintain their leverage exposure to a fixed level or range may lead to unexpected outcomes, especially compared with margin trading. (From this perspective, please remember that leveraged tokens are commonly regarded as an instrument to trade rather than hold.)

This is because when bull leveraged tokens have gains, they will borrow and reinvest to increase their long positions. And if bear leveraged tokens have gains, they will borrow and sell more to increase their short positions.

A practical example will help clarify how the behavior of leveraged tokens differs from standard leveraged trading. Let us compare ETHBULL (3x) with trading a 3x ETH position on margin. If ETH goes up one day and then up again the next, ETHBULL will do better than a standard margin position, because it will have reinvested the profits from the first day back into ETH. However, if ETH goes up and then falls back down, ETHBULL will do worse, because the reinvestment during rebalancing increased the exposure, compared with margin trading.

Therefore, it is possible that even if the underlier’s price increases, the leveraged token’s net value drops. As shown in the table below, even though over two days the price of ETH rises from $2000 to $2024, the value of leveraged tokens decreases, due to the re-leveraging on day 1.

|Time|ETH Price ($)|ETH Price Change|Leveraged Token ($)|Margin Trading ($)|
|---|---|---|---|---|
|Day 0|2000||2000|2000|
|Day 1|2200|10%|2600|2600|
|Day 2|2024|-8%|1976|2072|

## Risks associated with transaction failure
Dexes run on public chains and there may be unexpected scenarios leading to transactions failure, like network conjunctions, volatile price movement or platform misfunction. Collaboration of protocols may lead to the composability of risks. This may in turn cause a rebalancing failure, making the protocol unable to maintain the targeted leverage. In extreme cases, if the market makes a dramatic unfavorable movement, the lending pool may suffer a value loss due to the negative value in leveraged tokens.
## Smart contract risks
The whole DeFi ecosystem is still in an early experimenting stage. Please always be alert to possible smart contract risks and only invest what you can afford to lose.
## Oracle risks
Phoenix has partnered with Chainlink, the leading decentralized blockchain data provider, to bring off-chain data to smart contracts on Ethereum and other blockchains. The PPLT v1.0 applies decentralized price feeds covering cryptoasset pairs provided by Chainlink.

Chainlink is a decentralized oracle network that enables smart contracts to securely access off-chain data feeds, web APIs, and traditional bank payments. It is well known for providing highly secure and reliable oracles.

Nevertheless, oracles and external price data aggregation can be considered as a potential risk to the stability of the PPLT if any unforeseen issue arises.

