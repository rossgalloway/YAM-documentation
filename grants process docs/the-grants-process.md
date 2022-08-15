---
sidebar_position: 5
sidebar_label: "Grants Process"
---

# Grants Process

## Requirements Document

The first document that is needed to accurately determine the value of the grants proposal is a requirements document. This is a type of specification document that clearly lays out the goals and requirements that the project intends to achieve. This document is of critical importance because it provides the information that YAM token holders will use to evaluate whether a grant has been successfully completed.

---

**A requirements document may contain the following information:**

- What is the overall goal and purpose of the project?
- What problem does the project solve?
- Are there other potential ways to solve this problem? Why choose this one?
- Who are the participants/users of the project
  - What role does each user type have?
  - What skills do they need?
  - how will each user type interact with the project?
  - What is the full user flow for this project. Is this all part of the scope?
- What are the functional requirements of the project?
  - When complete user A must be able to do [blank]… etc.
  - When complete user B must not be able to do [blank]… etc.
- What are the non-functional requirements of the project?
  - For example, if it is a website, what browsers can run it? Will there be a mobile site?
  - Will it have multiple language support
- What are the design principles or other principles that guide the project?
- Are there other projects or contracts that the project will interact with? How will they do so? What are the security risks from these interactions?
- Are there security assumptions built into this project? If so what are they?
- Is it possible for any party to lose money via this project? How so?
- Are there similar examples to the proposal that token holders can use to compare or understand the scope?
- Timeframe expected to fulfill different parts of the scope, as well as full completion of the project.
- Expected compensation for completion of the project and/or specific milestones.

This list is not exhaustive and not all questions above will be relevant for all projects. Some projects may choose to split work up into smaller sections and so the requirements document may evolve and be added to over the course of multiple grants.

## Requirements Document Pre-Grants

Formulating a strong requirements document takes time and effort. Because it is such an important document in assuring accountability and the functioning of a robust grant system, we believe that there should be a mechanism to compensate applicants who work in good faith with the DAO to create this document. Funding of a grant will often be contingent on this document, but simply having one will not assure that the main grant receives funding.

The DAO should consider what kind of compensation it can offer for a well crafted requirements document even if the proposal is not ultimately approved by governance. This can also apply to requirements documents that are crafted as part of a Request for Proposal process. This is a relatively low stakes investment for the DAO and defrays the upfront costs to proposal writers.

## The Process in Practice

![GRANT FLOW 1.jpg](/grant-flow-1.jpg)

### Proactive Applications

1. Alice has a project that she would like to work on that she believes will benefit the YAM DAO and is looking for funding to build. She fills out an application form on the YAM forum stating her intention to write a comprehensive requirements document for the project.
2. After some discussion, A snapshot vote is created to decide whether YAM token holders think this the project sounds promising and wish to fund a Pre-Grant for Alice to write the requirements document.
3. Upon approval of the pre-grant via snapshot vote, Alice proceeds to write the requirements document, and work with Token holders and other YAM contributors to refine the document.
4. Upon completion of the requirements document, it should be published for public review along with the proposal to do the work to allow other parties to submit their own proposals based on the requirements document. Diana submits a competing proposal to do the work based on the requirements document.
*This review period enables other parties to review the work and offer competing bids, giving YAM token holders better information and more options.*
5. Following the review period, a new snapshot vote is created to determine whether, and to whom, the Project Grant will be given out. There should be 3 options for token holders to vote for. Any payouts will occur in the next on-chain proposal.
    - If the main grant is approved according to the requirements document and given to the original proposer (Alice in this case) then the pre-Grant should be approved for payout in the next transaction. The main grant agreement will go into effect and Alice can begin work on the project.
    - If the main grant is approved according to the requirements document, but governance chooses the bid from Diana over the original proposer, Alice, then the pre-grant should still be approved for payout to Alice in the next transaction. The main grant agreement will be given to Diana and she can begin work on the project.
    - If the main grant is not approved, but the work on the requirements document is deemed to have met the scope of the pre-grant then the pre-grant will be approved for payout to Alice, but no further work on the project will be compensated.
    - If the main grant is not approved and the work on the requirements document is  not deemed to have met the scope of the pre-grant agreement then there will be no payout.

### Alternate Proactive Option (no pre-grant approval)

1. Bob has a different project that he would like to apply for a grant for. He does not apply for a pre-grant, but writes a full requirements document and proposes the project to YAM governance. After a public review period where token holders can vet and discuss the project, and other parties can submit bids on the work, the proposal goes to a snapshot vote with the same 4 options that Alice has. If Bob does not win the project, but someone else does then he should receive the standard pre-grant payment.

### Request For Qualifications (RFQ) Applications

1. Charlie sees a need that the DAO needs filled, and while he cannot do the work himself, he can create a requirements document to specify what needs to be done. He fills out an application form to create a new requirements document as part of the RFQ track.
2. Like Alice, he can apply for a Pre-Grant for this work via snapshot vote.
3. Upon approval of the pre-grant, Charlie proceeds to create the requirements document for the potential work. Upon completion of the requirements document, Charlie posts it publicly and requests his grant be paid out.
    - The default outcome is one where the work has been completed satisfactorily and no action is required. The pre-grant is paid out according to the terms of the agreement in the next on-chain vote.
    - If any token holder believes that the work done does not meet the terms of the pre-grant agreement, then they can raise an objection and create a new snapshot vote to determine whether the pre-grant should be paid, not paid, or re-negotiated.
4. The completed requirements document is made publicly available and publicized as ready to receive offers to do the work. A minimum amount of time for which offers are accepted should be publicized. At the end of that period, if multiple offers have come in then Token holders should decide which offer they want to accept, or if none are acceptable either wait or try to negotiate the offers. If no offers have come in then the RFQ should remain open until an offer is accepted.

### Grant Completion (both tracks)

1. At the intervals specified in the requirements documents for each project, the deliverables that are specified are presented publicly in order for token holders to determine whether the work that was promised was completed. This model is described in the [Optimistic Grants](optimistic-grants.md) section.
    - The default outcome is one where the work has been completed satisfactorily and no action is required. The grant is paid out according to the terms of the agreement in the next on-chain vote.
    - If any token holder believes that the work done does not meet the terms of the grant agreement, then they can raise an objection and create a new snapshot vote to determine whether the grant should be paid, not paid, or re-negotiated.
2. If there is further work to be done, a new grant can be created to continue the work, using the same process.

❗ All work done for the DAO should be open source and published under a CC0 license unless otherwise negotiated. More complex deals that may involve tokens or equity in a project should be thoroughly negotiated with the DAO beforehand.
