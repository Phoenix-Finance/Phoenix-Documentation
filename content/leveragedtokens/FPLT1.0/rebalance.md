Rebalancing is a very important mechanism to keep the leverage at the targeted level. There are two instances when leveraged tokens will rebalance themselves.

## Scheduled Rebalancing
FinNexus leveraged tokens "rebalance" themselves periodically, so that they can keep the target leverage. In every rebalancing, each leveraged token reinvests profits if making any, and if losing money, sells off part of its position to lower the leverage and avoid liquidation.

In the FPLT v1.0, on ETH, the scheduled rebalancing happens once every day. On the Binance Smart Chain (BSC) & Wanchain, it happens once every 6 hours.

For example, let us imagine that a user holds 1 unit of ETHBULL (3x) token with an initial cost of $100. The price of ETH increases by 10% and the token price rises to $130 before rebalancing. Now, the holder’s leverage becomes 2.54 ($330/$130), lower than the targeted leverage.

During the scheduled rebalancing, the protocol will borrow more USD from the stablecoin pool and purchase extra ETH tokens to shift the leverage back to 3x. In our example, the protocol would borrow another $60 and exchange it for ETH. The total leverage would thus become 3 ($390/$130) again.

Following the example above, what would happen if the ETH price decreased by 10% and the token price dropped to $70 before rebalancing? The holder’s leverage would become 3.86 ($270/$70), higher than the targeted leverage. In the rebalancing process, the protocol would then sell ETH tokens and repay the outstanding debt to deleverage. In our example, the protocol would sell $60 ETH for USD and pay back to the pool. The total leverage would once again be 3X ($210/$70).

For Bear leveraged tokens, the rebalancing process is similar to the one mentioned above.

## Temporary Rebalancing
One interesting aspect of leveraged tokens is that their holders never have to worry about liquidation, as the product automatically deleverages itself.

However, it is important to be aware that a temporary rebalancing may be needed when an unfavorable price movement occurs, especially in a short period of time.

For example, for ETHBULL (3x) tokens, if the ETH price were to drop by over 33%, the token value would go ‘negative" — something akin to getting liquidated. In such cases, a rebalancing mechanism needs to be triggered to deleverage the tokens, even if the time for a scheduled rebalancing has not yet arrived.

In the FPLT v1.0, for the 3x leveraged tokens, the threshold to trigger a temporary rebalancing is set to be a 20% unfavorable movement against the past underliers’ rebalancing price. Bull and Bear leveraged tokens with different underlying assets will have independent triggers to activate a temporary rebalancing. 

The temporary rebalancing process itself, however, will be the same as the scheduled rebalancing.
## Termination
If the temporary rebalancing is unsuccessful, no matter the reason, the protocol will initiate a termination process once the price gets to a 30% unfavorable movement.

Termination is similar to a liquidation process, with all the terminated leveraged tokens being redeemed and burnt. After triggering a series of transactions on dexes, the debts will be paid back, outstanding interest and fees will be deducted, and the remaining balance will be claimable for the leveraged token holders.
