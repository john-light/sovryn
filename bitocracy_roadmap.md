# Sovryn Bitocracy Roadmap

## Bitocracy smart contracts

### Q2 2021
- Set [Guardian role](https://github.com/DistributedCollective/SIPS/blob/2c70b5834f874ca27a00c8373c00de1c610d0b89/SIPs/SIP-0011.md#sovryn-guardians) to burn on approximately 2022-01-21.

- Transfer contract ownership from Exchequer to Bitocracy
  - Permanently disable contract upgradeability after six months if no critical bugs are found. If a critical bug is found during these six months the clock is reset until no critical bugs are found for a six-month period.

- Implement Voting Rewards. Everyone who participates in a vote will be eligible to withdraw their share of voting rewards that have accumulated in the voting rewards pool since the last vote. The proportion of protocol revenue going toward voting rewards (rather than the treasury) is modifiable by the Governance admin.

### Q3 2021

- Implement Quiet Ending Voting. If the outcome of a vote is flipped within the last _x_ hours of a vote, the duration of the vote is extended for _y_ hours, and if the vote outcome is flipped at any time during the quiet ending period, then vote is extended _y_ more hours.

- Implement Bitocracy Ambassador. The Bitocracy Ambassador is a feature that enables Governance to interact with any RSK smart contract.

- Bitocracy expense model
  - Bounties for engagements valued at <$50,000
  - Superfluid contracts for ongoing engagements valued at >$50,000
  - Lump sum payments at the point of sale for everything else

### Q4 2021

- All treasury BTC not in the Governance contract is returned to the Governance contract under the direct control of SOV holders.

### Q1 2021

- Guardian role is burned. Sovryn is sovereign!

## Bitocracy interface

### Q2 2021

- Global Bitocracy dashboard:
  - Voting 
     - Current total voting power
     - Voting power calculator
     - Voting power leaderboard
     - Delegate leaderboard
  - Finances
    - Treasury balance (vested + unvested SOV, RTC, other ERC-20s)
    - Monthly and cumulative protocol revenues
    - Monthly and cumulative protocol rewards paid

- Bitocracy email notifications
  - Start vote
  - Reminder
  - Vote outcome

### Q3 2021

- Proposal GUI. Create new Bitocracy proposals.
  - Contract: Call another RSK contract.
  - Proclamation: Make a proclamation on behalf of Bitocracy.
  - Finance: Withdraw from the treasury to a specified address
  - Issuance: Mint new SOV to a specified address

- Global Bitocracy dashboard:
  - Show balances in non-treasury smart contracts e.g. Sovryn, Superfluid, etc.

### Q4 2021

- Frame integration
  - Add RSK network
  - Add Bitocracy Ambassador feature
