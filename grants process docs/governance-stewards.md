---
sidebar_position: 3
sidebar_label: "Governance Stewards"
---

:::warning

needs updating

:::

# Governance Stewards

## TL:DR

To improve DAO accountability and participation, create a new, paid, open community role for part time governance work that can be applied for in a similar way to how the current grants model works. This is an extension and generalization of the Treasury Director role created in [YIP-113](https://forum.yam.finance/t/yip-113-yam-treasury-director-creation/1719).

## Introduction

The Gov-Ops council was created as a facilitating, non-opinionated, closed group who are tasked with making sure the governance system is running smoothly and that all participants in the system understand what their roles and responsibilities are. They are explicitly not a steering committee for the DAO and could be better seen as the DAO’s minimal administrative arm.

Because Gov-Ops is intentionally unopinionated, there is still a need for a person or persons who are opinionated about the quality and quantity of work being done by grant recipients and other contributors. This is the intent, as I understand it, of the Treasury Director ([YIP-113](https://forum.yam.finance/t/yip-113-yam-treasury-director-creation/1719)) proposal. I agree with the idea that accountability needs to be enforced, but I do not think that YIP-113 frames the problem correctly, and as a result will not be an effective long term solution.

With that said, we must ask how can we create a long term solution that achieves the goal of improved accountability for grant recipients and other contributors. The first step is understanding the problem and constraints, and then using that understanding to craft a system that solves for those problems and constraints.

## The Problem

The broad problem that we are trying to solve is to ensure accountability of contributors and grant recipients. Secondary problems are a lack of participation by the broader community and a concern over the value of the work that is being paid for. Let’s look at each one:

### Accountability

I have written about accountability and the Re-Org [here](https://rossgalloway.github.io/docs-website/docs/siloDocs/YAM). The salient point from that post is this:

> YAM holders have one main tool to enforce accountability and that is control over the treasury and ability to withhold payment if promises are not kept. This is a powerful tool, but it is only effective if it can be used credibly and transparently.
>

This is no different from any other organization. Not performing to expectations risks getting fired and not being paid. In the carrot and stick analogy, this is the stick, and the (generous) pay package is the carrot. The difference between YAM and a normal company is who has the power to wield these tools to enforce accountability.

In a normal company, there is a boss who can recommend (or sometimes just implement) a firing, pay cut, pay raise, etc. This person has that control because there is someone else with the power to stop payment who will listen to them when they say “don’t pay this person anymore.”

Yam DAO does not work this way. The only way to pay (or not pay) someone is via governance vote. If you can pass a governance vote, you can pay someone. If you can’t, then you can’t pay them. Yam Token holders control the treasury and ultimately determine whether someone is paid not not. They therefore are the only party that can truly hold contributors and grant recipients accountable.

### Participation

I have also written about participation [here](https://rossgalloway.github.io/docs-website/docs/siloDocs/YAM%20Re-Org/Deliverables/YAM%20Replanted%20Docs/Goals%20for%20a%20New%20Yam%20DAO/participation). The salient point from that post is this:

> Participation is work. To do it well takes time and effort, and should therefore be compensated as such. We need to understand what kind of participation we can expect from different parties and incentivize that participation accordingly.
>

We have learned over the last year that we cannot simply expect active participation from token holders because they own tokens. Most token holders expect that at most they are going to need to occasionally vote, but not much else. The people who end up being informed and participate the most are the contributors who are paid to do work for the DAO. This makes sense. They have incentives that are not based on a sunk cost (earning future tokens vs appreciation of already purchased tokens).

## Constraints

The constraints on our model are based on both our existing infrastructure (practical) and the desire to operate in an open, decentralized, and permissionless way (ideological).

Our practical constraints are pretty clear and we have been working within them to craft the grants model and the Gov-Ops Council model. To make the system easy to implement we should try to stick to these already designed models as much as possible as long as they work reasonably well.

The most important ideological constraint is what I will call “Open-ness”. This refers to the ability for anyone to participate equally, and be compensated based on the value of their participation. Good advice and insightful analysis are not limited by the number of tokens one holds. Only the ability to act on that advice and analysis are. We have a gate for decision making and it is token weighted voting. All other gates should be as open as possible.

## A Solution: Governance Stewards

In thinking about the problems and constraints, it seems reasonable to assume that if we want to incentivize participation then the DAO should pay for quality participation. We now have a system that the DAO can use to set the standards and expectations for that participation. We can pay for participation similarly to how we pay grant recipients and gov-ops members. Token holders, as controllers of the treasury determine what participation is valuable, but do not limit who can attempt to participate valuably.

### How is this Different from YIP-113 (Treasury Director)

The model that I am proposing is really quite similar to what was proposed in YIP-113. In that proposal, there is a paid, part time position that is tasked with keeping up with the projects and proceedings of the DAO, review the various projects and give advice on whether they are valuable and should be continued.

But the YIP-113 proposal makes a number of assumptions about the powers of that position that are not enforceable within the current framework of the DAO without also making the assumption that the person in that position has the voting power to enact their recommendations. Reading between the lines, YIP-113 is essentially a request from a large token holder *who is already making decisions and enacting them via token voting* to be paid for their time to do the work to inform those decisions.

I don’t see anything wrong with this arrangement. On the contrary, what I am proposing is a generalization of this structure to allow more people to be paid to do the research and work to have informed decisions on the DAO. As I mentioned in the constraints section, the value of participation is not limited by the number of tokens one owns. It simply means that the output of that participation is a recommendation and not an imperative.

### Extending YIP-113

How can we extend the YIP-113 model? We need a set of criteria for what we expect from participants.

- Review and vet new grant and project proposals
- Review grant recipient compensation requests and work.
- Review operating procedures and proposed changes to the DAO structure when proposed.
- Submit recommendations and thoughts on the above in a structured way so that other participants and stakeholders can benefit from the analysis.

We also need a process by which prospective participants in the program can apply and then submit a request for compensation showing the work done and value added. We have the beginnings of this process in the grants model.

- We would need to adapt an application that would allow the applicant to describe their vision and priorities for YAM.
- Determine the expectation or cap for hours that can be billed.
- Determine the pay rate for this role.

> 💡 Idea Extension 1: This process could also extend into an effective model for delegation of voting power where these participants can advertise themselves and their views to other users who are looking to delegate their tokens. A threshold of delegated tokens could be a criteria to receive compensation from the treasury for this work.

> 💡 Idea Extension 2: At the end of the month or other payment period, a random number generator could be used to pick a day in that period in which the number of tokens delegated to each address is read from the governance contracts. Falling below the threshold would disqualify the Governance Steward from compensation in that month.

### Payment

Similar to payment for Gov-Ops and the Treasury director position proposed in YIP-113, the pay for Governance Stewards would be all in vested YAM. The vesting period and parameters could be determined specifically for the Governance Steward role or it could be kept the same 6 month linear vesting as other groups (grant recipients, gov-ops, etc).

### Other Options for Pay Structure

The grants-style model proposed above uses our existing processes, which makes it easier to implement, but there are other options that could be explored. Two off the top of my head are Coordinape and SourceCred.

**CoordinApe**

A Governance Steward Coordinator (Gov-Ops?) could create a Coordinape Circle and multi-sig that receives a set amount of funding each month, determined by token holders. All applicants for the Gov-Ops steward position would submit a wallet with their application and would be added to the  Circle. The Governance stewards would then distribute the tokens among themselves.

**SourceCred**

Sourcecred is more involved and is a system for paying out contributors based on the quantity and quality of contributions on different media (Discourse forums, github, discord, etc.). It uses a network graph of all participants and distributes an intermediate token to participants based on number of posts, number of likes on the posts, etc. That intermediate token can then be traded in for another token (YAM). While this takes more effort to set up and probably need maintenance, the system does not require anyone to adjudicate value. The model does that for you.

## Simple Specification

Create a new type of grant specially designed for part time contribution focused on governance.

- Stand up template application form, persistent storage location for applications/profiles, and template compensation request.
  - Re-use existing grant application infrastructure.
  - Provide a location either on the YAM Information repository site or the super site for these applications.
- Set expected monthly commitment to 20hrs (2.5 days/month)
- Set pay rate at $50/hour paid in 30-day avg priced YAM, 6 mo. linear vesting. ($1000 per steward/month)
- Set expectation for contribution work to entail:
  - Review and discussion of all Grant proposals and grant compensation requests (or concentrated review of a few, case made in compensation request).
  - Review and discussion around YIPs. Monthly report on work done as part of Compensation request.
  - Voting in all Snapshot votes that follow proper governance processes (forum post → discussion → vote)
  - Vote on monthly on-chain transactions

### Potential future additions

- Incorporation with vote delegation to further empower Governance Stewards.
- Requirement to have a certain amount of YAM delegated to the Steward Public address.
- Use of alternate payment flows (coordinape/sourcecred, etc)
