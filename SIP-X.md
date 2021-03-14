# SIP-X: Operating principles for Sovryn

Sovryn is a decentralized finance protocol on RSK governed by SOV tokenholders via Bitocracy. The protocol includes a Treasury that holds the funds originally used to purchase SOV from the protocol as well as fees collected from users of the protocol.

What Sovryn currently lacks is a positive vision for how it should operate and be governed by Bitocracy. This lack of prior vision and operating principles has left a void that is now being filled with ad hoc proposals that are quickly pushing the protocol toward centralization and trust in third parties.

This proposal attempts to provide a positive vision and operating principles fit for a decentralized protocol such as Sovryn.

## Against third-party custody
Recently two SIPs have approved transfers of large amounts of funds out of the Treasury and into the control of third parties:

- [SIP-0008](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0008.md): Transfers $1.375 million worth of BTC to the SIP-0001 BTC multisig.

- [SIP-0012](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0012.md): Transfers 100 BTC to a new BTC multisig.

In both cases, the keyholders to the multisigs custodying these funds are unknown to most tokenholders, and there are no legal or cryptoeconomic protections in place to ensure the safe return of funds. This puts Treasury funds at risk due to:

- Lost keys
- Insider/outsider theft
- Legal attacks

> These comments should not be taken as criticisms of the authors of either SIP-0008 or SIP-0012. I had a chance to review these proposals before they were voted on and believe they were presented in good faith. I am only just now recognizing a "boiling frogs" scenario with regard to risk and now feel that a comprehensive policy is needed to address these risks.

## In crypto we (don't need to) trust

Bitocracy should not expect protection from the legal system. It's not even possible to create a legal contract with a decentralized protocol like Sovryn. As one example of why: who would represent the protocol in court? If someone can represent the protocol in court, is the protocol really decentralized? Plus, if Sovryn can sue, Sovryn can _be sued_. That is a can of worms Bitocracy should not wish to open.

Sovryn is not a corporation with an identifiable board of directors and executives who have a legal fiduciary duty to shareholders. Sovryn is a decentralized protocol existing in a state of cryptoanarchy and should be governed as such. Cryptoeconomics is the only mechanism Bitocracy should expect for protection. For example, if a third party needs to temporarily manage funds from the Treasury, and Bitocracy expects to receive these funds back at a later date, the third party should put up collateral in a smart contract that Bitocracy and/or a credibly-neutral arbitrator controls until the Treasury funds are returned.

Bitocracy should shake its recent habit of trusting third parties with its (R)BTC and demand an immediate return of all Treasury funds currently in possession of third parties back to Bitocracy. Any further transfers of Treasury funds into the "temporary" control of third parties should be cryptoeconomically secured with collateral of equal or greater value, with Bitocracy or a neutral third party having the ability to transfer the collateral to Bitocracy if necessary.

## Managing payments

There is a lot of work that needs to be done for the full vision of Sovryn as laid out in the Blackpaper to be realized. Bitocracy will likely want to delegate to third parties most or all of the day-to-day management of the resources required to do this work. There is already an organization forming around the nucleus of the founding team that is becoming the de facto "executive arm" of the protocol, building the contracts and apps, writing the documentation, promoting the product, running operations, and so on. We need to establish how this organization, and others that may want to do work for Bitocracy, will interface with Sovryn and be held accountable going forward.

A workable model would be a combination of bounties, streaming payments, and lump-sum payments. Bounties would be used to pay for smaller one-off tasks, streaming payments would be used to pay for larger projects on an ongoing basis, and lump-sum payments would be used to pay for big-ticket items that must be paid for in full at the point of sale.

Bounties can be approved by Bitocracy directly or, for convenience, by one or more Bounties multisigs put in a charge of a moderate amount of funds (on the order of <1 BTC) with a mandate to identify small tasks that need to be done and pay contributors who complete these tasks. Since these tasks are small, there's not a lot of risk in doing the work first and expecting to receive the bounty later. As bounty hunters and volunteers successfully complete tasks, they gain the trust of the community and may be able to graduate to receive a streaming payment contract.

To set up a streaming payment, the recipient would first propose what project(s) they are going to work on and the amount of funds they will need to complete their project(s). If approved, the funds would be transferred to a streaming payment smart contract that releases the payment to the recipient on a per-block basis (that is, the recipient can withdraw all funds released by the contract up to the current point in time, as frequently as once per block if they want). At any point, Bitocracy can turn off the streaming contract and prevent any more funds from being released to the recipient, and the recipient would stop work until the contract is turned back on or renegotiated. This protects Bitocracy from having to trust a third party with a large upfront payment of funds, and it protects recipients from having to do a large amount of work and then trust that they will get paid at a later date.

