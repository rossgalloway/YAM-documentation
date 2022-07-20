# Governance

## Overview

YAM launched with fully decentralized governance from Day 1 by implementing the Compound governance module. This gives control of the protocol to YAM tokenholders, meaning that updates to the protocol and management of the treasury can only be performed with approval from YAM holders.

## Process

The governance process begins on [Yam Discord]() where ideas are initially discussed. Once discussion has formalized a potential proposal it is submitted to [Yam Governance Forum](). If the community signals its interest and any necessary modifications to the proposal are made, the proposal is submitted to [Snapshot off-chain governance](), where tokenholders can vote with their token balances.

If a Snapshot proposal is passed and no code is required to be implemented, the approved action can be taken.

If code deployment is required, the code will go to audit if necessary, and then be proposed via on-chain governance at which point tokenholders will vote on-chain to deploy.

### Timeline

- [Discord Ideation](): 1-3 days
- [Forum Discussion](): 3+ days
- [Snapshot Off-Chain Voting](): 3 days
- [On-chain Voting](): 2 days
- [Execution Timelock](): 12 hours

## Delegation
In order to vote, you must [delegate your vote]() to yourself or to someone else. This applies to off-chain snapshot voting as well. Any YAM tokens being used as an LP in Yam's incentivizer farming Yams are automatically delegated to self. You can currently delegate to yourself via [yam.finance](), and we are working on an interface to delegate to other addresses. You can also delegate via [etherscan]() directly.

## Quorum
For a proposal to pass and be executed on-chain, it must reach "minimum acceptance quorum," which means having 200,000 BoU YAM voting "For" the proposal, equivalent to 4% of the initial token supply. Quorum requirements for Yam are based on balanceOfUnderlying, which are YAMs without the rebasing scalingFactor applied. Since the rebase function has been disabled as of Dec 29 the scaling factor is currently fixed to 2.50. Your voting power is your balance of Yam tokens / 2.50.

## To submit a proposal:

In snapshot a user must have 100 BoU YAMs delegated to their address.

For on-chain voting, a user must have 50,000 BoU YAMs delegated to their address This is equivalent to 1% of the initial token supply.
Basing quorum around a minimum amount of "For" votes eliminates a scenario in which voting "Against" could actually lead a proposal to pass when abstaining would cause it to fail (for example if there were 198k "For" votes and zero "Against", a 2k "Against would allow the proposal to pass if quorum was based on total votes rather than total "For" votes).

## LP Governance Participation

Only if you provide liquidity to [Sushiswap]() Yam/ETH pool and stake on Yam's incentivizer using [yam.finance/farm](). Don't forget to register to vote on [yam.finance/governance](), only needs to be done once. Voting power is determined by distributing the voting power of YAM held in the YAM/ETH Sushiswap pool, but distributed to only YAM Incentivizer stakers. This was done to mitigate flashloan threats in voting, so the Incentivizer contract keeps a record of the necessary values at needed block heights to facilitate those mitigations.
