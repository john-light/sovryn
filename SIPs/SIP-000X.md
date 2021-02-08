---
SIP: X
Title: The Sovryn Improvement Proposal Process
Author: John Light (@john-light)
Status: Draft
Track: Meta
Created: 2021-02-05
---

# SIP-X: The Sovryn Governance Proposal Process

**Version 0.1**

## What is a Sovryn Improvement Proposal?
A Sovryn Improvement Proposal, or "SIP", is a document that details a change to the management, allocation, or use of shared resources owned or directly influenced by Sovryn. All SIPs must be consistent with the goals and values put forth in [SIP-0](SIP-0.md) (the Sovryn Constitution) and compliant with the requirements outlined in this document, SIP-X. The SIP author is responsible for building consensus within the community for their SIP and documenting dissenting opinions.

## Purpose
The purpose of the Sovryn Improvement Proposal Process ("the Sovryn proposal process") is to provide a structured process for making changes to the shared resources of Sovryn. For these shared resources, a governance process is needed to grant or deny access and approve or reject proposed changes. By creating a fair, lightweight, and transparent governance process, the SIP-X authors hope to give SOV holders a meaningful say in the governance of Sovryn and increase the chances of Sovryn's success.

## Proposal workflow
Parties directly involved in the process are the _SIP author(s)_ (you), _Sovryn Voters_, _Sovryn Guardians_, and _SIP Editors_. Each of these roles is explained later in this document.

Proposals follow this workflow:

* Stage I: Select SIP Track  
* Stage II: Pre-proposal  
* Stage III: Draft Proposal  
* Stage IV: Review Periods  
* Stage V: Sovryn DAO Vote  

During Stage III SIP Editors will review proposals for formatting, legibility, and compliance with SIP-X, referring to SIP-X as the basis for accepting, denying, or requesting modifications to a proposal.

At a high level, the SIP-X workflow looks like this:

TODO: Upload and link workflow image here

### Stage I: Select SIP Track
Before you spend time working on a proposal, make sure the proposal complies with SIP-X and has a chance of passing review by the SIP Editors and your peers. Review the SIP tracks and their requirements then select the track that you think is best for your proposal. If your proposal meets the requirements, it has a much greater chance of being accepted by SIP Editors and approved by Sovryn Voters.

There are four tracks that an SIP can be categorized into. Select the one you think is best for your SIP:

* Contract: proposals for modifying one or more Sovryn smart contracts  
* Finance: proposals for transferring funds from the Sovryn Treasury  
* Meta: proposals for changing SIP-0 or SIP-X (“changing the way things are changed”)  
* Proclamations: proposals for making a public statement on behalf of Sovryn  

Proposals that cannot be categorized into one of these tracks will likely be denied by SIP Editors. At the discretion of SIP Editors, a proposal may be categorized as “Other” until a new, appropriate track is approved as part of a Meta SIP.

In addition to the requirement that all SIPs must be consistent with SIP-0, each track has its own requirements for SIPs as follows:

**Contract**  
Proposals made to the Contract track must change one or more of the Sovryn smart contracts. The proposal should link to the existing contract(s) to be modified and to the source code of the proposed contract modification(s). All Contract track proposals must include a link to a third party audit report of the specified modification(s).

* All code modifications proposed made must be published under an MIT license.

**Finance**  
Proposals made to the Finance track must affect the movement of assets held by the Sovryn Treasury.

* All code and content funded through the Sovryn governance process must be released under one of the following licenses:  
  * Creative Commons Zero (CC-0)  
  * MIT  

**Meta**  
Proposals made to the Meta track must affect changes to SIP-0 or SIP-X. SIP Editors have the authority to fix errata in SIP-0 or SIP-X on an as-needed basis without going through the Sovryn governance process. All other proposals to modify SIP-0 or SIP-X should be made to the Meta track.

**Proclamations**  
Proposals made to the Proclamations track are used to make a statement on behalf of Sovryn and can say whatever the author(s) want, so long as the proclamation is consistent with the Sovryn Constitution.  

### Stage II: Pre-proposal
During Stage II you should seek feedback on your SIP idea by sharing it with your peers in the Sovryn community and soliciting their feedback. Examples of appropriate venues to share your SIP idea include:

