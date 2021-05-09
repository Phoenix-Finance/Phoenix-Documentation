# On the Risks in FPO v1.0

Before ‘jumping into the pool’ or starting buying options on the FPO v1.0, it is important to understand the potential risks of the protocol for every user. The liquidity/collateral pool is not risk-free, and participants can lose money/

The risks below are presented in no particular order.

## 1. Risks for pool participants

### (1) Option concentration risk

Options are contracts that give the buyers the right to buy or sell assets at a fixed price in a certain period. Therefore, options sellers/writers only have an obligation but paid with a premium (option price). Different from lending money and rewarded with interest, options sellers should deposit collateral for the performance and may lose money.

MASP (Multi-Asset Single-Pool) is the key mechanism FinNexus introduced in the FPO v1.0 model. The liquidity pool or collateral pool acts as the single counterparty for writing, trading, and exercising all of the options contracts. Hence, the pool is the joint options seller. The key to the pool is to have many different options live and dilute the risks exposed by a single option contract.

However, if the options are not adequately diversified, for example, some large option buyers drained the pool’s liquidity, with options of similar terms, the risks for the pool can be quite concentrated. This is more likely when the pool is small.

### (2) Unilateral market move risk

The nature of risk-return profiles is different between the option sellers and buyers. It is often regarded that the sellers have limited returns but unlimited risks. One of the goals in MASP is to diversify the ‘unlimited’ risks by pooling all options together. The market is always filled with different expectations and the more conflicting it may be, the more favorable it is for the pool.

However, even when the pool is in a relatively balanced status, in cases of extreme unilateral price moves, the gains in the pool may not be enough to compensate for the losses when option holders exercising the ITM options.

### (3) Multi-asset composition risks 

(in the official release of FPO v1.0 on Ethereum, it is changed to pools with single assets, therefore, this risk has been eliminated on Ethereum Pools, but still exists on Wanchain)

FPO v1.0 on Wanchain has a hybrid pool, that accepts WAN and FNX as accepted collateral in the options liquidity pool. The liquidity pool works like a mutual fund, where after transferring the crypto assets in the pool, you are holding the equivalent shares and entitled to benefits as measured in FPT( FinNexus Pool Token). All the values in the pool are calculated in USD, therefore, the net value of the share, as FPT, will be subject to the changes of the USD price of these assets.

For example, in all pool with an equal composition of WAN and FNX, with no other P&L in the pool, if the value of FNX increases by 30%, while WAN increases by 10%, for FNX participants, he/she may get less amount FNX by withdrawing, as the gains are diluted; and for WAN participants, he/she will get some FNX as gains due to the increase of net value in the pool, just like in a mutual fund.

### (4) Liquidity risks

To maintain the security of FPO, FinNexus introduces the minimum collateral ratio (MCR) in the protocol, to make sure the option contracts are always fully-collateralized. The MCR for WAN, USDC, and FNX is set to be different, 500%, 120%, and 500% respectively. For example, $100 of FNX in the pool can only have 20$ as collateral for writing options.

In cases when the collateral in the pool is fully occupied, pool withdrawal will be paused. Also, the liquidity pool will cease to write new option contracts, until the collateral utilization ratio recovers to be above the MCUR level. Therefore, the withdrawal request will be marked as ‘pending’, until the portal reopens as stated above. The pool participants may have to wait to withdraw their shares of assets out of the pool and suffer from the pool liquidity risks.

Also, to protect against possible flash loan exploits, a pool participant can only quit the pool one hour after making the initial deposit.

## 2. Risks for option buyers

### (1) Multi-asset consideration and settlement risks

FPO v1.0 has provided friendly choices for option buyers by setting their customized option terms when buying options, including a selection of currencies to pay. However, different from the pools with single asset on Ethereum, the pool on Wanchain is in a hybrid form with both WAN and FNX as the acceptable assets. This liquidity pool is the sole counterparty for all options. When selling or exercising options, the holder is trading against the pool, therefore, the crypto assets as consideration or settlement are transacted from the compositions in the pool. Due to the pool’s multi-asset nature, when selling or exercising options, users will get a basket of tokens that reflects the current composition of these assets (WAN/FNX) in the pool. Therefore, users will get risk exposure to the crypto assets in the pool.

### (2) Options of American type

Options on FPO v1.0 are all American types and options holders should exercise in-the-money options manually. Please do remember to exercise your ITM options, or you will lose your profits upon expiration.

## 3. Smart contract risks

Though the code audit of FPO v1.0 is [done in Dec 2020 by Peckshield](https://github.com/FinNexus/Pdfs/blob/master/PeckShield-Audit-FinnexusOptionsV1.0.pdf), the whole DeFi is still in the early and experimenting stage. Please keep cautious of the smart contract risks and do not put your life savings inside. 

## 4. Oracle risks

FinNexus has partnered with Chainlink, the leading decentralized blockchain data provider for bringing off-chain data to smart contracts on Ethereum and other blockchains. FPO v1.0 applies decentralized price feeds of crypto asset pairs on Ethereum, provided by ChainLink.

Chainlink is a decentralized oracle network that enables smart contracts to securely access off-chain data feeds, web APIs, and traditional bank payments. It is well known for providing highly secure and reliable oracles.

Also, FinNexus is cooperating with Band Protocol for price feeds on Wanchain.

Nevertheless, oracles and external price data aggregation can be considered as a potential risk to the stability of the FPO.
