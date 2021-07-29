## Concepts and Utilities

Lending pools power and rebalance the leverage for the "Bull" and "Bear" tokens.

For Bull tokens, a stablecoin pool is created. The single pool can lend assets to bull token contracts with different underlying assets. For example, the BTCBULL (3x) token and ETHBULL (3x) token share the same stablecoin pool. When new bull tokens are minted or rebalanced, borrowing and lending transactions take place within the protocols.

For Bear tokens, separate pools with underlying assets are created to power different tokens. For example, the BTCBEAR (3x) tokens will borrow WBTC and sell to take short positions on the market, therefore, a WBTC pool provides the necessary leverages when minting or rebalancing.

In the PPLT v1.0, the standard interest rate is fixed, provided that the lending pools are not fully utilized. Interest is collected periodically from the leveraged tokens, distributed to and shared by all pool participants automatically.


## Pool Shares

Similar to most pooled models in DeFi, the shares of the PPLT lending pools are tokenized as PPT, standing for “Phoenix Pool Token”. 

PPLT lending pools are created when individual liquidity providers contribute liquidity by staking their crypto assets in the pool. The liquidity providers receive a pool token - the PPT - which represents their share of ownership in the pool. 

In the PPLT v1.0’s lending pools, Interest is not distributed; instead, users earn interest simply by holding PPT. Over time, each PPT becomes convertible into an increasing amount of the asset, even while the number of PPTs in a wallet stays the same.


## Pool Net Value and FPT Value
### What Is Pool Net Value?
The Pool Net Value measures the monetary value of all assets and the outstanding lending amount currently in the lending pool. The Pool Net Value is also regarded as the Total Value Locked (TVL) in the lending pools. 

### What Affects Pool Net Value?
Let us take the ETH pool for example. The total Pool Net Value (PNV) in USD is affected by the following factors:

1)	ETH deposits increase the PNV;
2)	ETH withdrawals decrease the PNV;
3)	Receiving interest from lending assets to leveraged tokens increases the PNV;
4)	Changes in the USD value of ETH increase or decrease the PNV.

### PPT Value
After a user deposits crypto assets into the pool, assets are collateralized, and the holders are entitled to the benefits of having a fraction of the lending pool. PPT is minted and delivered to the users, representing a pro-rata share of the pools.

The net value of PPT is calculated using the Pool Net Value (as defined above) and dividing it by the total number of PPT tokens.

Net Value of FPT = Pool Net Value / No. of FPT

Due to the no-loss characteristics of the lending pools, the PPT value will be ever-increasing, if measured in pooled assets. Specifically, the PPT value of the USDC pool is ever-increasing measured in USDC, and the PPT value of the ETH pool is ever-increasing when measured in ETH.

## Basic Interest
Participants in the lending pools can earn interest from lending, which powers the tokens’ leveraged position. Interest is collected and distributed in the pool automatically through smart contracts, which leads to an increase in the PPT value over time, measured in terms of pooled assets.

Unlike most DeFi borrowing and lending protocols, the basic interest rate for borrowing and lending activities is a fixed amount in PPLT v1.0. For the borrowers, the borrowing rate is fixed and not subjected to changes, provided that the pool is not fully occupied.

For lenders, the higher the utilization rate of the pool, which means the larger proportion of the pooled assets is involved in lending, the higher APY the pool will have.


## Interest Adjustment Mechanism

When the lending pools are fully occupied, it is possible the targeted leverage level cannot be achieved when rebalancing, due to a lack of funds to borrow from the pools. In this case, the rebalancing could temporarily fail.

To address this issue, in order to incentivize more contributors to join the specific lending pool that is fully utilized, the interest rate for borrowing and lending will be temporarily increased, which in turn will attract lenders. If the pool is still not big enough to cover the amount needed for the tokens’ rebalancing, the interest will be further increased, until the targeted leverage level is reached.

Once the targeted leverage is reached, the rate will move back to the basic interest level.

