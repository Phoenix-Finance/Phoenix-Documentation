## Making FPO v1.0 Safe & Secure

In addition to the basic introduction of FinNexus Protocol for Options (FPO) model. There are several important mechanisms elaborately designed for security purposes. It is highly recommended that, before jumping into the pool or purchasing options on the FPO platform, one should go through these innovative mechanisms, in order to have a better understanding of the FPO model.

### 1. Minimum Collateral Requirement

As introduced in the [options guidance](guide.md), for the writers/sellers of options, the potential risks are theoretically unlimited. To keep the option contracts secure and capable to perform, there are usually two ways to maintain the full collateralization of the options exposure. 

#### (1) Margin Requirements for Cash Settlement
As widely applied in traditional finance and centralized crypto exchanges, for writers/sellers of options, in other words those who short call or put options, some deposits are required to collateralize the option contracts as margin. The margin ratio is normally 5% to 20%. For example, Deribit’s margin requirement for shorting options is shown [here](https://www.deribit.com/pages/docs/options). This mechanism is capital efficient. It needs less initial margin deposit and provides additional leverage to the sellers, but may require additional capital input, or even lead to liquidation events if the price moves unfavorably. [Cash settlement](https://www.investopedia.com/terms/c/cashsettlement.asp) is often applied with respect to these kinds of options.

#### (2) Full Collateral for Physical Settlement
Smart contracts and the digital nature of crypto assets provide alternative choices, especially for [physical settlement](https://www.investopedia.com/terms/p/physicaldelivery.asp). The full amount of underlying assets can be physically locked in the smart contracts, in a censorship-resistant way. No one needs to worry about counterparty risk, similar to the way that OPYN have designed their hedging contracts.

However, FPO v1.0 applies a unique Multi-Asset Single-Pool (MASP) model, which pools all the liquidity together to serve as the sole counterparty for writing, trading, and exercising all of the options exposure written from the pool. MASP is the core mechanism and the safety of the pool is always the first priority.

As introduced before, the option sellers’ risks can be relatively high. MASP pools all the sellers and liquidity, also sometimes referred to as collateral, together to form a collective counterparty for all options. The point of this pool is to diversify the pool’s risk exposure away from any single type of option. While this tactic largely mitigates the risk exposure for a single seller, it does not eliminate it. The collateralization ratio of the monolithic pool should be high enough to safeguard against massive market movements and other black swan events.

As a result, FinNexus introduces the [Minimum Collateral Ratio (MCR)](https://www.docs.finnexus.io/terminology/) requirement for the pool. It is an innovative mechanism designed to control the size of the pool’s total options exposure. The MCR ensures that the options are always over-collateralized.

Due to the multiple asset nature of the pool, according to the liquidity, volatility, and market acceptance of these different crypto assets, The MCR for FNX, USDC, and WAN is set to be different, 500%, 120%, and 500% respectively, and a weighted average MCR (if the pool has multiple kinds of assets) will decide the maximum value of options able to be issued by the pool.

For example, if there are $50,000 FNX in the pool, for BTC puts with $10,000 as the strike price, only an option of value 1 BTC can be written.

In other words, for the pool with relatively high MCR, the pooled sellers are de-leveraged, and more security is guaranteed. This is exceptionally important when the pool is relatively small.

### 2. Pricing Adjustment Coefficient

The [classic Black-Scholes options pricing model](https://www.investopedia.com/terms/b/blackscholes.asp) is applied in FPO v1.0 for pricing options and is integrated into the smart contract codes. After inputting certain variables of the Black-Scholes formula via the user interface — like the underlying assets, amount, strike price, and expiration — the remaining required Black-Scholes variables will be inferred and the option premium will be automatically calculated.

One of the main purposes of designing MASP is to make the risks faced by individual option sellers adequately diversified, by collectively pooling all the options writers together. The key is the difference in expectations of crypto holders and the variety of options live in FPO.

However, if the options are not adequately diversified, for example, some large options buyers could drain the pool’s liquidity with options of similar terms. In such a state, the risks for the pool can be quite concentrated. And that risk is much more likely when the pool is small.

Therefore, we have introduced a pricing adjustment coefficient to mitigate the concentration by adding a coefficient for pricing options. It automatically discourages the purchase of options that are already over-weighted in the pool. The coefficient acts as an adjustment multiplier of the Black-Scholes model in pricing options.

In FPO v1.0, the coefficient is decided as follows:

![](https://miro.medium.com/max/875/1*OuqCZKWhXZKh9nNBfLRaJA.png)

The Pricing Adjustment Coefficient changes as follows:

![](https://miro.medium.com/max/1250/1*vMTs8dm-fpIfzG9VtYaPJg.png)

In a nutshell,
*If there are more calls than puts, calls are more expensive.
And vice versa, if there are more puts than calls written by the liquidity pool, puts are more expensive.
The more options written by the pool, the more expensive they are.*

![](https://miro.medium.com/max/875/1*gtx24oI7Rd6kh3idl-xiKQ.png "An example on options pricing influenced by the coefficient")

### 3. One-hour Chill Time

DeFi is still at a nascent experimental stage. We witnessed a number of exploits in the past few months, among which a great proportion are done though [flash loans](https://news.bitcoin.com/defi-flash-loans/). These instant uncollateralized loans enable attackers to make nearly risk-free trials to hack decentralized protocols with little capital requirements and low costs beyond Ethereum gas fees and the time to research the potential exploit.

However, flash loans require that all assets borrowed should be returned before the end of the transaction, in the same mined block.

To protect against possible flash loan exploits in FPO v1.0, a special mechanism called ‘Chill Time’ is designed, during which the options buyers cannot sell or exercise the options, and the pool participants cannot withdraw their assets out of the pool. ‘Chill Time’ is set to be one hour.

### 4. Moving Average IV and the IV Surface Mapping

It is said that trading options is simply trading IV. What is IV? Implied Volatility (IV) is the measurement of the uncertainty of the price movement of the underlying asset. In the Black-Scholes pricing model, it is the key factor in option pricing.

However, the options market of crypto assets is not liquid enough to provide all the IVs for all the potential underlying crypto assets. Even with deeply liquid crypto on the spot market like ETH and BTC, IVs are still somehow quite volatile due to relatively high bid-ask spreads, even for some centralized well-known exchanges like Deribit. For some at-the-money IVs of certain assets with a 5% movement, there could be hundreds of on-chain data inputs per day. That could not accurately trace the market, and also get quite expensive in gas!

Therefore, FinNexus applies the average IV from the most liquid options on the market, which is 1 day, 2 days, and 7 days at-the-money IV, and feeds it into FPO v1.0 by an hourly [moving average](https://www.investopedia.com/terms/m/movingaverage.asp). The protocol then uses this data point as the ‘Anchor IV’ for our DeFi options market.

Based on this ‘Anchor IV’, FPO v1.0 applies the [Stochastic Volatility Inspired (SVI) parameterization model](https://medium.com/finnexus/designs-to-make-fpo-v1-0-safe-and-secure-afee6a729e1b), and derives the [volatility matrix or volatility surface](https://www.investopedia.com/articles/stock-analysis/081916/volatility-surface-explained.asp). To be noticed that the whole IV Surface is subjected to changes based on the feed of the ‘Anchor IV’.

Through these innovative mechanisms, FPO seeks to eliminate the abnormal IV movements due to the illiquidity of the market, derive the IV for less liquid options, and be fed by the live IV changes through anchors, according to the market conditions.

All that is to say that we think we’ve figured out a novel way to bring vital IV data into our smart contracts that no other DeFi options protocol does yet.

### 5. Dual Decentralized Oracles

Safety and stability of price feeds are crucial for the survival of FPO v1.0. FinNexus is integrating Chainlink and Band Protocol price feeds live on Ethereum and Wanchain Mainnet, respectively, to power decentralized options. We aim to be a pioneer in the crypto industry for this approach of dual decentralized oracles.

To sum up, we firmly believe that these 6 mechanisms enable us to provide a robust, safe, and secure environment for crypto enthusiasts to purchase options exposure.
