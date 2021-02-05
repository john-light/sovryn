---
SGP: 1
Title: The Sovryn Governance Proposal Process
Author: John Light (@john-light)
Status: Draft
Track: Meta
Created: 2021-02-05
---

# SGP-1: The Sovryn Governance Proposal Process

**Version 0.1**

## What is a Sovryn Governance Proposal?
A Sovryn Governance Proposal, or "SGP", is a document that details a change to the management, allocation, or use of shared resources owned or directly influenced by Sovryn. All SGPs must be consistent with the goals and values put forth in [SGP-0](SGP-0.md) (the Sovryn Constitution) and compliant with the requirements outlined in this document, SGP-1. The SGP author is responsible for building consensus within the community for their SGP and documenting dissenting opinions.

## Purpose
The purpose of the Sovryn Governance Proposal Process ("the Sovryn governance process") is to provide a structured process for making changes to the shared resources of Sovryn. For these shared resources, governance processes are needed to grant or deny access and approve or reject proposed changes. By creating a fair, lightweight, and transparent governance process, the SGP-1 authors hope to give SOV holders a meaningful say in the governance of Sovryn and increase the chances of Sovryn's success.

## Proposal workflow
Parties directly involved in the process are the _SGP author(s)_ (you), _Sovryn Voters_, _Sovryn Guardians_, and _SGP Editors_. Each of these roles is explained later in this document.

Proposals follow this workflow:

* Stage I: Select SGP Track  
* Stage II: Pre-proposal  
* Stage III: Draft Proposal  
* Stage IV: Review Periods  
* Stage V: Sovryn DAO Vote  

During Stage III SGP Editors will review proposals for formatting, legibility, and compliance with SGP-1, referring to SGP-1 as the basis for accepting, denying, or requesting modifications to a proposal.

At a high level, the SGP-1 workflow looks like this:

TODO: Upload and link workflow image here

### Stage I: Select SGP Track
Before you spend time working on a proposal, make sure the proposal complies with SGP-1 and has a chance of passing review by the SGP Editors and your peers. Review the SGP tracks and their requirements then select the track that you think is best for your proposal. If your proposal meets the requirements, it has a much greater chance of being accepted by SGP Editors and approved by Sovryn Voters.

There are four tracks that an SGP can be categorized into. Select the one you think is best for your AGP:

* Finance: proposals for transferring funds from the Sovryn Treasury  
* Meta: proposals for changing SGP-0 or SGP-1 (“changing the way things are changed”)  
* Proclamations: proposals for making a public statement on behalf of Sovryn  

Proposals that cannot be categorized into one of these tracks will likely be denied by SGP Editors. At the discretion of SGP Editors, a proposal may be categorized as “Other” until a new, appropriate track is approved as part of a Meta SGP.

In addition to the requirement that all SGPs must be consistent with SGP-0, each track has its own requirements for SGPs as follows:

**Finance**  
Proposals made to the Finance track must affect the movement of assets held by the Sovryn Treasury.

* All code and content funded through the Sovryn governance process must be released under one of the following licenses:  
  * Creative Commons Zero (CC-0)  
  * MIT  

**Meta**  
Proposals made to the Meta track must affect changes to SGP-0 or SGP-1. SGP Editors have the authority to fix errata in AGP-0 or AGP-1 on an as-needed basis without going through the Sovryn governance process. All other proposals to modify SGP-0 or SGP-1 should be made to the Meta track.

**Proclamations**  
Proposals made to the Proclamations track are used to make a statement on behalf of Sovryn and can say whatever the author(s) want, so long as the proclamation is consistent with the Sovryn Constitution.  

### Stage II: Pre-proposal
During Stage II you should seek feedback on your SGP idea by sharing it with your peers in the Sovryn community and soliciting their feedback. Examples of appropriate venues to share your SGP idea include:

