# Phoenix Rewarding and Boosting System

In order to achieve sustainable ecological development, Phoenix Finance's mining mechanism aims to reward contributors in a long-term and stable manner. These contributors include but are not limited to users who provide liquidity for Phoenix DeFi options and leveraged tokens, those who provide liquidity on Dexes, reciprocal rewards for partners, and more. These rewards will be distributed from the PHX community reserves. 
## Incentives for Providing Liquidity for Phoenix Products
Liquidity is the key to any DeFi protocol. Decentralized derivatives need deep liquidity to power the trading volume and lower slippages, and the product liquidity mining reward will be a long-term incentive measure. 
### Pools
Phoenix Finance is launching the following liquidity pools for options and leveraged token products with cPHX as incentives:

 - USDC/USDT options pools on Polygon, BSC and Wanchain 
 - USDC lending pools for leveraged tokens on Polygon and BSC 
 - WBTC lending pools for leveraged tokens on Polygon and BSC  
 - ETH lending pools for leveraged tokens on Polygon and BSC

For the options pool, other stable coins will be added as collateral assets in the future. For any newly added leveraged token, there will be an additional lending pool with its related underlier. For instance, a $MATIC lending pool will be established when launching $MATIC leveraged tokens and so forward.
### Mining Incentives
#### Basic Rewards
Basic rewards are incentives for liquidity providers contributing collateral assets.
When a user deposits collateral assets into the relevant pools, he/she will receive pool tokens, representing a share of the pool and be rewarded accordingly. Rewards will be calculated in each block.

*Basic Rewards = Total Basic Rewards × Share of the Pool.* 

#### Boosted Rewards
Boosted rewards are incentives for miners staking PHX or cPHX in the contracts, meaning users can stake PHX or cPHX in the boosting contracts to enhance the basic mining rewards. 

*Boosted Rewards = Basic Rewards × Multiplier*

The more PHX or cPHX is staked, the higher the multiplier will be. Likewise, the longer the time PHX or cPHX is staked for, the more substantial the returns. 

The multiplier is derived by the following formula.

*multiplier=[0.004×(N/500)^0.3 + 0.0067×(N/500)^0.25 ]×(T-1)+(N/500)^0.05*

In which N is the effective staking amount, and T is the number of months in lockup. Staking 1 PHX or 1 cPHX means N=1.

Please note that you have to stake enough PHX or cPHX so that N is no smaller than 500, to have an effective multiplier, which is greater than 1.

For example, if locking your tokens for 6 months, the multiplier chart against the PHX locked amount will shape as follows:
![](https://z3.ax1x.com/2021/08/08/flay1U.png)
For example, if locking 50,000 PHX tokens, the multiplier chart against the lock time will shape as follows:
![](https://z3.ax1x.com/2021/08/09/f13WO1.png)

Please also note that the boosting effect will decrease on a monthly basis. E.g., a user staking PHX for 6 months will have a 5-month boosting effect after 1-month period. However, one can always increase his/her lockup time by one month to have a constant boost in every month.

### Miscellaneous
#### Boosting designation
If a user has boosted rewards in a pool, the reward enhancement can be transferred to other pools at any time. You can transfer the multiplier or the boosting re-designation by moving the locked PHX or cPHX (vePHX) between pools. A partial transfer is also possible. 

For example, Alice is contributing USDC and ETH in the USDC and ETH lending pools for leveraged tokens. She is also staking all of her PHX holdings and boosting the rewards in the USDC lending pool. At any time, she may choose to designate part or all of the vePHX as the booster for the ETH pool. After the re-designation, the boosting in the USDC pool will decrease, while the boosting in the ETH pool will increase. 
#### cPHX
All incentives are distributed in cPHX, or convertible PHX. cPHX can be converted to PHX at an equal ratio. Once converted to PHX, the cPHX is burned and it entitles the holder to claim ⅙ of the PHX every 30 days. The first ⅙ of the PHX will be released immediately. cPHX can be also staked as a booster, with the same boosting effect as PHX.

#### vePHX
Both PHX and cPHX, once staked as reward boosters, are called vePHX. The vePHX lock-time is the same in each address, even if they are powering different pools. In other words, if a user adjusts the vePHX lock period in a pool, the lock time in all pools will be adjusted. The vePHX lock time can only be extended, not shortened.

#### Boosting Impact
vePHX only affects the rewards after boosting and does not change the basic rewards. The basic rewards solely depend on the amount of collateral assets one stakes. The boosting will not affect the withdrawal of the collaterals. 

The advantage of this mechanism is that users can flexibly adjust the pools they intend to boost in, according to the change of the basic rewards. 

### Returns in Native Collateral Assets
In addition to PHX rewards, in the long run, the native returns directly generated by the protocols are essential.
#### Options
Options pools collect liquidity from contributors, as the collective option sellers, who earn premiums from buyers. These premiums automatically accrue in the liquidity pools and accumulate over time. (Please notice that being an options seller entails risks, though these are diversified by varieties of outstanding options. Please check the product paper for more details.)

#### Leveraged Tokens
The pools powering leveraged tokens are lending pools. They generate interest income by lending assets to users who buy leveraged tokens. The income directly accumulates in the pools, which is reflected in the value of LP tokens. Please check the product paper for more details.

### Total returns from the Phoenix Protocols
*Returns in the options pools = Options Premiums (in collateral assets) + Basic Mining Rewards (in cPHX) + Boosted Rewards (in cPHX)

Returns in the lending pools for leveraged tokens = Interest for lending assets (in collateral assets) + Basic Mining Rewards (in cPHX) + Boosted Rewards (in cPHX)*

## Incentives for Providing Liquidity for PHX pairs in Dexes

There are incentives for providing liquidity for PHX pairs on Dexes on all four chains - Ethereum, Polygon, BSC and Wanchain. Rewards are distributed in cPHX. It suffices to stake the relative LP tokens in the mining contracts to be entitled to the mining rewards.

*Mining rewards on Dexes = Total Basic Rewards × Share of the Liquidity Pool.* 

However, please note that these mining incentives are not eligible for boosting.
 
## Reciprocal Rewards for Ecological Partners

Phoenix Finance intends to establish deep cooperative relations with relevant DeFi partners, providing mutually beneficial mining incentive schemes. These incentives will be drawn from the community reserves. Please follow our official channels for the latest announcements.
## Final Notes

The parts above constitute Phoenix's rewarding and boosting system. Since Phoenix Finance implements multi-chain deployment, the reward mechanisms do not specifically refer to one single chain, but in a more general manner across all chains. Specific mining rewards will be determined according to the live products on each chain.




