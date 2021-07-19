## PPO

PPO stands for The Phoenix Protocol for Options. It is a cross-chain, permissionless protocol for decentralized options built by Phoenix Finance.


## MASP

MASP stands for Multi-Asset-Single-Pool. It is the core mechanism applied in PPO v1.0.

PPO v1.0 is a decentralized peer-to-pool options protocol, with liquidity pools as the counterparty for writing and settling option contracts.

'Multi-Asset' features in the liquidity pools enables the creation and trading of options from any type of underlying asset, including crypto assets, commodities, fiats, stocks, indexes, etc. The potential for the underliers can be unlimited.

Also, 'Multi-Asset' means that there can be multiple types of crypto assets in the liquidity pool. For example, PPO v1.0 has a USDC pool on Polygon. It may include other stable coins like USDT, DAI, etc., in later updates.

'Single-Pool' does not mean that there is only one pool in PPO v1.0. While one liquidity pool may power many different options contracts. Liquidity can be shared automatically, different from the traditional order books.

The MASP (Multi-Asset Single Pool) Liquidity Pool in the PPO is much different than liquidity pool concepts found on other DeFi platforms like Uniswap or Balancer. These two, in particular, behave as automated market makers for cryptocurrency swaps. MASP Liquidity powered by the collateral token is the liquidity solution for both the creation and settlement of options contracts, as well as the transaction between those options.

The unique MASP system — Multi-Asset Single-Pool — allows the users to gain exposure to a variety of bespoke cash-settled options positions on a variety of underlying assets.

## PPT
PPT means the Phoenix Pool Token, as the shares in the PPO v1.0 liquidity pools.

PPO v1.0 is a decentralized options protocol with a peer-to-pool model. The liquidity pool is created when individual liquidity providers contribute liquidity by locking their crypto assets in the pool. The liquidity provider receives a pool token, as PPT, which represents their share of ownership in the pool. 

It works similar as the Uniswap LP token or Balancer LP token (BPT), but in the options collateral/liquidity pool.

Options exposure sold to options buyers will earn options premiums. These premiums will automatically accrue in the MASP liquidity pool and, as premiums compound over time, there should be an increased value reflected in the PPT tokens. Remember that these PPT tokens represent are pro-rata share in the liquidity pool. Returns of pool participants are easily measured by the pool share net value.

## Pool Net Value

Pool Net Value measures the monetary (USD) value of all the options exposures currently in the liquidity pool. It is calculated on the basis of accrual accounting and, as a result, may not be equal to the sum of actual net inflows and outflows at any given time.

**What Affects Pool Net Value?**

Let us take the USDC pool for example. (The other liquidity pools follow the same principles as described below.)

The total Pool Net Value (PNV) in USD is affected by the following factors:

① USDC deposits increase the PNV;
② USDC withdrawals decrease the PNV;
③ Receiving option premiums increases the PNV, with the caveat that the premiums accrue to the PNV over time as the options within the pool move towards maturity. This accrual mechanism is explained in more detail below;
④ The change in the intrinsic value of options (otherwise known as the “moneyness” level) increases or decreases the PNV. If an option goes further in the money, the intrinsic value is higher and benefits option holders. Hence, the PNV would decrease. If the option goes further out of the money, the intrinsic value of the options exposure printed by the pool would be lower and thus the PNV would be higher because the pool, acting as counterparty, would have reduced obligations;
⑤ Exercising options leads to a cash settlement that decreases PNV;
⑥ Selling options to the pool allows options holders to receive consideration from the pool and leads to the termination of the options contract, which in turn decreases PNV; (Currently disabled in v1.0)
⑦ The change in USD value of the USDC token increases or decreases PNV.


**Calculating Pool Net Value**

With the principles above, we can put the Pool Net Value (PNV) at the time of T (NetValue(T)) into the following formula:

