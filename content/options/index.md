# The FinNexus Protocol for Options (FPO)

The FinNexus Protocol for Options (FPO) provides a decentralized way of writing and trading options. All the functions of options - writing, trading, exercising, etc. - are deployed on smart contracts. It is a permissionless, censorship-resistant, and non-custodial protocol. The settlement is verified on-chain.

FinNexus plans to introduce its options protocol with a two-step plan for 2020. The first phase for the FinNexus Protocol for Options (FPO) will debut online today with the v0.1 release. The second phase is currently under development. In general, FPO v0.1 is a tokenized options protocol for minting and trading options tokens, while the next iteration will be a collective pooled options protocol for options writing, exercising, and trading. Different smart contracts will be deployed in these two phases.

## What are FinNexus options?
The FinNexus options in FPO v0.1 are tokenized options that give the holders the right, but not the obligation, to buy or sell underlying crypto assets at a specified price (Strike Price) at expiration.

Every option supported by the FinNexus Protocol for Options is integrated through an option token smart contract which is a WRC20 compliant representation of options on Wanchain. Later, when we modify these smart contracts for our Ethereum-based platform, the option tokens will be ERC20 compliant. These option tokens are transferable, fungible, and can integrate or be integrated with other DeFi protocols.

For those who are unfamiliar with options in general, please review our [What are options?](guide.md) and [Key Terms](terms.md) sections before continuing in this section.


## How to read a FinNexus option token symbol?
A FinNexus token symbol is combined with a symbol of the underlying asset, a tag indicating whether it's a put or a call, along with its expiration and strike price.

For example, 'BTC, put, Jul 03, $9000' means a BTC put option with an expiration date, sometimes called a maturity date, of July 3rd and a strike price of $9000.

## Writing Options/Minting Option Tokens
FPO is permissionless and anyone can be an option writer by depositing enough collateral into the contract. In FPO v0.1, the creation of the types of options is controlled by the FinNexus Foundation account. For instance, to control risk during these beta stages, only the Foundation will be able to decide what types of options (put/call, expiration, strike) are available for minting. At later stages, this functionality will be open to the public.

Just as with options in traditional finance, the sellers or writers of options need to deposit some form of collateral as margin in case the contract gets exercised. In FPO v0.1, users can choose to write options or mint option tokens by locking an equivalent amount of value denominated in the acceptable crypto asset as collateral into the smart contracts. In FPO v0.1, both FNX and WAN can serve as collateral for these contracts. In one transaction, the collateral is posted into the smart contract and the corresponding amount of options tokens are created and transferred to the writer's same address.

The minted option tokens can then be directly sold to capture the premium through the FinNexus options platform. Selling an option token means selling the buyer the right to buy or sell a crypto asset at a specific price (strike price) at a specific date. The writers need to take the equivalent risks with the possible exercising of the options. In addition, they could also consider hedging their exposure by buying other options available on the platform.

In FPO v0.1, the type of options provided are European, which means the buyer can only exercise the contract at the time of expiration. Users may have more flexible choices in later versions of the protocol.

FinNexus option tokens will be tradable anytime up until 5 hours before maturity. At that time, trading will be halted and settlement will occur at UTC 8:00am of the expiration date of the option.

For minting and selling option tokens, options writers will be compensated with premiums. Transaction fees and liquidity mining incentives will also accrue to liquidity providers. Details will be released.

## Buying Options

FPO v0.1 will provide a trading venue for option tokens transactions. Option Tokens can be bought by calling the buy function. 

No collateral or margin is needed for the option buyer to buy option tokens. However, he/she needs to transfer the equivalent amount of crypto assets in trading pairs into the order system.
By purchasing a call option token, you are taking advantage of leverage; allowing you to use less money to gain positive exposure to the price of the underlying assets.

By purchasing a put option token, you are taking advantage of protection or insurance, to protect yourself against the underlier's price drops, with negative exposure to the price of the underlying assets.

With the combination of buying different kinds of Options, one may get exposure to some more complex trading strategies.

## Selling Options
Once a user buys option tokens on the FinNexus options platform, he/she can sell it in part or fully anytime before the expiration.

FinNexus will try to provide an active and liquid exchange market for the circulation of the option tokens.

## Selling and buying order
In FPO v0.1, it will provide a neat exchange venue with order books for users to buy and sell options tokens.

The buying and selling orders will be matched based on the time sequence.

FinNexus foundation will provide the initial market-making function for the liquidity of the option token circulation.

## Margins(collateral) of Options - a dynamic margin mechanism

FPO smart contracts provide a potential for multi-coin collateral function, meaning that there could be a variety of crypto-assets (WRC20 on Wanchain and later ERC20 on Ethereum) used as collateral/margin for minting option tokens, as long as they are whitelisted in smart contracts.
The seller/writer of options should deposit and collateralize a certain amount of margin (or collateral) in the contract to ensure the exercise and performance of the contract. In theory, the minimum margin requirement should cover the loss of the option seller. However, considering the penalty of compulsory liquidation and reducing the risks of liquidation when the market suffering large fluctuation, the margin should generally exceed the potential loss of option seller.

