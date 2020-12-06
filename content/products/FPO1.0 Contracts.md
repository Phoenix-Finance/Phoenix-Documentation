# FPO Contracts Functions

This file is introduction of functions of FPO(FinNexus Protocols of Options). Functions are coded by Liquidity and deployed as smartcontracts on EVM.

All functions are combined by several contracts as the pictures below.

(Picture link)

#OptionsManager

This is the main contract for FPO 1.0 which runs functions directly related to users operate options. And it interacts with other related contracts.

**Responsibility**


- Deposits into the collateral pool
- Withdraws from the collateral pool
- Buys options
- Excercises options
- Inquires related information of options
- Interacts with others contracts

**API Overview**

*addCollateral()*

Descriptions: Deposits currency into the collateral pool

Subscribe: function addCollateral(address collateral,uint256 amount) nonReentrant notHalted public payable

Parameters: 



- The address of the collateral. 
- Unit256 amount

Return Values:


None

.....
# **CollateralPool** #
This Contract store funds depositted from users and supply inquirement service which is related with collateral. Excepting inquirement service the contract does not supply any functions outside.

**Responsibility**
- Stores funds depositted from users
- Inquires total amount of collateral
- Inquires amount of collateral belong to each user.
- Calculates amount when users deposit and withdraw from collateral pool

**API Overview**
......

# OptionsPool #

This contract stores all imformation of opitons and calculates collateral rate and net value of collateral.

**Responsibility**

- Stores information of all options
- Stores information of options on each address
- Calculate collateral which is used by writed options
- Calculate net value of collateral pool
- Management of lock period after writing opitons

**API overview**

....
 
# FPTCoin #

This contract is ERC20 which is for LP token(FPT) of collateral pool. Others contract inquire the amount of FPT token on each address.

**Responsibility**

- Produces, destroys and transfers FPT. These functions are controlled by related functions in MinePool contract
- Inquires amount of FPT on each address

**API overview**

# MinePool #

This contract controls functions related mining.

**Responsibility**
- Manages currency of mining
- Manages total amount of mining
- Withdraw mining rewards
- Inquire mining rewards

# OptionsPrice #

This contract calculates price of options. The BS fomula and oracles including Implied volatility are be used to calculate price of options when users buy contracts.

# ImpliedVolatility #

This contract calculates surface of implied volatility based on the data from Oracle

# FNXOracle #

This contract interact with others contracts outside