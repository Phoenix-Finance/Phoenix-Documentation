# FinNexus FNX Token API v0.1 Alpha

*Note: API is still under development and routes were changed on July 29th, 2020. The original routes still work but we recommend you use the new routes listed below. Also note that the domain name is subject to change. Any changes will be noted here and in API error messages until the official release of the 1.0 API.*

This is an API for getting data about the FNX token and the FinNexus Options Protocol on the Wanchain blockchain.

## API URL

[https://fnx-api.herokuapp.com/api/v1](https://fnx-api.herokuapp.com/api/v1)

The API makes use of Web3 to interact directly with the blockchain and also uses smart contract ABIs to connect with smart contract addresses and get access to their functions and events. 

A single route at `/api/v1` returns all of the API data, while individual pieces of data may also be queried at the specific routes listed below.

## Full Info Routes
*These routes return raw values, formatted values, and other associated information as a simple JSON object.*

### `Get all token data:` 

> [`GET https://fnx-api.herokuapp.com/api/v1`](https://fnx-api.herokuapp.com/api/v1)

### `Max supply:`
> [`GET https://fnx-api.herokuapp.com/api/v1/maxAmount`](https://fnx-api.herokuapp.com/api/v1/maxAmount) 

### `Minted FNX:`
> [`GET https://fnx-api.herokuapp.com/api/v1/minted`](https://fnx-api.herokuapp.com/api/v1/minted)

### `Current total supply:`
> [`GET https://fnx-api.herokuapp.com/api/v1/currentTotalSupply`](https://fnx-api.herokuapp.com/api/v1/currentTotalSupply) 

### `Operational reserves:`
> [`GET https://fnx-api.herokuapp.com/api/v1/opReserves`](https://fnx-api.herokuapp.com/api/v1/opReserves)    

### `Team and founding investors:`
> [`GET https://fnx-api.herokuapp.com/api/v1/teamAndFounders`](https://fnx-api.herokuapp.com/api/v1/teamAndFounders) 

### `Community rewards:`
> [`GET https://fnx-api.herokuapp.com/api/v1/communityRewards`](https://fnx-api.herokuapp.com/api/v1/communityRewards)

### `Institutional investors:`
> [`GET https://fnx-api.herokuapp.com/api/v1/institutional`](https://fnx-api.herokuapp.com/api/v1/institutional) 

### `Burnt FNX:`
> [`GET https://fnx-api.herokuapp.com/api/v1/burned`](https://fnx-api.herokuapp.com/api/v1/burned)    

<!-- ### `Converted FNX:`
> [`GET https://fnx-api.herokuapp.com/api/v1/converted`](https://fnx-api.herokuapp.com/api/v1/converted) -->

### `FNX Circulating Supply:` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fnxCirculatingSupply`](https://fnx-api.herokuapp.com/api/v1/fnxInCirculation)

### `FNX locked in FPO:`
> [`GET https://fnx-api.herokuapp.com/api/v1/lockedFnx`](https://fnx-api.herokuapp.com/api/v1/lockedFnx)    

### `FNX in circulation with locked FNX deducted:` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fnxInCirculationDeducted`](https://fnx-api.herokuapp.com/api/v1/fnxInCirculationDeducted)

### `Current total supply of FNX on Ethereum:` 
> [`GET https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupply`](https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupply)

### `Current total supply of FNX on Wanchain:` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupply`](https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupply)



## FinNexus Protocol For Options (FPO) Routes
*These return information about FPO.*

 
### `FPO total value locked on all chains` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fpoTvl`](https://fnx-api.herokuapp.com/api/v1/fpoTvl)

### `FPO total value locked on Wanchain` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fpoTvlEth`](https://fnx-api.herokuapp.com/api/v1/fpoTvlEth)

### `FPO total value locked on Ethereum` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fpoTvlWan`](https://fnx-api.herokuapp.com/api/v1/fpoTvlWan)

### `FPO WAN total value on Wanchain pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wan_wanPoolTotalValue`](https://fnx-api.herokuapp.com/api/v1/wan_wanPoolTotalValue)

### `FPO FNX total value on Wanchain pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wan_fnxPoolTotalValue`](https://fnx-api.herokuapp.com/api/v1/wan_fnxPoolTotalValue)

### `FPO FNX total value in FNX Ethereum Pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/eth_fnxPoolTotalValue`](https://fnx-api.herokuapp.com/api/v1/eth_fnxPoolTotalValue)

### `FPO USDC total value in USDC Ethereum Pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/eth_usdcPoolTotalValue`](https://fnx-api.herokuapp.com/api/v1/eth_usdcPoolTotalValue)

### `FPO WAN total amount on Wanchain pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wan_wanPoolTotal`](https://fnx-api.herokuapp.com/api/v1/wan_wanPoolTotal)

### `FPO FNX total amount on Wanchain pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wan_fnxPoolTotal`](https://fnx-api.herokuapp.com/api/v1/wan_fnxPoolTotal)

### `FPO FNX total amount in FNX Ethereum Pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/eth_fnxPoolTotal`](https://fnx-api.herokuapp.com/api/v1/eth_fnxPoolTotal)

### `FPO USDC total amount in USDC Ethereum Pool` 
> [`GET https://fnx-api.herokuapp.com/api/v1/eth_usdcPoolTotal`](https://fnx-api.herokuapp.com/api/v1/eth_usdcPoolTotal)


## Raw Number Routes 
*These routes return raw numebrs only, as required for consumption by certain other APIs.*

### `Current total supply of FNX (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/currentTotalSupplyRaw`](https://fnx-api.herokuapp.com/api/v1/currentTotalSupplyRaw)

### `Current total supply of FNX Decimal Conversion (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/currentTotalSupplyRawDecimals`](https://fnx-api.herokuapp.com/api/v1/currentTotalSupplyRawDecimals)

### `FNX in circulation (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fnxInCirculationRaw`](https://fnx-api.herokuapp.com/api/v1/fnxInCirculationRaw)

### `FNX in circulation Decimal Conversion (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/fnxInCirculationRawDecimals`](https://fnx-api.herokuapp.com/api/v1/fnxInCirculationRawDecimals)

### `Current total supply of FNX on Ethereum (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupplyRaw`](https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupplyRaw)

### `Current total supply of FNX on Wanchain (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupplyRaw`](https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupplyRaw)

### `Current total supply of FNX on Ethereum Decimal Conversion (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupplyRawDecimals`](https://fnx-api.herokuapp.com/api/v1/ethCurrentTotalSupplyRawDecimals)

### `Current total supply of FNX on Wanchain Decimal Conversion (Raw Number):` 
> [`GET https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupplyRawDecimals`](https://fnx-api.herokuapp.com/api/v1/wanCurrentTotalSupplyRawDecimals)