![](https://cdn-images-1.medium.com/max/2030/1*PCvtVgynlWfc2pXiibPcOA.png)

Where,

p(T) is the USD price of USDC at the time of T

N(T-1) is the number of USDC in the pool at the time of T-1

Input(T) is the number of USDC tokens that are input into the pool during the time between T-1 and T

Output(T) is the number of USDC tokens that are withdrawn out of the pool during the time between T-1 and T

Premium(T) is the USD amount of premium that should be distributed into the pool, during the time between T-1 and T. Please check the details of calculation in the ‘Options Premium Distribution’ section below

△IntrinsicValue(T) is the change of the intrinsic value of the existing options and the options that get exercised during the time between T-1 and T

Sellback(T) is the USD value of the options that are sold back to the pool by the option holders during the time between T-1 and T

## Collateralization Ratio (CR)

The Collateralization Ratio, abbreviated as CR, is the ratio (or percent) of the value of the collateral to the value of the asset which is being collateralized. Typically the ratio is defined using some *reference currency*. The term is common throughout both decentralized finance as well as traditional finance. the most commonly known example of collateralization ratios is the required amount of collateral needed to issue DAI using MakerDAO. See [MCR definition](/terminology/#minimum-collateralization-ratio-mcr) for a detailed example of CR and MCR with MakerDAO and other related applications.

CR = C * C<sup>rc</sup> / A * A<sup>rc</sup>

Where:

C = units of collateral assets "ex: 100,000 USDC"  
A = units of asset "ex: 38 ETH" 

C<sup>rc</sup> = price of one unit of collateral in the reference currency  "ex: $1.00"  
A<sup>rc</sup> = price of one unit of asset in the reference currency  "ex: 400"  
rc = referrence currency "ex: USD"  

CR = 100000 * 1.00 / 38 * 400 = 6.58 or 658%

## Minimum Collateralization Ratio (MCR)

The Minimum Collateralization Ratio (MCR) is the minimum required value of the  Collateralization Ratio (CR). Typically it is used to define the level of collateral needed to issue a synthetic currency such as MakerDAO's DAI or Synthetix's sUSD, or the level of collateral needed to issue some other type of synthetic asset. 

**Example 1: Issuing DAI with MakerDAO** 

MakerDAO is one of the most well-known and widely used defi appplications in the world. It allows users to generate a DAI token which is a synthetic asset meant to track the price of the US dollar. In order to issue new DAI, a user must lock up collateral which is higher in value than the amount of die they want to generate. ETH and other select assets are able to be used as collateral. MakerDAO requires that the value of the collateral is 150% or more than the value of the amount of DAI to be generated, or other words, that the Collateralization Ratio (CR) is not lower than 150%. ***In this case, 150% is the MCR.*** Values are defined using USD as a reference currency. Therefore, in order to generate 200 DAI, one must lock up at least 300 USD worth of ETH or other accepted collateral type. This ensures that there is always a sufficient value of collateral to back up the issued DAI in case the price of the collateral falls. If value of the collateral falls too close to the value of the synthetic asset that it backs (DAI), then it will be liquidated.

**Example 2: Writing Synthetic Option Contracts with Individual Writers** 

A simple method for writing options is for individual options writers to issue individual options contracts backed by crypto collateral, for example ETH. The ETH collateral is locked up when the options writer issues the option contract to the option buyer. The value of the collateral should be more than enough to complete the option buyer's settlement in case they successfully exercise their option contract.  
 
In case of a highly volatile underlying asset, the MCR should be set higher, since there is a greater chance that the settlement value could be quite high for a volatile asset. 

For example, the minimum collateral requirement might be 500% the value of the option. In case that the underlying asset is SNX for example, we may set the MCR at 500% In order to guarantee that regardless of large price changes for SNX, the option buyer can always successfully exercise their option. For an underlying asset such as USDC, however, the MCR may be set as low as 110%, since USDC has a very low volatility, and even given the most extreme historical price changes, 110% collateral should be more than enough to exercise the option. 

**Example 3:  Writing Options with PPO v1.0** 

In contrast to PPO v0.1, PPO v1.0 uses the MASP (multi-asset single pool) model. In this model, multiple users contribute collateral in the form of a an approved asset such as USDC to a single pool for that collateral type. Users who wish to purchase options may then purchase them through the PPO interface. The entire MASP collateral pool acts as the counterparty, not any single liquidity provider. 

While there is no single counterparty to the option buyer in v1.0, we must still make sure that there is always enough collateral to settle the contract should the option buyer choose to exercise their option. Therefore, the MCR is defined for the entire pool, not for individual option contract. Since different assets all have different rates of volatility, different MASP pools with different collateral types will have different MCRs. 

For example, for the pool with volatile cryptoassets, the MCR maybe be as high as 500%, while for the USDC pool, it may be only 120%. This is because as a stable coin, USDC is expected to hold its price much better than a volatile coin. A MCR of 500% means that once the ratio of value of issued options to the value of collateral in the MASP pool falls below 500%, new options may no longer be issued. So, for example, if there is 1,000,000 USD worth of a volatile asset in a MASP pool, It would mean that up to 200,000 USD worth of options may be issued.

## Chill Time

DeFi is still at a nascent experimental stage. We witnessed a number of exploits in the past, among which a great proportion are done though flash loans. These instant uncollateralized loans enable attackers to make nearly risk-free trials to hack decentralized protocols with little capital requirements and low costs beyond Ethereum gas fees and the time to research the potential exploit.

However, flash loans require that all assets borrowed should be returned before the end of the transaction, in the same mined block.

To protect against possible flash loan exploits in PPO v1.0, a special mechanism called ‘Chill Time’ is designed, during which the options buyers cannot sell or exercise the options, and the pool participants cannot withdraw their assets out of the pool. ‘Chill Time’ is set to be one hour.