* The [#bitocracy channel](https://discord.gg/WApXyz4D5h) in the Sovryn Discord  
* The [SIP category](https://forum.sovryn.app/c/bitocracy/sip-sovryn-improvement-proposals/) in the Sovryn forum  
* The Issues section of the Bitocracy repo  

Be open-minded and respectful of all feedback you receive. Adjust your proposal to address legitimate concerns as they come up to increase the odds of your proposal passing review in later stages.

### Stage III: Draft
After you have asked the Sovryn community whether an idea has any chance of support, and you have received sufficient feedback to feel confident going forward, you can create a draft SIP as a draft pull request to the Bitocracy repo. Use a template from the Templates section below to ensure you are including all the necessary information. The draft SIP file should be located in the `SIPs` directory and given a temporary name e.g. `SIP.md`, which the SIP Editor will later assign an SIP number.

**Templates**  
Below is a list of SIP templates for each track. Copy the template for the track your SIP is in, fill it out, and submit the pull request with your SIP for review. Sections marked as “required” in the template must be completed. Note that all proposals must be licensed CC-0.

* [Contract](../templates/contract_template.md)  
* [Finance](../templates/finance_template.md)  
* [Meta](../templates/meta_template.md)  
* [Proclamations](../templates/proclamation_template.md)  

To make a Meta track change, you must:

1. Create and submit a pull request changing either SIP-0 or SIP-X. Add your name and GitHub username, and the name and username of any of your co-authors, to the "Author" section in the SIP header.  
2. In a _separate_ draft pull request, create a new file in the SIPs directory of the Bitocracy repo.  
3. Add a link to the pull request created in (1) to the new file created in (2).  
4. Submit the new file from (2) as a pull request to the Bitocracy repo. This will be the SIP pull request. If the SIP is approved by SOV holders, the pull request created in (1) will be merged. If the proposal is rejected/withdrawn, the pull request created in (1) will be closed.

### Stage IV: Review Periods
After an SIP has been submitted as a draft pull request to the Bitocracy repo, it must undergo three review periods:

1. A Community Review, which starts the moment that a proposal has been submitted to the Bitocracy repo and lasts for one calendar week.  
2. An Editor Review, which starts when the Community Review ends and lasts for an indefinite period of time.  
3. A Final Review, which starts when the Editor Review ends and lasts for one calendar week.  

**Community Review**  
During the Community Review period, the SIP author will have a chance to respond to feedback and make changes to their proposal based on the feedback they have received to increase the likelihood of the proposal passing.  

**Editor Review**  
At the end of the Community Review period, SIP Editors will perform their review of the proposal. The SIP author should incorporate any changes suggested by the SIP Editor to prepare the proposal for the Final Review. After a proposal is reviewed by SIP Editors, an SIP Editor will ask the author if the proposal is ready for the Final Review. If the SIP Editors do not receive a response from the SIP author then the SIP Editors may at their discretion either close the pull request or move the proposal on for a Final Review.

* If agreeable, an SIP Editor will assign the SIP a number (generally the number of the SIP pull request), change the status of the SIP pull request from "draft" to "ready", and move the SIP on for a Final Review.  
* Reasons for denying an SIP number and closing the pull request include the SIP being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing legitimate concerns by reviewers, or not in compliance with SIP-X.  

**Final Review**

During the Final Review, the proposal cannot be changed. This gives Sovryn Voters a chance to review the proposal in its final state before the SIP is voted on.

### Stage V: Sovryn Vote
After an SIP has gone through its Final Review, an SIP Editor will add a "Ready to vote" tag to the pull request. At the soonest available opportunity, Sovryn Guardians will review proposals that have the "Ready to vote" tag and decide whether to put the proposal to a final vote by Sovryn Voters or veto the proposal.

Regardless of the vote outcome, after an SIP has been put to a vote a link to the vote will be added to the SIP and the "Ready to vote" label will be removed. If an SIP is rejected by Sovryn Voters, then the pull request will be closed. If an SIP is approved by Sovryn Voters, then the pull request will be merged. Any pull request referenced in a Meta track proposal that is approved by Sovryn Voters will be merged by an SIP Editor.  

## Sovryn Voters
Sovryn Voters are holders of the SOV token who have staked their SOV in the Sovryn Governance contract. The voting power of Sovryn Voters is determined by the number of SOV they have staked and the length of time their SOV is staked for.

## Sovryn Guardians
Sovryn Guardians are elected by Sovryn Voters to participate in a 3-of-5 multisig. This multisig has the exclusive authority to submit onchain proposals to the Sovryn Governance contract. The multisig also decides which repo is the canonical repo for SIPs.

When Sovryn Guardians submit a proposal for a vote, they will refer to the proposal with a link to the commit referred to as the canonical proposal as well as a SHA-256 hash of the raw proposal file at that commit. For Contract track proposals, only the contract source code specified in the proposal will be submitted for a vote.

## SIP Editors
Each Sovryn Guardian is by default also an SIP Editor. Sovryn Guardians can choose to delegate their SIP Editor role to another Sovryn community member and, by a 3-of-5 vote, remove existing SIP Editors or add additional SIP Editors as needed.

SIP Editors have two responsibilities:

* Review SIPs during the Editor Review and prepare them for the Final Review  
* Update the SIP status and merge or close its pull request depending on the Sovryn Vote outcome  

**Review proposals**  
SIP Editors review proposals and accept, reject, or request modifications to them based on formatting, legibility, and compliance with SIP-X.

**Update the SIP status**  
From the Final Review until the end of the Sovryn Vote, SIP Editors will update the SIP pull request and any associated pull requests as specified in the Sovryn governance process.  

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