In case a large lump-sum payment is absolutely necessary, this may be acceptable to Bitocracy provided there is sufficient justification in the proposal. For example, a big-ticket item may require full payment at the time of purchase rather than streaming payments over a period of time. In this case, bounties and streaming payments would not be the appropriate tool to use, and a lump-sum payment should be proposed to Bitocracy instead. The funds must go directly from the Treasury to the final recipient, without being managed by a third party in the middle of the transaction.

## A path to Sovrynty

Currently there exist two major points of centralization in the Sovryn protocol:
1. Contract upgradeability  
2. The Guardian veto

### Contract upgradeability
Many contracts in the Sovryn protocol have the ability to be "upgraded", that is, completely changed in place from one contract to another. While the protocol is in its infancy, it is understandable to maintain the ability to upgrade contracts to fix errors. This feature has already proven its usefulness to Sovryn and its users more than once. However, even with a time delay on upgrades, this remains a point of vulnerability from the perspective of protocol users and SOV holders.

The current contract owner, with the sole power to initiate upgrades, is [the Exchequer Multisig](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0007.md). I propose that at the end of the four-week bonus period of the SIP-0008 bug bounty program, the Exchequer Multisig transfer ownership of all Sovryn protocol smart contracts over to Bitocracy. Furthermore, I propose that if no critical bugs are found within six months of Bitocracy taking control, that the ownership function be burned so that the Sovryn contracts are no longer upgradeable. A critical bug being found within these six months will reset the clock until ownership is finally burned.

### The Guardian veto
In Bitocracy, all proposals have the possibility of being vetoed by the Guardian, a special role currently designated to the Exchequer Multisig. As with contract upgradeability, it is understandable that while Bitocracy is being established, that the system be protected from its own immaturity by a trusted set of participants. However, as time goes on and increasingly consequential decisions are put forth to Bitocracy, this role will take on more and more power and expose Bitocracy to the risk of censorship. I propose that an expiration date of 2022-01-21 be put on the Guardian role, on the one year anniversary of Bitocracy, to limit the potential for long-term censorship of the protocol.

## Conclusion

Currently, Bitocracy is placing trust in third parties to manage a significant amount of the Treasury. Given this precedent, such demands for trust are likely to continue. Bitocracy should rein this back in and formally adopt principles of trust-minimization, particularly with regard to funds and other resources Bitocracy expects to be returned at a later date. Using collateralized contracts, Bitocracy can minimize the counterparty risk involved with such transactions. For transfers where funds are not expected to be returned at a later date, several payment options exist, including bounties, streaming payments, and lump-sum payments. Furthermore, point of centralization in the protocol that were prudent early on should be phased out on a reasonable timeline to ensure its long-term Sovrynty.

With these operating principles in place Bitocracy will be in a better position to balance the need for security of the Treasury with the rapid execution required for Sovryn's success.

## Resolved

- All BTC from the Sovryn Treasury currently in the possession of the SIP-0001 and SIP-0012 bitcoin multisigs and any other addresses or systems outside the control of Bitocracy are to be transferred across the RSK Powpeg and into the Sovryn Treasury under the control of Bitocracy as soon as possible and no later than March 31, 2021 (UTC).
- All future transfers of Treasury funds or other resources to third parties, that Bitocracy expects to receive back at a later date, will be cryptoeconomically secured with collateral of equal or greater value under the control of Bitocracy and/or a credibly-neutral arbitrator until the Treasury funds/resources are returned to Bitocracy in full.
- Bitocracy will adopt a streaming payment smart contract standard and use it to pay for ongoing operational costs going forward. For purchases where full payment is due at the point of sale, a lump-sum payment can be proposed to Bitocracy and the payment should go directly from the Treasury to the seller.
- Bitocracy will consider setting up one or more Bounties multisigs governed by active members of the community to pay for small, one-off bounties.
- Contract upgradeability powers will be transferred from the Exchequer Multisig to Bitocracy at the end of the four-week bonus period of the SIP-0008 bug bounty program. Contract upgradeability will then be permanently disabled after six months of no critical bugs being found, with a critical bug being found during these six months resetting the clock until no critical bugs are found for a six-month period and contract upgradeability is permanently disabled.
- The Guardian role will have an expiration date of 2022-01-21 at which point the Guardian role will be permanently removed from Bitocracy.
