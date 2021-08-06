## PPLT

PPLT stands for Phoenix Protocol for Leveraged Tokens. It is one of the main products of Phoenix.

PPLT provides a decentralized way for creating and trading decentralized leveraged tokens on cryptoassets, like BTC, ETH, etc., on different chains. These leveraged tokens are powered by no-loss lending pools, where participants can earn interest. All the core functions of token minting, redeeming, taking leverages, borrowing and lending occur on-chain and are managed by smart contracts. It is a permissionless, censorship-resistant, and non-custodial protocol.

## Leveraged Tokens

Leveraged tokens are derivatives giving holders leveraged exposure to cryptocurrency markets, without having to worry about actively managing a leveraged position.For example, the ETHBULL/USD — also known as 3X Long Ethereum Token — is an ERC-20 token with a return that corresponds to three times the daily return of ETH. For every 1% ETH that goes up in a day, ETHBULL rises by 3%.

Leveraged tokens usually offer fixed leverages or leverage ranges through rebalancing mechanisms that maintain the target leverages.

## Rebalancing
Rebalancing is the mechanism that keeps the leverage at the targeted level. By rebalancing, the leveraged token will automatically re-leverage in profit and deleverage in loss to restore its target leverage level.

## Scheduled Rebalancing
Phoenix leveraged tokens "rebalance" themselves periodically, so they can keep the target leverage. At every rebalancing occasions, each leveraged token reinvests profits if making any, and if losing money, sells off part of its position to lower the leverage to avoid liquidation.

## Temporary Rebalancing
A temporary rebalancing may be needed when an unfavorable price movement occurs, especially if this happens in a short period of time.

For example, for ETHBULL (3x) tokens, if the ETH price were to drop by over 33%, the token value would go ‘negative" — something akin to getting liquidated. In such cases, the rebalancing mechanism needs to be triggered to deleverage the tokens, even if the time for a scheduled rebalancing has not yet arrived.

## Subscription and Minting
When users buy/subscribe for Phoenix leveraged tokens, the same number of tokens is minted by smart contracts. A series of transactions take place upon the receipt of the consideration, priced in stablecoins or the underlying assets.


## Redemption
In the PPLT v1.0, when the Phoenix leveraged tokens are "sold" on the market, they are actually redeemed, which also triggers a series of transactions. The same number of leveraged tokens is burnt, and the purchasing transactions are reversed, with the remaining balance paid back to the holders.

## Lending Pools
Lending pools power and rebalance the leverage for the "Bull" and "Bear" tokens.

For Bull tokens, a stablecoin pool is created. The single pool can lend assets to bull token contracts with different underlying assets. For Bear tokens, separate pools with underlying assets are created to power different tokens.

## Pool Shares
Similar to most pooled models in DeFi, the shares of the PPLT lending pools are tokenized as PPT, standing for “Phoenix Pool Token”.

PPLT lending pools are created when individual liquidity providers contribute liquidity by staking their crypto assets in the pool. The liquidity providers receive a pool token - the PPT - which represents their share of ownership in the pool.

## Basic Interest
Unlike most DeFi borrowing and lending protocols, the basic interest rate for borrowing and lending activities is a fixed amount in PPLT v1.0. For the borrowers, the borrowing rate is fixed and not subjected to changes, provided that the pool is not fully occupied.

For lenders, the higher the utilization rate of the pool, which means the larger proportion of the pooled assets is involved in lending, the higher APY the pool will have.

## Interest Adjustment Mechanism
When the lending pools are fully occupied, it is possible the targeted leverage level cannot be achieved when rebalancing, due to a lack of funds to borrow from the pools. In order to incentivize more contributors to join the specific lending pool that is fully utilized, the interest rate for borrowing and lending will be temporarily increased, which in turn will attract lenders. 