* The [#bitocracy channel](https://discord.gg/WApXyz4D5h) in the Sovryn Discord  
* The [SGP category](https://forum.sovryn.app/c/bitocracy/sip-sovryn-improvement-proposals/) in the Sovryn forum  
* The Issues section of the Bitocracy repo  

Be open-minded and respectful of all feedback you receive. Adjust your proposal to address legitimate concerns as they come up to increase the odds of your proposal passing review in later stages.

### Stage III: Draft
After you have asked the Sovryn community whether an idea has any chance of support, and you have received sufficient feedback to feel confident going forward, you can create a draft SGP as a draft pull request to the Bitocracy repo. Use a template from the Templates section below to ensure you are including all the necessary information. The draft SGP file should be given a temporary title e.g. "SGP: This is an example title", which the SGP Editor will later assign an SGP number.

**Templates**  
Below is a list of SGP templates for each track. Copy the template for the track your SGP is in, fill it out, and submit the pull request with your SGP for review. Sections marked as “required” in the template must be completed. Note that all proposals must be licensed CC-0.

* [Finance](../templates/finance_template.md)  
* [Association](../templates/guardians_template.md)  
* [Meta](../templates/meta_template.md)  
* [Proclamations](../templates/proclamation_template.md)  

To make a Meta track change, you must:

1. Create and submit a pull request changing either SGP-0 or SGP-1. Add your name and GitHub username, and the name and username of any of your co-authors, to the "Author" section in the SGP header.  
2. In a _separate_ draft pull request, create a new file in the SGPs directory of the SGPs repo.  
3. Add a link to the pull request created in (1) to the new file created in (2).  
4. Submit the new file from (2) as a pull request to the Bitocracy repo. This will be the SGP pull request. If the SGP is approved by SOV holders, the pull request created in (1) will be merged. If the proposal is rejected/withdrawn, the pull request created in (1) will be closed.

### Stage IV: Review Periods
After an SGP has been submitted as a draft pull request to the Bitocracy repo, it must undergo three review periods:

1. A Community Review, which starts the moment that a proposal has been submitted to the SGP repo and lasts for one calendar week.  
2. An Editor Review, which starts when the Community Review ends and lasts for an indefinite period of time.  
3. A Final Review, which starts when the Editor Review ends and lasts for one calendar week.  

**Community Review**  
During the Community Review period, the SGP author will have a chance to respond to feedback and make changes to their proposal based on the feedback they have received to increase the likelihood of the proposal passing.  

**Editor Review**  
At the end of the Community Review period, SGP Editors will perform their review of the proposal. The SGP author should incorporate any changes suggested by the SGP Editor to prepare the proposal for the Final Review. After a proposal is reviewed by SGP Editors, an SGP Editor will ask the author if the proposal is ready for the Final Review. If the SGP Editors do not receive a response from the SGP author then the SGP Editors may at their discretion either close the pull request or move the proposal on for a Final Review.

* If agreeable, an SGP Editor will assign the SGP a number (generally the number of the SGP pull request), change the status of the SGP pull request from "draft" to "ready", and move the SGP on for a Final Review.  
* Reasons for denying an SGP number and closing the pull request include the SGP being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing legitimate concerns by reviewers, or not in compliance with SGP-1.  

**Final Review**

During the Final Review, the proposal cannot be changed. This gives Sovryn Voters a chance to review the proposal in its final state before the SGP is voted on.

### Stage V: Sovryn Vote
After an SGP has gone through its Final Review, an SGP Editor will add a "Ready to vote" tag to the pull request. At the soonest available opportunity, Sovryn Guardians will review proposals that have the "Ready to vote" tag and decide whether to put the proposal to a final vote by Sovryn Voters or veto the proposal.

Regardless of the vote outcome, after an SGP has been put to a vote a link to the vote will be added to the SGP and the "Ready to vote" label will be removed. If an SGP is rejected by Sovryn Voters, then the pull request will be closed. If an SGP is approved by Sovryn Voters, then the pull request will be merged. Any pull request referenced in a Meta track proposal that is approved by SOV Voters will be merged by an SGP Editor.  

## Sovryn Voters
Sovryn Voters are holders of the SOV token who have registered their SOV in the Sovryn Governance contract. Registered Sovryn Voters are granted the ability to vote on SGPs that are submitted to Sovrn by Sovryn Guardians.

## Sovryn Guardians
Sovryn Guardians are elected by Sovryn Voters to participate in a 3-of-5 multisig. This multisig has the exclusive authority to submit onchain proposals to the Sovryn Governance contract. The multisig also decides which repo is the canonical repo for SGPs.

## SGP Editors
Each Sovryn Guardian is by default also an SGP Editor. Sovryn Guardians can choose to delegate their SGP Editor role to another Sovryn community member and, by a 3-of-5 vote, remove existing SGP Editors or add additional SGP Editors as needed.

SGP Editors have two responsibilities:

* Review SGPs during the Editor Review and prepare them for the Final Review  
* Update the SGP status and merge or close its pull request depending on the Sovryn Vote outcome  

**Review proposals**  
SGP Editors review proposals and accept, reject, or request modifications to them based on formatting, legibility, and compliance with SGP-1.

**Update the SGP status**  
From the Final Review until the end of the Sovryn Vote, SGP Editors will update the SGP pull request and any associated pull requests as specified in the Sovryn governance process.  

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).  
