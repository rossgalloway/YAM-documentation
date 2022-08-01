# Governance

## Overview

YAM launched with fully decentralized governance from Day 1, built on the Compound Labs governance module. YAM tokenholders have control over updates to all the DAO smart contracts including the token implementation, governor, timelock, and treasury. All modifications and interactions must pass through on-chain governance votes to be executed. YAM governance consists of 2 broad steps:

- Consensus: This is how the DAO decides what to do. It is an "off-chain" process. This step uses YAM Improvement Proposals (YIPs) and Grant Administration Proposals (GAPs).
- Execution: This is how the DAO implements what it has decided upon. It is an "on-chain" process. This step uses YAM Execution Proposals (YXPs).

The [Gov-Ops Council]() provides assistance with the governance process, including facilitation for determining consensus and execution for routine and minimal proposals.

You can read more about why the process is structured this way [here]()

## Consensus Process (off-chain)

:::note

The YAM governance process has recently had an overhaul. The core governance contracts remain unchanged, but the implementation and execution of the process has changed.

:::

There are 2 types of governance interactions: DAO upgrades (YIPs) and Grant Administration (GAPs). Both these types follow the consensus and execution steps, but have different requirements and are used for different types of proposals. YIPs are used to make changes to the DAO and GAPs are used to allocate funding for different projects.

### DAO Upgrades (YIP Process)

DAO upgrades include changes to the existing rules or operation of the DAO. These upgrades may be proposed as the result of work from a grant, or simply as an idea to improve something. 
1. DAO upgrades follow to YIP governance process, which begins on the [Yam Governance Forum]() and [Yam Discord]() where ideas are initially discussed by token holders. 
2. Once the idea has been discussed, the proposer writes and posts their proposal to the [proposals section of the forum](). The community signals its interest and may suggest modifications to the proposal.
3. After recieving feedback a vote on the proposal can be created on [Snapshot]() (off-chain voting), where tokenholders vote on it.

:::caution

Proposing a snapshot vote without sufficient discussion runs the risk of the Gov-Ops council refusing to add it to a YXP, or the guardian multi-sig signers vetoing the on-chain execution.

:::

If a YIP requires additional work to be implemented and executed, and that work is outside the scope of the [Gov-Ops Council]() then that work needs to be done by the proposing party. Funding to do this work can be provided via the grant process. **Just because a YIP passes a snapshot vote does not mean that someone will implement it.** If additional work is expected, Gov-Ops Council members may recommend that a YIP proposer request grant funding prior to submitting their YIP.

An example of a YIP that doesn't require additional code work is a rebalance of the YAM treasury from one approved asset to another approved asset. If the parameters of the rebalance are specified in the YIP then this work falls within the scope of the Gov-Ops council to execute in a YXP.

#### YIP Timeline

- Forum and Discord Discussion: 3+ days
- Snapshot Off-Chain Vote: 3+ days, avoid holidays and weekends.
- Upon passing, on-chain execution will occur in the next scheduled YXP (typically occuring monthly) assuming all information and requirements are met.

### Grant Administration (GAP Process)

Grant Administration is the process by which the DAO determines what it is going to fund. Grants are the vehicles the DAO uses to pay for work done on its behalf. This process includes the initial application grant, the vetting of the proposed work to be done, and the review of deliverables once completed. 

1. Grant applicants start by submitting a new Silo Creation Application (if an applicable silo doesn't exist) or a Silo Extension Application (if one does). Token holders can then give feedback on the idea included in the application, allowing the applicant to cater their proposal to the DAO's needs and preferences. 
2. The next step is the creation of a specifications document for the project, which defines the scope, deliverables, requirements, and specifications for the project that will be funded by the grant. The specification document is submitted both on the YAM Governance Forum and on Github so it can be added to the YAM Governance Repository. It will be reviewed by the Gov-Ops council for completeness and by token holders for quality.
3. Once the specifications document is complete, the applicant then submits a grant proposal, also on the forum and Github. This document should reference the specification document and propose a request for funds to do the work, as well as a timeline to do so.
4. After posting the grant application, the applicant should create a snapshot vote for token holders to determine whether they want to fund the grant or not.

#### GAP Timeline

- Silo Application, Specification Document, Grant application discussion: 3+ days after final docs are posted
- Snapshot Off-Chain Vote: 7+ days
- Upon passing, work on the project should begin.
- Upon completion of milestones specified in the grant proposal, payment requests should be posted to the governance forum and github.
- Payment will occur in the next scheduled YXP (typically occuring monthly) assuming all information and requirements are met and the payment is not disputed.

### Proposing and reaching Quorum for Consensus Votes (Snapshot)

A proposer must have > 100 BoU YAM (251 scaled) delegated to their address.

In order to pass, a proposal must reach quorum which means that a certain threshold of total voting power votes "for" the proposal. For snapshot votes, this number is 200,000 BoU YAM ([what does BoU mean?]()) or 500,000 scaled YAM, equivalent to 4% of the initial token supply.

## Execution Process (on-chain)

The execution process...

For on-chain voting, a user must have 50,000 BoU YAMs delegated to their address This is equivalent to 1% of the initial token supply.

## Other important information

### Delegation

In order to vote, you must [delegate your vote]() to yourself or to someone else. This applies to off-chain snapshot voting as well. Any YAM tokens being used as an LP in Yam's incentivizer farming Yams are automatically delegated to self. You can currently delegate to yourself via [yam.finance](), and we are working on an interface to delegate to other addresses. You can also delegate via [etherscan]() directly.

### Voting with LP tokens

Only if you provide liquidity to [Sushiswap]() Yam/ETH pool and stake on Yam's incentivizer using [yam.finance/farm](). Don't forget to register to vote on [yam.finance/governance](), only needs to be done once. Voting power is determined by distributing the voting power of YAM held in the YAM/ETH Sushiswap pool, but distributed to only YAM Incentivizer stakers. This was done to mitigate flashloan threats in voting, so the Incentivizer contract keeps a record of the necessary values at needed block heights to facilitate those mitigations.
