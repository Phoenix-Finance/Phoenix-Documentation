## Holding a call to speculate

The long call option strategy is the most basic option trading strategy, whereby a user buys call options with the belief that the price of the underlying asset will rise significantly beyond the strike price before the option expiration date.

![image|690x437](https://aws1.discourse-cdn.com/standard17/uploads/community12/original/1X/0bce6bc743ed0c8d30a496a7ad594c2199ebec5f.jpeg) 

Sam is a ETH hodler and he is bullish due to the growing DeFi ecosystem on Ethereum. He is holding 1 ETH already. To maximize his gains if the ETH price goes up in the near future, Sam buys 1 ETH call with the strike price of $700 and the expiry of 15 days. The premium is $70 for each contract.
If the price grows by 20% to $840 in two weeks, Sam will get $140 ( $840-$700 ) by exercising the call, and the return is 100% ( ( $140-$70 ) / $70 ). The call gives Sam a 5x leverage in return.

If the price drops by 20% to $560 in two weeks, Sam will not exercise the call option and $70 is all he can lose. But for holding one ETH, Sam may lose $140 from the collapse.

If Sam is extremely bullish and he can even deposit ETH on Makerdao, Compound or Aave, to borrow stable coins to buy call options. This will give him even further leverages, and higher risks.

## Protective Puts: A Hedging Strategy

A **protective put** position is created by buying (or owning) an asset and buying **put** options with a [strike price](https://corporatefinanceinstitute.com/resources/knowledge/trading-investing/strike-price/) equal or close to the current price of the asset. 

A protective put strategy is analogous to the nature of insurance. The main goal of a protective put is to limit potential losses that may result from an unexpected price drop of the underlying asset.

Adopting such a strategy does not put an absolute limit on the potential profits of the investor. Profits from the strategy are determined by the growth potential of the underlying asset. However, a portion of the profits is reduced by the premium paid for the put.

![image|690x437](https://aws1.discourse-cdn.com/standard17/uploads/community12/original/1X/2958cb8fb0e32b2ffb508249f3456f3faa1652b7.jpeg) 

**Example of Protective Put**

You own 100 ETH, with each ETH valued at $500. You believe that the price of ETH will increase in the future. However, you want to hedge against the risk of an unexpected price decline. Therefore, you decide to purchase 100 protective put contracts with a strike price of $500. The premium of one protective put is $10.

## A Covered Call to Benefit From a Flat Market

A covered call is created by owning an asset and selling an equivalent amount of call options. To execute this strategy, a trader holds a long position in an asset and writes (sells) call options on that same asset to generate an income stream.

![image|690x437](https://aws1.discourse-cdn.com/standard17/uploads/community12/optimized/1X/9e53e3ba617863002bb971e12f725c8658ddb441_2_1035x655.jpeg) 

Lucy is holding ETH with a price of $750. She expects that the market will stay flat for a while and wants to possibly lower her cost in the flat market. Therefore, she decides to sell ETH calls with the strike price of $760 and earn the premiums of $50 immediately.
If the price gets higher than $760, she will sell when the option buyers exercise the calls. If the price stays lower than $760 till expiration, she will still get premiums and lower the cost of holding one ETH by $50.

In this example, Lucy employs a covered call strategy as she intends to hold the underlying asset for a long time but does not expect an appreciation in price in the short term, and she is satisfied with selling the assets at a predetermined price.

Please note that FPO v1.0 on FinNexus doesn’t allow for selling options for now.

## Straddle Strategy

A straddle is a strategy accomplished by holding an equal number of puts and calls with the same strike price and expiration dates.

A straddle is meant to take advantage of the market price change by exploiting increased volatility, regardless of which direction the market’s price moves.
For example, I am not sure BTC is going to go upwards or downwards in the coming days. But I expect the movement will be big. I can buy a straddle from FinNexus options platform.

Suppose I buy a call and a put together with the strike price $19000. If the market moves up, the call is there; if the market moves down, the put is there. It may cost me like 500 USD in total. If the BTC rises above 19500, or fall below 18500, I will end up in profit.
What is more beneficial is that I can exercise the options and collect the profit anytime before they go expired.

This is a typical straddle strategy.

## Strangle Strategy


The **long strangle** involves going long (buying) both a [call option](https://en.wikipedia.org/wiki/Call_option) and a [put option](https://en.wikipedia.org/wiki/Put_option) of the same underlying security. Like a [straddle](https://en.wikipedia.org/wiki/Straddle), the options expire at the same time, but unlike a straddle, the options have different [strike prices](https://en.wikipedia.org/wiki/Strike_price).
![image|601x305](https://aws1.discourse-cdn.com/standard17/uploads/community12/original/1X/e6c44ffaa78cc4012afff1b0e1ebb327f51be4f6.png)  

A strangle is a good strategy if you think the underlying security will experience a large price movement in the near future but are unsure of the direction. However, it is profitable mainly if the asset does swing sharply in price.

The cost of a strangle can be lower than a straddle, as the options are [OTM](https://www.investopedia.com/terms/o/outofthemoney.asp).
The example is just like the one in the straddle strategy, well with different strike prices.

## IL Hedging

[Hedging Against Impermanent Loss: A Deep Dive With FinNexus Options](https://coinmarketcap.com/alexandria/article/hedging-against-impermanent-loss-a-deep-dive-with-finnexus-options) on Coinmarketcap Alexandria by FinNexus Cofounder Ryan Tian
