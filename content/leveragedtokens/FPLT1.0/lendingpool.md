## Concepts and Utilities

Lending pools power and rebalance the leverage for the "Bull" and "Bear" tokens.

For Bull tokens, a stablecoin pool is created. The single pool can lend assets to Bull tokens with different underlying assets. For example, the BTCBULL (3x) token and ETHBULL (3x) token may share the same stablecoin pool. When new bull tokens are minted or rebalanced, borrowing and lending transactions take place within the protocols.

For Bear tokens, separate pools with underlying assets are created to power different tokens. For example, the BTCBEAR (3x) tokens will borrow WBTC and sell to take short positions on the market, therefore, they need a WBTC pool for providing the necessary leverages when minting or rebalancing.

The lending pool participants can lend their tokens and earn a higher lending interest rate than would be the case with normal borrowing and lending protocols.

In the FPLT v1.0, the standard interest rate is fixed, provided that the lending pools are not fully utilized. Interest is collected periodically from the leveraged tokens, distributed to and shared by all pool participants automatically.

## Pool Shares

Similar to most pooled models in DeFi, the shares of the lending pools are tokenized as FPT, standing for “FinNexus Pool Token”. 

FPLT lending pools are created when individual liquidity providers contribute liquidity by locking their crypto assets in the pool. The liquidity provider receives a pool token - the FPT - which represents their share of ownership in the pool. 

In this sense, the mechanism resembles Compound’s cTokens. In the FPLT v1.0’s lending pools, Interest is not distributed; instead, simply by holding FPT, you'll earn interest. Over time, each FPT becomes convertible into an increasing amount of the asset, even while the number of FPT in your wallet stays the same.

## Pool Net Value and FPT Value
### What Is Pool Net Value?
The Pool Net Value measures the monetary value of all assets and outstanding lending amount currently in the lending pool. The Pool Net Value is also regarded as the Total Value Locked (TVL) in the pools. 
### What Affects Pool Net Value?
Let us take the ETH pool for example. 
The total Pool Net Value (PNV) in USD is affected by the following factors:
ETH deposits increase the PNV;
ETH withdrawals decrease the PNV;
Receiving interest from lending assets to leveraged tokens increases the PNV;
The change in the USD value of ETH increases or decreases PNV.
### FPT Value
After a user deposits cryptoaasets into the pool, the assets will be collateralized and the holders will be entitled to the benefits of having a fraction of the lending pool. FPT will be minted and delivered to the users, to represent the pro-rata share in the pools.

The net value of FPT is calculated using the Pool Net Value (as defined above) and dividing it by the total number of FPT tokens.

Net Value of FPT = Pool Net Value / No. of FPT

Due to the no-loss characteristics in the lending pools, the FPT value will be ever-increasing, if measured in the pooled assets. Specifically, the FPT value of the USDC pool is ever-increasing measured in USDC, and the FPT value of the ETH pool is ever-increasing measured in ETH.

## Basic Interest
Participants in the lending pools can earn interest from lending, which powers the tokens’ leveraged position. Interest is collected and distributed in the pool automatically by smart contracts, which leads to an increase in the FPT value over time, measured in terms of pooled assets.

Unlike most DeFi borrowing and lending protocols, the basic interest rate for borrowing and lending activities is a fixed amount. For the borrowers, meaning the leveraged token protocol itself, the borrowing rate is fixed and not subjected to changes even if the need grows, provided that the pool is not fully occupied.

For lenders, the higher the utilization rate of the pool, which means the larger proportion of the pooled assets are participating in the lending activities, the higher APY the pool will have.

## Interest Adjustment Mechanism

In cases when the lending pools are fully occupied, it is possible that in the rebalancing process as mentioned below, the targeted leverage level cannot be achieved, due to a lack of funds to borrow from the pools. In this case, the rebalancing could temporarily fail.

In these cases, in order to incentivize more contributors to join the lending pool, the interest rate for borrowing and lending will be temporarily increased, which in turn will attract lenders. If the pool is still not big enough to cover the amount needed for the tokens’ rebalancing, the interest will be further increased, until the targeted leverage level is fully reached.

Once the targeted leverage, the rate will move back to the basic interest level.
