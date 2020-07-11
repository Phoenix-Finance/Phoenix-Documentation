# FPO v0.1 Smart Contracts Overview

This document contains details about the Finnexus Protocol for Options (FPO). This document outlines the complete protocol, and includes descriptions of aspects of the protocol which have yet to be completed. FPO is at its core composed of a collection of smart contracts. Some of them concern the core options process, while others are for liquidity and rewards. The following diagram shows how they communicate in general: 

![](../img/options/options15.png "FPO smart contracts")
<center>*FPO smart contracts*</center>
<br>

## Core Components

| Name            | Source                  | ABI                     |
|-----------------|-------------------------|-------------------------|
| Options Manager | [ManagerContract\.sol](https://github.com/FinNexus/OptionsContract/blob/master/contracts/ManagerContract.sol)| ManagerContract\.abi    |
| Options Formula | [OptionsFormulas\.sol](https://github.com/FinNexus/OptionsContract/blob/master/contracts/OptionsFormulas.sol)| OptionsFormulas\.abi    |
| Compound Oracle | [CompoundOracle\.sol](https://github.com/FinNexus/OptionsContract/blob/master/contracts/CompoundOracle.sol)| CompoundOracle\.abi     |
| Trading Orders  | [MatchMakingTrading\.sol](https://github.com/FinNexus/OptionsContract/blob/master/contracts/MatchMakingTrading.sol)| MatchMakingTrading\.abi |
| Options Token   | [IERC20\.sol](https://github.com/FinNexus/OptionsContract/blob/master/contracts/IERC20.sol)| IERC20\.abi             |

## Options Manager Contract

Responsibilities

* Manages underlying assets and collateral
* Creates and manages option types
* Issues additional option token supply
* Liquidation 
* Exercising
* Setting transaction fee rate
* Interacts with others contracts

This is the main contract for FOB 1.0 which is composed of a number of sub contracts. It runs all functions directly related to options. It gets token price information from the compound oracle contract to run necessary calculations. It also triggers the deployment of new options token contracts and issues new options tokens when all conditions are fulfilled. It handles calculation of collateral coverage, liquidation and exercising. Calculations are performed using the formulae defined in the options formula contract. 

