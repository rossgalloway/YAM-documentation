---
sidebar_position: 4
sidebar_label: "Optimistic Grants"
---

# Optimistic Grants

## What are they?

Optimistic Grants are a way to streamline the YAM grants process and limit token holder overhead while maintaining security and accountability for the DAO. Optimistic grants are conceived based on inspiration from other “optimistic” models for systems such as Element.fi’s [optimistic grants program](https://docs.element.fi/governance-council/council-protocol-smart-contracts/optimistic-grants), Joey Santoro’s [Optimistic Approval](https://medium.com/fei-protocol/decentralized-governance-structures-9c4eb8a3e452), and the way optimistic rollups work.

The term “optimistic” refers to the expectation that the person doing the work will complete the work. That is the default state, but there are easy ways to make a dispute in which the matter is escalated to the standard verification methods. Optimistic models use governance as an adjudication layer that is only used if needed. It relies on there being at least one person who is paying attention and willing to make a claim of wrongdoing.

In the model described here, once a grant proposal is submitted and approved, the milestone payments for the grant would be paid without a full snapshot vote upon posting of the completion of the milestone, unless an objection is made. Only if an objection is made would the payment be contested and go to a snapshot vote. Unlike the [Element.fi](http://Element.fi) version of optimistic grants which uses a specific contract to hold funds, there will still need to be an on-chain vote to pay the grant recipient from the treasury, but this payment would be routine and included in the monthly on-chain transaction.  

### The full process would be as follows

1. The grant applicant would go through the application process as described [here](the-grants-process.md) in which the scope of work and deliverables for the project are laid out and approved.
2. Work begins on the project funded by the grant and when the first deliverable or milestone is completed per the approved grant specification, it would be posted for review.
3. If there are no objections then payment for the milestone will be added to the next on-chain transaction. If an objection is raised about the work then it should be posted and reviewed and a snapshot vote created to determine whether the payment or grant contract need to be adjusted.
4. After the snapshot vote, the approved path forward is followed and any payment is added to the next on-chain transaction.

### Questions to answer

- How much time should a milestone be reviewed for before it is paid? There should be a minimum amount of time to ensure that the work can be reviewed and any objections brought up.
- How much time for evidence and rebuttal should be allowed after a milestone is objected to? This needs to be calibrated to prevent griefing attacks where someone submits a protracted objection to prevent timely payment, but also allow enough time for governance to understand if the contract has been breached.
- What kind of process, templates, and documentation is needed for effective oversight? A document that explains why the payment is being objected to with evidence and rationale sets the standard for effective objections.
