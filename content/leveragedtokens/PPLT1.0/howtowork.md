### Tokenization of Leveraged Positions

As the name indicates, Phoenix tokenizes decentralized leveraged products into ERC-20 tokens. These tokens are fungible and can easily be transferred.

Tokenization makes it extremely easy for holders to take fixed leveraged exposures. By simply buying tokens and holding them, traders automatically and passively take leverages.

For example, ETHBULL 3x means that the token is longing ETH and taking a 3x leverage with ETH exposures. If ETH goes up by 1%, the token will go up by 3%. An ETHBEAR 3x token shorts ETH with a 3x leverage. If ETH goes up by 1%, the token will go down by 3%.

### Net Value and the ‘Anchor’ 

Phoenix’ leveraged tokens are fully backed with cryptoassets and their net value can be calculated through live price feeds. The net value of leveraged tokens is an important indicator when evaluating their financial performance.

The net value of a leveraged token is calculated as the value of total assets subtracting total debts. When drafting a balance sheet for the token, the net value will be equivalent to the ‘net assets’ in equities.

To make the tokens easier to comprehend and trade, Phoenix protocols designate the initial value/price for leveraged tokens as $100. This initial ‘price’ is regarded as the ‘Anchor’. If the price of a leveraged token becomes too low and the market is unfavorable, the protocol will restore the price to its initial anchor and adjust the quantity of the token accordingly. The mechanism shares similarities with rebasing, as the quantity of the token holding is subjected to changes according to the asset’s price.

To maintain the continuity and smoothness of the price curve, in the first version of the protocol (PPLT v1.0), the rebasing price is set to be $10.

For example, assume Bob purchases 10 units of ETHBULL (3x) tokens. If the value of the token decreases to $10, due to the drop of the ETH price, the value of Bob’s holdings becomes $100. The $10 price triggers the rebasing process, and the value of the ETHBULL (3x) token will be rebased to $100, while units of Bob’s ETHBULL (3x) tokens will be adjusted to 1. Bob’s holdings are worth $100, the same as they were before rebasing.

## Collateralization Requirements

When creating decentralized leveraged tokens, the PPLT makes sure that these tokens are 100% collateralized. In other words, Phoenix leveraged tokens are NOT synthetic assets, but asset-backed tokens. Real transactions on decentralized exchanges guarantee that the tokens’ value is fully backed by cryptoasset holding and borrowing.

Suppose there are no gas or other transaction costs. When one buys an ETHBULL (3x) token with a net value of $100, he/she will pay $100 for the token, and the smart contract will simultaneously borrow $200 from the stablecoin lending pool. The $300 will immediately be transacted for $300 worth of ETH from decentralized exchanges, assuming there is no slippage. This will generate a 3x ETH price exposure.

If we are making a balance sheet for the token, the total asset is $300 and the total liability is $200, which makes the net value of the token $100. The leveraged token is therefore fully collateralized.

If the ETH price rises by 50%, due to the 3x leverage, the leveraged token price will be $100×（1+50%×3）=$250. According to the ‘balance sheet’, the total asset in ETH will be worth $300×(1+50%)=$450, while the total liability is still $200, as it is borrowing stablecoins. Therefore, the net asset/equity of the token will be $250 ($450-$200). Again, the leveraged token is fully collateralized.

These considerations remain true when the ETH price drops. Full collateralization is a fundamental tenet of Phoenix’ leveraged tokens.


## Creation and Minting

When users buy Phoenix leveraged tokens, the same number of tokens is minted by smart contracts. A series of transactions take place upon the receipt of the consideration, priced in stablecoins or the underlying assets.

For example, imagine a user buying 1 unit of ETHBULL (3x) token with USDC, supposing its net value is $120. Let us assume there is no transaction cost or price slippage, and the token has not rebalanced yet.

After receiving $120 USDC, the contract will invoke the function needed to borrow $200 USDC from the pool, which is two times the "anchor" net value of the token. Then, the $320 USDC will be exchanged for ETH from decentralized exchanges. 1 unit of ETHBULL (3x) token will be minted accordingly, with a claim to the net value of the collateral. Note that in this example, the actual leverage upon purchasing is 2.67 ($320/$120).

For the creation of an ETHBEAR (3x) token, the process would be slightly different. For every ETHBEAR (3x) token, $200 ETH will be borrowed from the pool and sold through decentralized exchanges for stablecoins.


## Redemption

In the PPLT v1.0, when the Phoenix leveraged tokens are "sold" on the market, they are actually redeemed, which also triggers a series of transactions. The same number of leveraged tokens is burnt, and the purchasing transactions are reversed, with the remaining balance paid back to the holders.

For example, if the value of ETHBULL (3x) token is $110, the ‘balance sheet’ of the token comprises $310 ETH in total assets and $200 borrowing in total liabilities.

When 1 unit of the token is sold/redeemed, the mechanism sells the ETH for $310 and repays the $200 debt, leaving $110 as the remaining balance to be transferred to the seller.

To redeem an ETHBEAR (3x) token, ETH will be bought back from the market to repay the ETH debt. The remaining balance will be transferred to the seller.

