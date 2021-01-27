# FNX mining

Currently there are two ways to mine FNX:

1. Uniswap liquidity mining
1. FinNexus Protocol for Options (FPO) liquidity mining

## FPO Liquidity Mining

The basic principle of FPO liquidity mining is that users first supply liquidity to the FPO platform, and in return, receive FPT tokens which represent their share of the FPO liquidity pool. Users then stake their FPT tokens in the FPO mining contract to earn rewards for providing liquidity. There are various ways to increase the level of rewards from mining. Read below to learn how to maximize your rewards.

### Mining Program on Ethereum

*Note: the FPT-USDC/USDT refers to the pool share token in the USDC/USDT Pool (USDT is included as additional collateral on this update), while FPT-FNX indicates the pool share token in the FNX Pool.

#### Basic Mining

+ Both USDC/USDT and FNX contributors in the USDC/USDT and FNX liquidity pools can participate in FNX mining, by simply staking FPT-USDC/USDT or FPT-FNX* pool share tokens in the mining contract.
+ Each user’s mining power is calculated according to her/his amount of  FPT-USDC/USDT or FPT-FNX tokens staked.
+ Each FPT-USDC/USDT or FPT-FNX counts as 1 point, while a group of overlapping FPT-USDC/USDT and FPT-FNX is considered 20 points.
+ The goal of the mining system is to increase the Total Value Locked (TVL) in the FinNexus Protocol for Options (FPO), especially in the USDC/USDT pool. When calculating the overlapping FPT-USDC/USDT and FPT-FNX groups, different weights will be given to the two FPT tokens, with FPT-USDC/USDT scoring 10 times higher than FPT-FNXs.
+ The share/weight of a miner is calculated as his/her mining score divided by the total score of all miners.
+ The total basic mining reward is set to be 20,000 FNX/Day.
+ FPT-FNX is required to be locked for a minimum period of 15 days to participate in basic mining. FPT-USDC/USDT does not require to be locked.

#### Mining Calculations

*User’s mining score = amt of FPT-USDC/USDT + amt of FPT-FNX + min(amt of FPT-USDC/USDT, 10×amt of FPT-FNX)×20
Share of a miner = one’s mining score / total score of all miners
Basic mining Amt = Total Basic Reward × Share of a miner
Total Basic Reward = 20,000 FNX/Day*

#### Boosting

+ A reward multiplier is added to the basic mining amount.
+ The longer one locks FPT-FNX, the higher the boost will be. (See table below.)
+ The minimum locking time for assets is 15 days, guaranteeing a 1x multiplier. After that, there is no lockup requirement and FPT-FNX can be transferred or removed at any time.
+ Once a choice is made, the locking period can only be increased but not decreased.
+ The reward multiplier decays as time moves forward. For example, assuming an investor locks FNX for 6 months, after 3 months, the reward multiplier decays from 6 to 5.
+ FPT-USDC/USDT does not require locking.

|locking period|15 days|3 months|6 months|9 months|12 months|15 months|18 months|
| --- | --- | --- | --- | --- | --- | --- | --- |
|reward multiplier|1|5|6|7|8|9|10|
|locking period|21 months|24 months|27 months|30 months|33 months|36 months||
|reward multiplier|11|12|13|14|15|16||

#### Boosting Calculations

*Total mining Amt = Basic mining Amt × reward multiplier*

#### Notes

+ All FNX mined will be vested and linearly released in 6 months.
+ cFNX tokens will be minted and can be claimed anytime as a voucher for mining rewards.
+ cFNX tokens are transferable on the market.
+ cFNX can be transferred to FNX at a 1:1 ratio.
+ Once sent to the conversion contract, cFNX will be burnt and ⅙ FNX can be claimed monthly in 6 months.

#### Summary

+ Greatly increases mining incentives compared with the current plan.
+ Creates a joint mining pool with new mining contracts for both the USDC/USDT and FNX pool.
+ Encourages simultaneous contributions to both pools with higher mining rewards.
+ Introduces a reward multiplier according to the lockup period in the FNX pool.
+ All FNX mining incentives will be vested and linearly released in 6 months.

### New Mining Program on Wanchain

The new mining program on Wanchain will apply a similar mechanism to the one proposed for Ethereum and described above.

![](https://i.imgur.com/Jhsuqyn.jpg)

However, please bear in mind:

+ The WAN/FNX pool on Wanchain will be equivalent to the FNX pool on Ethereum.
+ The stablecoin pool (wanUSDT Pool) on Wanchain will be equivalent to the USDC/USDT pool on Ethereum.
+ The total basic mining reward is set to be 2,000 FNX/Day.

## [Uniswap liquidity mining](https://www.docs.finnexus.io/products/liquidity/)

The FinNexus Options Liquidity Mining DApp rewards participants with extra FNX for providing liquidity to the [FNX/ETH Uniswap Pool](https://uniswap.info/pair/0x722885cab8be10b27f359fcb225808fe2af07b16).

Visit the [mining UI](https://liquidity.finnexus.io). With the UNI-V2 tokens you get from providing liquidity to the [FNX/ETH Uniswap Pool](https://uniswap.info/pair/0x722885cab8be10b27f359fcb225808fe2af07b16), enter the amount of FNX/ETH UNI-V2 tokens you want to stake from your wallet. Once you have completed this step, you will begin to accrue FNX rewards.

Please refer to the content [here](https://www.docs.finnexus.io/products/liquidity/) and [here](https://medium.com/finnexus/migrating-to-uniswap-liquidity-mining-phase-2-15e98a4e7bc2) for further information.

