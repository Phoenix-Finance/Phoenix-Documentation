# FNX mining

Currently there are two ways to mine FNX:

1. FinNexus Protocol for Options (FPO) liquidity mining
1. Sushiswap liquidity mining and PancakeSwap liquidity mining

## FPO Liquidity Mining

The basic principle of FPO liquidity mining is that users first supply liquidity to the FPO platform, and in return, receive FPT tokens which represent their share of the FPO liquidity pool. Users then stake their FPT tokens in the FPO mining contract to earn rewards for providing liquidity. There are various ways to increase the level of rewards from mining. Read below to learn how to maximize your rewards.

### Mining Program on Ethereum and Binance Smart Chain (BSC)

*Note: the FPT-USDC/USDT refers to the pool share token in the USDC/USDT Pool, while FPT-FNX indicates the pool share token in the FNX Pool. Similarly, on BSC, we have a BUSD/USDT Pool.
A Frax Pool was added as an experimental pool in Q1 2021 on Ethereum.


#### Basic Mining
We take the USDC/USDT and FNX pools as an example in this guide. The same rule applies to other pools and on BSC and Wanchain.

+ Both USDC/USDT and FNX contributors in the USDC/USDT and FNX liquidity pools can participate in FNX mining, by simply staking FPT-USDC/USDT or FPT-FNX* pool share tokens in the mining contract.
+ Each user’s mining power is calculated according to her/his amount of  FPT-USDC/USDT or FPT-FNX tokens staked.
+ Each FPT-USDC/USDT or FPT-FNX counts as 1 point, while a group of overlapping FPT-USDC/USDT and FPT-FNX is considered 20 points.
+ The goal of the mining system is to increase the Total Value Locked (TVL) in the FinNexus Protocol for Options (FPO), especially in the USDC/USDT pool. When calculating the overlapping FPT-USDC/USDT and FPT-FNX groups, different weights will be given to the two FPT tokens, with FPT-USDC/USDT scoring 10 times higher than FPT-FNXs.
+ The share/weight of a miner is calculated as his/her mining score divided by the total score of all miners.
+ FPT-FNX is required to be locked for a minimum period of 15 days to participate in basic mining. FPT-USDC/USDT does not require to be locked.

#### Mining Calculations

*User’s mining score = amt of FPT-USDC/USDT + amt of FPT-FNX + min(amt of FPT-USDC/USDT, 10×amt of FPT-FNX)×20
Share of a miner = one’s mining score / total score of all miners
Basic mining Amt = Total Basic Reward × Share of a miner
Total Basic Reward = 20,000 CFNX/Day*
+ The total basic mining reward on Ethereum is set to be 20,000 FNX/Day, and begin halving in every 6 months from 2021-04-01.
+ The total basic mining reward on BSC is set to be 15,000 FNX/Day, and following the same halving rule as above.

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

Please note that on BSC, the longest lock-up period for FNX is 6 months, and the largest reward multiplier is 6x.

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

### Mining Program on Wanchain

The new mining program on Wanchain will apply a similar mechanism to the one proposed for Ethereum and described above.

![](https://i.imgur.com/Jhsuqyn.jpg)

However, please bear in mind:

+ The WAN/FNX pool on Wanchain will be equivalent to the FNX pool on Ethereum.
+ The stablecoin pool (wanUSDT Pool) on Wanchain will be equivalent to the USDC/USDT pool on Ethereum.
+ The total basic mining reward is set to be 500 CFNX/Day.

## Sushiswap Liquidity Mining

Following a favorable community vote, FinNexus is starting a new liquidity mining program on Sushiswap on February 10, 2021, with 3000 CFNX as daily mining rewards, changed to 10000 CFNX from 1st April 2021.

Incentives will be paid in convertible FNX (CFNX), which can be exchanged 1:1 to FNX.

Liquidity mining on Uniswap will end at the same time.

Please be aware that in order to convert, users must send the cFNX to the conversion contact. Afterward, 1/6th of the total cFNX burnt will be added to the user's redeemable FNX once a month over the following 6 months. The user may choose to redeem their FNX either once every month, or may choose to wait until they have accumulated enough and redeem it all together.

### How to mine Sushi and FNX together?

![](https://i.imgur.com/Sn3bmco.png)

A notice will pop up once you open the [FinNexus Options UI](options.finnexus.io). This will take you to the [Sushi Onsen Program](https://app.sushi.com/pair/0xaa500101c73065f755ba9b902d643705ef2523e3).

By contributing liquidity to the FNX/ETH pair and staking in the Onsen Farming Program, you will be automatically eligible for both Sushi and FNX rewards.

![](https://i.imgur.com/zDQf4mH.png)

Sushi rewards can be claimed on the [Sushi Onsen page](https://www.sushiswap.fi/farms/special) by navigating to the FNX/ETH pair. Please note that the Sushi rewards will be vested according to [the Sushi farming rules](https://docs.sushiswap.fi/products/yield-farming/the-sushi-menu).

![](https://i.imgur.com/TEwOp8B.png)

FNX rewards can be claimed on the 1st day of every month from our UI pop-ups.

The FinNexus team reserves the right to adjust the FNX mining rewards monthly according to the liquidity in the Sushiswap liquidity pool.

