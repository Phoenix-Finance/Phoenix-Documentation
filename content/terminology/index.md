# Terminology

The following includes terms commonly used within FinNexus applications, articles, and other media. These terms come from a variety of different fields such as traditional finance cryptocurrency, blockchain, and decentralized finance (DeFi).   

## Collateralization Ratio (CR)

The Collateralization Ratio, abbreviated as CR, is the ratio (or percent) of the value of the collateral to the value of the asset which is being collateralized. Typically the ratio is defined using some *reference currency*. The term is common throughout both decentralized finance as well as traditional finance. the most commonly known example of collateralization ratios is the required amount of collateral needed to issue DAI using MakerDAO. See [MCR definition](/terminology/#minimum-collateralization-ratio-mcr) for a detailed example of CR and MCR with MakerDAO and other related applications.

CR = C * C<sup>rc</sup> / A * A<sup>rc</sup>

Where:

C = units of collateral "ex: 1,000,000 FNX"  
A = units of asset "ex: 38 ETH" 
C<sup>rc</sup> = price of one unit of collateral in the reference currency  "ex: $00.10"  
A<sup>rc</sup> = price of one unit of asset in the reference currency  "ex: 400"  
rc = referrence currency "ex: USD"  

CR = 1000000 * 00.10 / 38 * 400 = 6.58 or 658%

## Minimum Collateralization Ratio (MCR)

The Minimum Collateralization Ratio (MCR) is the minimum required value of the  Collateralization Ratio (CR). Typically it is used to define the level of collateral needed to issue a synthetic currency such as MakerDAO's DAI or Synthetix's sUSD, or the level of collateral needed to issue some other type of synthetic asset, such as options contracts from the [FinNexus Protocol for Options (FPO)](/options). 

**Example 1: Issuing DAI with MakerDAO** 

MakerDAO is one of the most well-known and widely used defi appplications in the world. It allows users to generate a DAI token which is a synthetic asset meant to track the price of the US dollar. In order to issue new DAI, a user must lock up collateral which is higher in value than the amount of die they want to generate. ETH and other select assets are able to be used as collateral. MakerDAO requires that the value of the collateral is 150% or more than the value of the amount of DAI to be generated, or other words, that the Collateralization Ratio (CR) is not lower than 150%. ***In this case, 150% is the MCR.*** Values are defined using USD as a reference currency. Therefore, in order to generate 200 DAI, one must lock up at least 300 USD worth of ETH or other accepted collateral type. This ensures that there is always a sufficient value of collateral to back up the issued DAI in case the price of the collateral falls. If value of the collateral falls too close to the value of the synthetic asset that it backs (DAI), then it will be liquidated.

**Example 2: Writing Synthetic Option Contracts with Individual Writers** 

A simple method for writing options is for individual options writers to issue individual options contracts backed by crypto collateral, for example ETH. The ETH collateral is locked up when the options writer issues the option contract to the option buyer. The value of the collateral should be more than enough to complete the option buyer's settlement in case they successfully exercise their option contract.  
 
In case of a highly volatile underlying asset, the MCR should be set higher, since there is a greater chance that the settlement value could be quite high for a volatile asset. 

For example, the minimum collateral requirement might be 500% the value of the option. In case that the underlying asset is SNX for example, we may set the MCR at 500% In order to guarantee that regardless of large price changes for SNX, the option buyer can always successfully exercise their option. For an underlying asset such as USDC, however, the MCR may be set as low as 110%, since USDC has a very low volatility, and even given the most extreme historical price changes, 110% collateral should be more than enough to exercise the option. 

**Example 3:  Writing Options with FPO v1.0** 

In contrast to FPO v0.1, FPO v1.0 uses the MASP (multi-asset single pool) model. In this model, multiple users contribute collateral in the form of a an approved asset such as FNX to a single pool for that collateral type. Users who wish to purchase options may then purchase them through the FPO interface. When they purchase an option contract through the FPO interface, the entire MASP collateral pool acts as the counterparty, not any single liquidity provider (this is in contrast with the FPO v0.1 model described in the previous section, where for each option contract, there is a single writer on one side and a single buyer on the other). While there is no single counterparty to the option buyer in v1.0, we must still make sure that we obey the same basic principles described in v0.1 that ensure there is always enough collateral to settle the contract should the option buyer choose to exercise their option. The difference here is that the collateral is pooled, rather than individual. Therefore, the MCR is defined for the entire pool, not for individual option contract. Since different assets all have different rates of volatility, different MASP pools with different collateral types will have different MCRs. For example, for the FNX pool, the MCR maybe be as high as 500%, while for the USDC pool, it may be only 200%. This is because as a stable coin, USDC is expected to hold its price much better than a volatile coin such as FNX or ETH. A MCR of 500% means that once the ratio of value of issued options to the value of collateral in the MASP pool falls below 500%, new options may no longer be issued. So, for example, if there is 1,000,000 USD worth of FNX in a MASP pool, It would mean that up to 200,000 USD worth of options may be issued.
