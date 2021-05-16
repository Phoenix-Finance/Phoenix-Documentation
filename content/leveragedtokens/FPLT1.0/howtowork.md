## How does the FPLT work?
### Tokenization of Leveraged Positions

As the name indicates, FinNexus tokenizes the decentralized leveraged products into ERC-20 tokens. These tokens are fungible and can easily be transferred.

Tokenization will make it extremely easy for holders to take fixed leveraged exposures. By simply buying tokens and holding them, traders will automatically and passively take leverages.

For example, ETHBULL 3x means that the token is longing ETH and taking a 3x leverage with ETH exposures. If ETH goes up by 1%, the token will go up by 3%. An ETHBear 3x token shorts ETH with a 3x leverage. If ETH goes up by 1%, the token will go down by 3%.

### Net Value and the ‘Anchor’ 

FinNexus’ leveraged tokens are fully backed with cryptoassets and their net value can be calculated by live price feeds. The net value of leveraged tokens is an important indicator when evaluating the financial performance of leveraged holdings.

The net value of a leveraged token is calculated as the value of total assets subtracting total debts. When drafting a balance sheet for the token, the net value will be equivalent to the ‘net assets’ in equities.

To make the tokens easier to comprehend and trade, FinNexus protocols designate the initial value/price for leveraged tokens as $100. This initial ‘price’ is regarded as the ‘Anchor’. If the price of a leveraged token becomes too low and the market is unfavorable, the protocol will restore the price to its initial anchor, and adjust the quantity of the token accordingly. The mechanism shares similarities with rebasing, as the quantity of the token holding will be subjected to changes according to the asset’s price when rebalancing.

To maintain the continuity and smoothness of the price curve, in the FPLT v1.0, the rebasing price is set to be $10.

For example, let us assume Bob purchases 10 units of ETHBULL (3x) tokens. If the value of the token decreases to $10, due to the drop of the ETH price, the value of Bob’s holding becomes $100. The $10 price triggers the rebasing process, and the value of the ETHBULL (3x) token will be rebased to $100, while units of Bob’s ETHBULL (3x) tokens will be adjusted to 1. Bob’s holding is still worth $100, the same as it was before rebasing.