At the same time, to simplify the model and implementation, a dynamic margin design is applied in the smart contracts, for writing options and minting option tokens. The minimum margin required will be dynamically changed according to the price of underly assets comparative to the strike price, or the degree of moneyness of an option.

## Call option margin
The writer of a call option shall lock up the option margin in the smart contract. In cases that the price of the underlying asset rises, especially if it exceeds the strike price (in the money), the option seller will bear the loss after the exercise, and generally, the writer's margin should increase; if the price of the underlying asset drops and is lower than the exercise price (out of the money), the buyer is less likely to exercise, and the margin should be reduced accordingly.

The blue bold polyline in the chart below is the dynamic minimum margin requirement for a FinNexus call option writer. If the deposited USD value of the collateral is above the polyline, it means the collateral ratio is over 100% and the position is safe; if it drops below the line, meaning that the collateral ratio is less than 100% and the position is not regarded as safe by the smart contract and should be liquidated.

![](../img/options/options01.png "The minimum margin requirement for FinNexus call options")
<center>*The minimum margin requirement for FinNexus call options*</center>
<br>
![](../img/options/options02.png "The minimum margin requirement for FinNexus call options")
<br>
<br>

For example, for a BTC call option with a strike price of $7000, when 6300 ≤ market price P ≤ 9100, the minimum margin required is $3500 (0.5*$7000), which means when the writer deposits $7000 margin into the SMC, he or she may mint up to 2 option tokens. When the BTC price P is $5400, the minimum margin for minting one option token is $3000; while, when the BTC price P is $10000, the minimum is $4400.

## Put option margin
The writer of a put option shall lock up the option margin in the smart contract. In cases that the price of the underlying asset drops, especially when it is becoming lower than the strike price (in the money), the option writer will bear the loss after the exercise, and in principle, the margin requirement of the writer should increase; if the price of the underlying asset rises, and is higher than the strike price (out of the money), the buyer will not exercise, and the margin should be reduced accordingly.

Similarly to the calls, the blue bold polyline in the chart below is the dynamic minimum margin requirement for a put option writer. If the deposited USD value of the collateral is above the polyline, it means the collateral ratio is over 100% and the position is safe. If it drops below the line, it means the collateral ratio is less than 100% and the position should be liquidated.

![](../img/options/options03.png "The minimum margin requirement for FinNexus put options")
<center>*The minimum margin requirement for FinNexus put options*</center>
<br>
![](../img/options/options04.png "The minimum margin requirement for FinNexus put options")
<br>
<br>

It is noted that in cases when the price of the underlier is out of the money to some great extent (1.928 times of strike price); to avoid the margin falling below zero, the protocol keeps a minimum margin requirement to the level of 0.01SP.

Corresponding margin/collateral will be locked when the option tokens are minted and before expiration. The writer may choose how many options tokens to be created, but he/she has to make sure that the value of the collateral is above the minimum margin requirement, which is defined as the polyline above.

When a writer's margin (the value of collateral) falls below the minimum requirement, anyone who holds the equivalent minted options tokens, could transfer some or all of the number of outstanding tokens minted by the writer, into the contract, acting as a liquidator, to liquidate the position. The liquidator may, in return, get a discounted amount of collateral held by the writer; and this discount is defined as the liquidation incentive.

After expiration corresponding collateral will be unlocked and redeemed by the writers.
Collateral could be withdrawn anytime by the writers provided that the collateral is above the margin requirement.

## Liquidation

### What is Liquidation?

Liquidation is the process of selling collateral to cover a user's generated option tokens. When collateral coverage is below the minimum margin requirement, it means that there are risks that collateral may not be adequate to cover the exercise of the option contract. During the Liquidation process, margin/collateral will be transferred to the liquidator's holdings along with a Liquidation Penalty.

Liquidation helps to ensure that the potential cash settlement of options tokens is always fully backed by an appropriate amount of collateral that is under the minimum margin requirement.

### What are the Collateral Ratio and Liquidation Ratio?

The Collateral Ratio is the ratio of the actual value of collateralization/margin to the minimum margin requirement.

> *Collateral Ratio = value of collateralization/minimum margin requirement*

The Liquidation Ratio is the minimum required collateralization/margin level for each option token before it is considered undercollateralized and subject to liquidation. In FinNexus Protocol for Options v0.1, the Liquidation Ratio is set to 100%, which means the value of the collateral should at least be no less than the minimum margin requirement.

> *Liquidation Ratio = 100%*

The FinNexus Protocol for Options's Oracles provides the system with price data that is used to track whether the Liquidation Ratio is breached. Once breached, the positions are exposed to liquidation.

