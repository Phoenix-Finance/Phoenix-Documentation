Pool Net Value measures the monetary (USD) value of all the options exposures currently in the liquidity pool. It is calculated on the basis of accrual accounting and, as a result, may not be equal to the sum of actual net inflows and outflows at any given time.

**What Affects Pool Net Value?**

We take the FNX pool for example. The other liquidity pools, like the USDC pool, follow the same principle as described below.

The total Pool Net Value (PNV) in USD is affected by the following:

① FNX deposits increase the PNV;

② FNX withdrawals decrease the PNV;

③ Receiving option premiums increases the PNV, with the caveat that the premiums accrue to the PNV over time as the options within the pool move towards maturity. This accrual mechanism is explained in more detail below;

④ The change in the intrinsic value of options (otherwise known as the “moneyness” level) increases or decreases the PNV. If an option goes further in the money, the intrinsic value is higher and benefits option holders. Hence, the PNV would decrease. If the option goes further out of the money, the intrinsic value of the options exposure printed by the pool would be lower and thus the PNV would be higher because the pool, acting as counterparty, would have reduced obligations;

⑤ Exercising options leads to cash settlement that decreases PNV;

⑥ Selling options to the pool allows options holders to receive consideration from the pool and leads to the termination of the options contract, which in turn decreases PNV;

⑦ The change in USD value of the FNX token increases or decreases PNV.

**Calculating Pool Net Value**

With the principles above, we can put the Pool Net Value (PNV) at the time of T (NetValue(T)) into the following formula:

![](https://cdn-images-1.medium.com/max/2030/1*PCvtVgynlWfc2pXiibPcOA.png)

Where,

p(T) is the USD price of FNX at the time of T

N(T-1) is the number of FNX in the pool at the time of T-1

Input(T) is the number of FNX tokens that are input into the pool during the time between T-1 and T

Output(T) is the number of FNX tokens that are withdrawn out of the pool during the time between T-1 and T

Premium(T) is the USD amount of premium that should be distributed into the pool, during the time between T-1 and T. Please check the details of calculation in the ‘Options Premium Distribution’ section below

△IntrinsicValue(T) is the change of the intrinsic value of the existing options and the options that get exercised during the time between T-1 and T

Sellback(T) is the USD value of the options that are sold back to the pool by the option holders during the time between T-1 and T
