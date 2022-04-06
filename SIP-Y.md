---
SIP: 'N/A'
Title: Changing of the Guardians
Author: John Light (@john-light)
Status: Draft
Track: Contract
Created: 2022-04-06
---

# SIP-Y: Changing of the Guardians

## Description  

If approved, this proposal will signal approval for a changing of the Guardians:
- The role of Bitocracy Guardian, which has the power to veto any proposal that goes through Bitocracy, will be held by a 3-of-9 multisig.
- The role of Contracts Guardian, which has the power to pause or freeze certain functions or entire smart contracts, will be held by a 3-of-12 multisig.

The proposed membership of these multisigs is as follows:

|	Guardian          	         | Keyholder	                 | RSK address  |
| ---------------------------- |:---------------------------:|:------------:|
| Bitocracy Guardian (3-of-9)  |                             |              |
|                              | .                           | `0x...`      |
| Contracts Guardian (3-of-12) |                             |	            |
|                              | .                           | `0x...`      |

To ensure the effectiveness of these Guardian roles, processes will be put in place by the Guardian members and Sovryn core team to ensure close coordination and rapid incident response actions and communications.

## Motivation

Currently the Bitocracy and Contracts Guardian roles are both filled by the Exchequer Multisig, using the original Gnosis Multisig contracts. We propose assigning these roles to two different multisigs, both created using the newer Gnosis Safe Multisig contracts, with different signer sets to account for the different responsibilities and skills required of each multisig.

## Proposed change

- The Bitocracy Guardian role will be transferred from the Exchequer Multisig to the Bitocracy Guardian Multisig.
- The Contracts Guardian role will be transferred from the Exchequer Multisig to the Contracts Guardian Multisig.

### Bitocracy Guardian
The Bitocracy Guardian will have the role of vetoing any potentially "dangerous" proposals that are submitted. For the purposes of this SIP, a "harmful" proposal is one that the Guardian signers determine would have a high likelihood of leading to either a) an unfair loss of funds owned by Sovryn users or stakers, or b) a loss of Treasury funds due to an exploited vulnerability in the staking contract. For illustration purposes, below are some examples of proposals that either would or would not be likely to be considered "harmful".

Examples of "harmful" proposals:
- A proposal that transfers ownership of Sovryn smart contracts to an address that the Guardian signers do not trust.
- A proposal that upgrades a Sovryn contract to contain a backdoor that would allow an attacker to drain user funds.
- A proposal that changes the interest rate curve of the lending pool in such a way that interest rates would immediately increase by >100%.
- A proposal that has been passed because someone exploited a vulnerability in the staking contract that gave them an overwhelmingly large amount of voting power.
- A proposal that makes the voting period and/or time lock period shorter than 24 hours.
- A proposal that adds an illiquid asset as collateral for borrowing.

Examples of proposals that would be controversial but nonetheless not be considered "harmful" for the purposes of this SIP:
- A proposal that sends Treasury funds to a project that no one has ever heard of with founders no one recognizes.
- A proposal that upgrades Sovryn contracts to only allow users with a KYC token to use the protocol.
- A proposal proclaiming that Sovryn should migrate all its smart contracts and liquidity to an altcoin blockchain. 

### Contracts Guardian
The Contracts Guardian will have the role of either pausing or freezing any Sovryn contract or contract function that can be paused or frozen and is found to have a vulnerability that could be exploited and cause harm to Sovryn users. SOV stakers will have the ability to replace the Contracts Guardian if desired or needed.

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
