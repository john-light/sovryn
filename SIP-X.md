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

If approved, this proposal will result in an on-chain state change transferring the administrator role in the Sovryn AMM smart contracts from the Exchequer Multisig to the GovernorAdmin contract controlled by SOV stakers.

Furthermore, this proposal will result in a signal from SOV stakers that they are willing and ready to accept the owner and/or adminstrator role in the following Sovryn smart contracts, to be transferred by the Exchequer Multisig no later than `2022-XX-XX 23:59:59 UTC`:

|	Category        	| Contract name	              | Role  | New governor                                                 |
| ----------------- |:---------------------------:|:-----:|:------------------------------------------------------------:|
| LoanToken Modules |	                            | 	    |                                                              |
|                   |	LoanTokenLogicLM            | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanTokenLogicWRBTC         | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanTokenSettingsLowerAdmin | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
| Protocol          |	                            |       |                                                              |
|                   |	Affiliates                  | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanClosingsLiquidation     | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanClosingsRollover        | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanClosingsWith            | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanMaintenance             | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanOpenings                | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	LoanSettings                | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	ProtocolSettings            | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	SwapsExternal               | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
| Other             |                             |       |                                                              |
|                   |	Liquidity Mining            | Owner	| GovernorOwner (`0x6496df39d000478a7a7352c01e0e713835051ccd`) |
|                   |	StakingRewards              | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	VestingLogic                | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	Modules                     | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
| Connectors        |                             |       |                                                              |
|                   |	LoanToken                   | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	LoanTokenLogicBeacon        | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	LoanTokenSettingsLowerAdmin | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	LoanTokenLogicStandard      | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
| Core              |	                            |     	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	Protocol                    | Admin	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
| Oracles           |	                            |     	|                                                              |
|                   |	BPro Price Feed             | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	RSK Price Feed              | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	MoC Price Feed              | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	Price Feeds Gateway         | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   |	PriceFeedV1PoolOracle       | Owner	| GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
| Governance        |	                            |      	|                                                              |
|                   | SOV                         | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | Locked SOV                  | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | FeeSharingProxy             | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | Staking                     | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | StakingRewards              | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | Origin Investor Claim       | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | Token Sender                | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |
|                   | Vesting Registry            | Admin | GovernorAdmin (`0xff25f66b7d7f385503d70574ae0170b6b1622dad`) |

## Motivation

Currently, all [upgradeable Sovryn smart contracts](https://docs.google.com/document/d/1gGY4Rua_FVBZCJCftzf14cD4c6kqg6VTr9g-9-uDCA0/edit), with the exception of Staking and FeeSharingProxy, are owned by the [Exchequer Multisig](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0007.md) (not to be confused with the [Exchequer Committee](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0041.md)). This ownership role gives the Exchequer Multisig the power to upgrade any of these smart contracts instantly, that is, with no time lock or advance notice. Similarly, the Exchequer Multisig currently also holds all administrator roles on Sovryn smart contracts, giving the Exchequer Multisig the ability to instantly change the modifiable parameters of these contracts.

This mode of operation has worked well enough for the project during its early stages, allowing the core team to respond quickly to issues, but as total value locked has increased, so too has the risk of maintaining this status quo.
 
## Proposed change

To mitigate risks to Exchequer Multisig keyholders and to the Sovryn protocol and its users, we propose transferring ownership and administration of all Sovryn contracts currently owned by the Exchequer Multisig to either the GovernorOwner or GovernorAdmin contract, as specified in the table in the `Description` section above. This will put the contracts under the control of SOV stakers, increasing the decentralization and censorship resistance of these contracts. After the governor roles are transferred to SOV stakers, all proposed smart contract upgrades and parameter changes will have to go through a 24-hour voting period and up to 48-hour timelock, giving Sovryn stakers and users up to 72 hours to react to any changes they might disagree with.

Approval of this SIP will only result in a change in the administrator role in the AMM contracts. No SIP is needed to approve the transfer of governance roles in the rest of the contracts. However to ensure alignment with and readiness from SOV stakers, we are also asking in this proposal for SOV stakers to signal their willingness to accept governance responsibilities in all of the other smart contracts too.

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
