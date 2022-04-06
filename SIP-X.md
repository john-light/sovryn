---
SIP: 'N/A'
Title: Accepting ownership of Sovryn contracts
Author: John Light (@john-light)
Status: Draft
Track: Contract
Created: 2022-03-31
---

# SIP-X: Accepting ownership of Sovryn contracts  

## Description  

If approved, this proposal will result in the on-chain acceptance by SOV stakers of the ownership of the Sovryn AMM.

Furthermore, this proposal will result in a signal from SOV stakers that they are willing to accept the ownership of the following Sovryn smart contracts and admin roles, to be transferred by the Exchequer Multisig no later than `2022-04-30 23:59:59 UTC`:

|	Category        	| Contract name	              | Role  |
| ----------------- |:---------------------------:|:-----:|
| LoanToken Modules |	                            | 	    |
|                   |	LoanTokenLogicLM            | Owner	|
|                   |	LoanTokenLogicWRBTC         | Owner	|
|                   |	LoanTokenSettingsLowerAdmin | Owner	|
| Protocol          |	                            |       |
|                   |	Affiliates                  | Owner	|
|                   |	LoanClosingsLiquidation     | Owner	|
|                   |	LoanClosingsRollover        | Owner	|
|                   |	LoanClosingsWith            | Owner	|
|                   |	LoanMaintenance             | Owner	|
|                   |	LoanOpenings                | Owner	|
|                   |	LoanSettings                | Owner	|
|                   |	ProtocolSettings            | Owner	|
|                   |	SwapsExternal               | Owner	|
| Other             |                             |       |
|                   |	Liquidity Mining            | Owner	|
|                   |	StakingRewards              | Owner	|
|                   |	VestingLogic                | Owner	|
|                   |	Modules                     | Admin	|
| Connectors        |                             |       |
|                   |	LoanToken                   | Admin	|
|                   |	LoanTokenLogicBeacon        | Admin	|
|                   |	LoanTokenSettingsLowerAdmin | Admin	|
|                   |	LoanTokenLogicStandard      | Admin	|
| Core              |	                            |     	|
|                   |	Protocol                    | Admin	|
| Oracles           |	                            |     	|
|                   |	BPro Price Feed             | Admin	|
|                   |	RSK Price Feed              | Admin	|
|                   |	MoC Price Feed              | Admin	|
|                   |	Price Feeds Gateway         | Admin	|
|                   |	PriceFeedV1PoolOracle       | Admin	|
| Governance        |	                            |      	|
|                   | SOV                         | Admin |
|                   | Locked SOV                  | Admin |
|                   | FeeSharingProxy             | Admin |
|                   | Staking                     | Admin |
|                   | StakingRewards              | Admin |
|                   | Origin Investor Claim       | Admin |
|                   | Token Sender                | Admin |
|                   | Vesting Registry            | Admin |

## Motivation



## Proposed change

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