Following the examples above, for a BTC call option with a strike price of $7000, when 6300 ≤ market price P ≤ 9100, the minimum margin for writing one option contract is $3500 (0.5*$7000). If the writer deposits $7000 worth of FNX tokens into the smart contract as the collateral, then the collateral ratio will be 200% ($7000/$3500).

Please be noted that the collateral ratio is subjected to changes due to the price movement of both the underlying asset and the collateralized asset.

When a seller is getting some multiple exposures to different options tokens, the Collateral Ratio will be jointly calculated, as follows:

> *Collateral Ratio = ∑ value of collateralization / ∑minimum margin requirement*

### What is the Liquidation Penalty/Incentive?

In order to make sure the option tokens are always fully collateralized for the potential settlement, the liquidated writers will be subjected to Liquidation penalties, and the liquidators will be incentivized to liquidate the undercollateralized positions.

Liquidation Penalty means that the liquidated writers will suffer a loss from the value of the collateral when liquidated by others; and the loss will be distributed to the liquidators as Liquidation Incentive.

The Liquidation Penalty/Incentive in FPO v0.1 is 20% of the bid value of the option token when transferring into the smart contract for liquidation.

For example, when the bid price for one BTC option token is $300, the liquidator will get the collateral amounting to $360 instantly, after liquidating one BTC option token. 

### What happens during a Liquidation?

* The protocol detects when the collateral ratio falls below 100% and triggers a liquidation occasion

* The collateral is put up for liquidation

* Liquidators may transfer some or the full amount of the option tokens into the smart contract, and the equivalent value of the collateral will be paid back into the same address, including the Liquidation Incentive

* The same amount of collateral will be deducted from the writer's margin account, including the Liquidation Penalty

* The amount of Liquidation Penalty/Incentive will be calculated from the USD value of the option tokens, when transferring into the smart contract for liquidation

* The Liquidation Penalty/Incentive is 20% of the bid value of the option token when transferring into the smart contract for liquidation

* The option tokens sent into the smart contract for liquidation are burnt

* When the collateral ratio is above 100% after a certain liquidation process, further liquidation will be ceased, and the remaining options will be regarded as fully collateralized.

* It is strongly advised that the writers should always keep a healthy position and closely monitor the collateral ratio above the liquidation level.

## Exercising

### When to exercise
The FinNexus option tokens in FPO v0.1 will be European type and can only be exercised upon expiration.

### Whether to exercise
Whether it is financially beneficial for the option holders to exercise will be judged by the oracles and smart contracts.

Options will be automatically exercised upon expiration if the strike price is in the money, when, for call options, the strike price is lower than the underlier's current price, and for put options, the strike price is above the underlier's current price.

### How to exercise

The exercising is automatically done by the smart contracts, when the options are in the money at expiration. While if the options are at the money or out of the money, the exercising will not be triggered.

### What happens when exercising

The FinNexus options will be cash-settled, which means only the difference will be settled. The difference between the strike price and the market value of the underlying asset will be exchanged into the margin\collateral assets by oracles and transferred into the buyer's address.
For example, a call option, backed by WAN, is in the money at expiration, the option token holder will get the following amount of WAN when exercising:

![](../img/options/options05.png "Exercising options")
<br>
<br>
![](../img/options/options06.png "Exercising options")
<br>
<br>

A put option, backed by WAN, is in the money at expiration, the option token holder will get the following amount of WAN when exercising:

The same logic will apply in other collateralized crypto assets.

After expiration, whether exercised or not, the relating option smart contracts will be terminated.

The gas fees of automatic exercising option contracts at expiration will be undertaken by the FinNexus platform in FPO v0.1.

## Oracles and Price

In FPO v0.1, all the crypto assets' values, including the collaterals, strike assets, etc., will be calculated and measured in US dollars.

All related token prices except options token will be fed by the oracle and written in the contract.
All price feeds are exercised in every 5 minutes.

![](../img/options/options07.png "Band Protocol partnership")
<br>
<br>

FinNexus has established a partnership with Band Protocol, and decentralized oracles will be integrated into FPO.

## Security and Fees

### Security
FPO v0.1 has not been audited yet, and can currently be considered experimental software. The code is publicly available at FinNexus's [GitHub](https://github.com/FinNexus/OptionsContract). We've made a considerable effort in order to create a secure protocol, but please don't supply your life savings or assets you can't afford to lose. When an audit is performed the results will be published publicly through FinNexus's official channels.

### Fees
FPO v0.1 is free of charge except:
There is a 0.3% transaction fee when buying and selling options on the FinNexus exchange venue.
There is a 0.3% fee collected from the holders, when exercising the options at expiration; and a 0.3% fee collected from the liquidator when liquidating.
User interface

FPO v0.1 will provide a user-friendly interface for users to buy and sell the option tokens easily. In the first version, there is no interface for option writers, but one may do the related writing operations through the API.

See our [FPO Smart Contracts](contracts.md) section for more information.

The options writing interface is under development and will be open to the public in future upgrades.