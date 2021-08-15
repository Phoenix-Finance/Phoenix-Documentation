# On the Risks in PPO v1.0

Before ‘jumping into the pool’ or starting trading options on PPO v1.0, it is important to understand the potential risks of the protocol for every user. The liquidity/collateral pool is not risk-free, and participants can lose money.

The risks below are presented in no particular order.

## 1. Risks for pool participants

### (1) Options concentration risk

Options are contracts that give the buyers the right to buy or sell assets at a fixed price in a certain period. Therefore, options sellers/writers only have an obligation but paid with a premium (option price). Different from lending money and rewarded with interest, options sellers should deposit collateral for the performance and may lose money.

MASP (Multi-Asset Single-Pool) is the key mechanism Phoenix introduced in the PPO v1.0 model. The liquidity pool or collateral pool acts as the single counterparty for writing, trading, and exercising all of the options contracts. Hence, the pool is the joint options seller. The key to the pool is to have many different options live and dilute the risks exposed by a single option contract.

However, if the options are not adequately diversified, for example, some large option buyers drained the pool’s liquidity, with options of similar terms, the risks for the pool can be quite concentrated. This is more likely when the pool is small.

### (2) Unilateral market move risk

The nature of risk-return profiles is different between the option sellers and buyers. It is often regarded that the sellers have limited returns but unlimited risks. One of the goals in MASP is to diversify the ‘unlimited’ risks by pooling all options together. The market is always filled with different expectations and the more conflicting it may be, the more favorable it is for the pool.

However, even when the pool is in a relatively balanced status, in cases of extreme unilateral price moves, the gains in the pool may not be enough to compensate for the losses when option holders exercising the ITM options.

### (3) Multi-asset composition risks 

PPO v1.0 may have hybrid pools, that accept multiple assets as accepted collateral in the options liquidity pool. The liquidity pool will somehow work like a mutual fund, where after transferring the crypto assets in the pool, you are holding the equivalent shares and entitled to benefits as measured in PPT( Phoenix Pool Token). All the values in the pool are calculated in USD, therefore, the net value of the share, as PPT, will be subject to the changes of the USD value of these collateral assets.

The PPO pools are made of one or several stable coins, whose value is more likely to remain stable and pegged to USD. But for example, in the USDT/USDC hybrid pools, in case that one stablecoin, say USDT, as the collateral asset losses its peg, it may lead to risks and losses to the PPO pool participants, even to the USDC contributors.

### (4) Liquidity risks

To maintain the security of PPO, Phoenix Finance introduces the minimum collateral ratio (MCR) in the protocol, to make sure the option contracts are always fully-collateralized. 

In cases when the collateral in the pool is fully occupied, pool withdrawal will be paused. Also, the liquidity pool will cease to write new option contracts, until the collateral utilization ratio recovers to be above the MCUR level. Therefore, the withdrawal request will be marked as ‘pending’, until the portal reopens as stated above. The pool participants may have to wait to withdraw their shares of assets out of the pool and suffer from the pool liquidity risks.

Also, to protect against possible flash loan exploits, a pool participant can only quit the pool one hour after making deposits.

## 2. Risks for option buyers

### (1) Multi-asset consideration and settlement risks

PPO v1.0 has provided friendly choices for option buyers by setting their customized option terms when buying options, including a selection of currencies to pay. With hybrid liquidity pools, like the USDC/USDT pool, for example, both of the two stablecoins are regarded as the collateral assets. This liquidity pool is the sole counterparty for all options.

When exercising options, the holder is trading against the pool, therefore, the crypto assets as consideration or settlement are transacted from the compositions in the pool. Due to the pool’s multi-asset nature, upon settlement, users will get a basket of tokens that reflects the current composition of these assets (USDC/USDT) in the pool. Therefore, users will get risk exposure to the crypto assets in the pool.

### (2) Options of American type

Options on PPO v1.0 are all American types and options holders should exercise in-the-money options manually. Please do remember to exercise your ITM options, or you will lose your profits upon expiration.

## 3. Smart contract risks

Though the code audit of PPO v1.0 is done in Aug 2021 by Peckshield, the whole DeFi is still in the early and experimenting stage. Please keep cautious of the smart contract risks and do not put your life savings inside. 

## 4. Oracle risks

Phoenix Finance has partnered with Chainlink, the leading decentralized blockchain data provider for bringing off-chain data to smart contracts on Ethereum and other blockchains. PPO v1.0 applies decentralized price feeds of crypto asset pairs on Ethereum, provided by ChainLink.

Chainlink is a decentralized oracle network that enables smart contracts to securely access off-chain data feeds, web APIs, and traditional bank payments. It is well known for providing highly secure and reliable oracles.

Nevertheless, oracles and external price data aggregation can be considered as a potential risk to the stability of the PPO.
