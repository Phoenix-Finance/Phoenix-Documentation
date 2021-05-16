## What Are Leveraged Tokens?

Leveraged tokens are derivatives giving holders leveraged exposure to cryptocurrency markets, without having to worry about actively managing a leveraged position. They were initially introduced by derivatives exchange FTX, and have since been listed on other centralized exchanges.

For example, the ETHBULL/USD — also known as 3X Long Ethereum Token — is an ERC-20 token with a return that corresponds to three times the daily return of ETH. For every 1% ETH that goes up in a day, ETHBULL rises by 3%.

Leveraged tokens usually offer fixed leverages or leverage ranges through rebalancing mechanisms that maintain the target leverages.

## Rebalancing
![](https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.bringyourfinancestolife.com%2F2017%2F03%2Fwhy-your-portfolio-may-be-overdue-for-a-rebalance%2F&psig=AOvVaw2IfhWGA_aTYAjB_vIz8TjJ&ust=1621245043162000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCKDbu8r2zfACFQAAAAAdAAAAABAD)

Rebalancing is a very important element in the design of leveraged tokens, for it is the mechanism that keeps the leverage at the targeted level. 

Let us take a look at how rebalancing works with an example.

You are holding $100 USDC and purchase an ETHBULL (3x) leveraged token. The protocol will automatically borrow $200 in USDC and trade them for $200 ETH.

‍Suppose the price of ETH increases by 20% and the ETHBULL (3x) token price rises to $300*(1+20%)-$200=$160 before rebalancing. Now, your real leverage becomes 2.25 ($360/$160), lower than the targeted leverage.

‍As part of the rebalancing process, the protocol will borrow more USDC and purchase extra ETH tokens to shift the leverage back to 3x. In our example, it will borrow another $120 and exchange it for ETH. The total leverage thus becomes ($360+$120)/$160=3x again.

Suppose the price of ETH decreases by 20%, and the ETHBULL (3x) token price decreases to $300*(1-20%)-$200=$40 before rebalancing. Now, your real leverage would become six ($240/$40), higher than the targeted leverage.

In this case, it will sell ETH tokens and repay the outstanding debt to deleverage. In this example, it will sell $120 ETH for USD and pay back to the pool. The debt would become $80 and the total leverage would once again be ($240-$120)/$40=3x.

In other words, the leveraged token will automatically re-leverage in profit and deleverage in loss, to restore its targeted leverage level. If the mechanism works smoothly, even in unfavorable market trends, the leveraged token holders will never be liquidated, as the deleveraging mechanism will constantly lower the effective leverage level.
