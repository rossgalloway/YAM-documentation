---
sidebar_position: 3
sidebar_label: "Governance Overview"
---

# Governance

![Yam Voters deliberating](/img/Ross___painting_of_the_founding_fathers_signing_the_declaration_e259e7aa-f2d3-41f8-9826-ba0fcf607a5b.png)

## Overview

YAM launched with fully decentralized governance from Day 1, built on the Compound Labs governance module. YAM tokenholders have control over updates to all the DAO smart contracts including the token implementation, governor, timelock, and treasury. All modifications and interactions must pass through on-chain governance votes to be executed. YAM governance consists of 2 broad steps:

- Consensus: This is how the DAO decides what to do. It is an "off-chain" process. This step uses YAM Improvement Proposals (YIPs) and Grant Administration Proposals (GAPs).
- Execution: This is how the DAO implements what it has decided upon. It is an "on-chain" process. This step uses YAM Execution Proposals (YXPs).

The [Gov-Ops Council](https://github.com/yam-finance/documents/blob/master/govops/govops-council.md) provides assistance with the governance process, including facilitation for determining consensus and execution of routine and minimal proposals.

You can read more about why the process is structured this way [here](https://rossgalloway.github.io/docs-website/docs/siloDocs/YAM%20Re-Org/Deliverables/YAM%20Replanted%20Docs/Goals%20for%20a%20New%20Yam%20DAO/efficiency)

## Consensus Process (off-chain)

:::note

The YAM governance process has recently had an overhaul. The core governance contracts remain unchanged, but the implementation and execution of the process has changed.

:::

There are 2 types of consensus governance interactions: DAO upgrades (YIPs) and Grant Administration (GAPs). Both these types follow the consensus and execution steps, but have different requirements and are used for different types of proposals. YIPs are used to make changes to the DAO and GAPs are used to allocate funding for different projects.

### DAO Upgrades (YIP Process)

DAO upgrades include changes to the existing rules or operation of the DAO. These upgrades may be proposed as the result of work from a grant, or simply as an idea to improve something.

1. DAO upgrades follow the YIP governance process, which begins on the [Yam Governance Forum](https://forum.yam.finance/) and [Yam Discord](https://discord.gg/qceE8SQjXs) where ideas are initially discussed by token holders.
2. Once the idea has been discussed, the proposer writes and posts their proposal to the [proposals section of the forum](https://forum.yam.finance/c/proposals/9). The community signals its interest and may suggest modifications to the proposal.
3. After recieving feedback a vote on the proposal can be created on [Snapshot](https://snapshot.org/#/yam.eth) (off-chain voting), where tokenholders vote on it.

:::caution

Proposing a snapshot vote without sufficient discussion runs the risk of the Gov-Ops council refusing to add it to a YXP, or the guardian multi-sig signers vetoing the on-chain execution.

:::

If a YIP requires additional work to be implemented and executed, and that work is outside the scope of the [Gov-Ops Council](https://github.com/yam-finance/documents/blob/master/govops/govops-council.md) then that work needs to be done by the proposing party. Funding to do this work can be provided via the grant process. **Just because a YIP passes a snapshot vote does not mean that someone will implement it.** If additional work is expected, Gov-Ops Council members may recommend that a YIP proposer request grant funding prior to submitting their YIP.

An example of a YIP that doesn't require additional code work is a rebalance of the YAM treasury from one approved asset to another approved asset. If the parameters of the rebalance are specified in the YIP then this work falls within the scope of the Gov-Ops council to execute in a YXP.

#### YIP Timeline

- Forum and Discord Discussion: 3+ days
- Snapshot Off-Chain Vote: 3+ days, avoid holidays and weekends.
- Upon passing, on-chain execution will occur in the next scheduled YXP (typically occuring monthly) assuming all information and requirements are met.

### Grant Administration (GAP Process)

Grant Administration is the process by which the DAO determines what it is going to fund. Grants are the vehicles the DAO uses to pay for work done on its behalf. This process includes the initial application grant, the vetting of the proposed work to be done, and the review of deliverables once completed. 

1. Grant applicants start by submitting a new Silo Creation Application (if an applicable silo doesn't exist) or a Silo Extension Application (if one does). Token holders can then give feedback on the idea included in the application, allowing the applicant to cater their proposal to the DAO's needs and preferences. 
2. The next step is the creation of a specifications document, which defines the scope, deliverables, requirements, and specifications for the project that will be funded by the grant. The specification document is submitted both on the YAM Governance Forum and on Github so it can be added to the YAM Governance Repository. It will be reviewed by the Gov-Ops council for completeness and by token holders for quality.
3. Once the specifications document is complete, the applicant then submits a grant proposal, also on the forum and Github. This document should reference the specification document and propose a request for funds to do the work, as well as a timeline to do so.
4. After posting the grant application, the applicant should create a snapshot vote for token holders to determine whether they want to fund the grant or not.

#### GAP Timeline

- Silo Application, Specification Document, Grant application discussion: 3+ days after final docs are posted
- Snapshot Off-Chain Vote: 7+ days
- Upon passing, work on the project should begin.
- Upon completion of milestones specified in the grant proposal, payment requests should be posted to the governance forum and github.
- Payment will occur in the next scheduled YXP (typically occuring monthly) assuming all information and requirements are met and the payment is not disputed.

### Proposing and reaching Quorum for Consensus Votes (Snapshot)

To propose a snapshot vote, A proposer must have > 100 BoU YAM (251 scaled) delegated to their address.

In order to pass, a proposal must reach quorum which means that a certain threshold of total voting power votes "for" the proposal. For snapshot votes, this number is 200,000 BoU YAM ([what does BoU mean?](FAQ_new.md)) or 500,000 scaled YAM, equivalent to 4% of the initial token supply.

## Execution Process (on-chain YXP Process)

The execution process (YXP) starts after the consensus process has completed. As the name suggests, this is how any on-chain actions required by YIPs or GAPs are executed. On-chain execution proposals use the DAO's Compound Governor based smart contracts and are able to interact directly with the treasury and other smart contracts owned by the Yam DAO. While anyone can propose an on-chain vote by callign the governor contracts directly, the Gov-Ops council is empowered to submit proposals on behalf of the token holders. These (typically monthly) proposals will include all the routine actions for that month that have been approved via consensus voting (YIPs and GAPs). For more information about what is considered routine, see [this post](https://github.com/yam-finance/documents/blob/master/govops/govops-council.md)

Separating the execution from the consensus phase has 2 advantages. First, it allows token holders to vote for free in the consensus phase, using snapshot. Second, it bundles all the smart contract execution, which requires vetting, into one package that can be reviewed and tested all together. On-chain proposals will be posted to the YAM organization Github and announced on discord when they are ready for review. After at least 2 days of open review, if not problems are found, the vote and transactions will be submitted to the governor contract for token holders to vote on.

If the transactions required to be executed fall outside of the scope of work of the Gov-Ops council then the code required to execute those transactions will need to be written (or coordinated) by the party submitting the consensus votes. Whether that code will need to be audited will be determined on a case by case basis by the Gov-Ops council.

#### YXP Timeline

- Pre-requisite: Pass consensus phase
- Coordinate with Gov-Ops council on the code needed to execute the proposal. If needed, write, or coordinate the writing of that code: As long as needed.
- Proposal submission and voting: 2 days.
- Timelock delay: 5 days.

### Proposing and reaching Quorum for Execution Votes

To propose an on-chain vote, the proposer must have 50,000 BoU YAM (125,000 scaled) delegated to their address. They must maintain this minimum amount of YAM in their wallet throughout the entire voting and timelock period.

In order to pass, a proposal must reach quorum which means that a certain threshold of total voting power votes "for" the proposal. For on-chain votes, this number is 200,000 BoU YAM ([what does BoU mean?](FAQ_new.md)) or 500,000 scaled YAM, equivalent to ~4% of the initial token supply.

## Other important information

### Delegation

In order to vote, you must delegate your vote to yourself or to someone else. This applies to off-chain snapshot voting as well. Any YAM tokens being used as an LP in Yam's incentivizer farming Yams are automatically delegated to self. You can currently delegate to yourself or others via [yam.finance](https://yam.finance/#/governance). You can also delegate via [etherscan](https://etherscan.io/address/0x0aacfbec6a24756c20d41914f2caba817c0d8521#writeContract#F9) directly.

### Voting with LP tokens

Liquidity Providers to the [Sushiswap](https://sushi.com) Yam/ETH pool who stake thier SLP tokens in Yam's [incentivizer](https://yam.finance/#/farm) can vote with those tokens as well. You need to register to vote (delegate to yourself). If you have YAM tokens in both a wallet and in the incentivizer contract, we recommend delegating via etherscan so that both locations are counted toward your total voting power. If you need help with this, please come by the discord and ask.
