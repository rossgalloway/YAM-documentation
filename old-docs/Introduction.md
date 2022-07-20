# Introduction
Welcome to Yam!

## What is Yam?

Official YAM Token: [sushiswap]-[etherscan] 0x0aacfbec6a24756c20d41914f2caba817c0d8521

Yam launched on August 12th, 2020 as An Experiment in Fair Farming, Governance, and Elasticity. Yam Protocol mashes up some of the most exciting innovations in programmable money and governance. Built by a team of DeFi natives, but now controlled by the community.

On December 29th, 2020 the Yam community has voted to disable the rebasing / elastic supply function of Yam and the scaling factor of Yam has been fixed at 2.50. 

Originally, YAM was an elastic supply cryptocurrency, which expanded and contracted supply in response to market conditions, targeting 1 USDC per YAM. This stability mechanism was supplemented by one key addition to existing elastic supply models: a portion of each supply expansion was used to buy yUSD/ETH and added to the Yam treasury, which is controlled via Yam community governance.

YAM now acts as a DAO governance token and has evolved into a launch pad for DeFi projects supported by a community governed treasury. Yam is currently developing multiple projects including Umbrella (Smart Contract Insurance),  (Synthetics) and Yam DAO Set (Set Protocol DAO Investment fund). All of which will generate revenue for Yam. For most current projects, please visit us on [Discord]
.

## Fair Launch

YAM was launched using a fair distribution method inspired by YFI, in which users could stake cryptocurrencies to receive a pro rata distribution of YAM each block. There was no pre-mine, and neither the launch team nor VCs received any shares outside the prescribed rules of distribution to which all had access.

This form of distribution had two goals:

- To ensure Yam was truly a community owned and governed protocol.
- To align interests with the communities of the staked tokens, all of which had potential value and experience to add to the Yam protocol

​[medium-article]
​
## Rebase

Rebasing mechanism had been disabled by community governance as of Dec 29th, 2020. 

Below is just for archival purposes: 
Rebasing is a mechanism generally used to promote price stability by increasing the supply when the price is above the target price and decrease supply when price is below the target. YAM is currently pegged to 1 USDC, and uses the YAM/ETH Sushiswap pool to generate a TWAP (Time-Weighted Average Price) oracle to determine the necessary change in supply.

- If YAM price is above 1.05 USDC, YAM supply increases. This is known as a positive rebase.
- If YAM price is below 0.95 USDC, YAM supply decreases. This is known as a negative rebase.
- If YAM price is between 0.95 and 1.05 USDC, YAM does not rebase.

When a rebase occurs, the `scalingFactor` within the token itself changes, which automatically updates the balance of the tokens. In other words, all YAMs are always rebased.
In the Yam protocol, when a positive rebase occurs, 5% of the YAM rebase amount is minted and sold for ETH via the YAM/ETH Sushiswap pool. The ETH is subsequently deposited to the governance-controlled treasury.

## Decentralized Governance

YAM launched with fully decentralized governance from Day 1 by implementing the Compound governance module. This gives control of the protocol to YAM tokenholders, meaning that updates to the protocol and management of the treasury can only be performed with approval from YAM holders.

The governance process begins on Yam Discord where ideas are initially discussed. Once discussion has formalized a potential proposal it is submitted to Yam Governance Forum. If the community signals its interest and any necessary modifications to the proposal are made, the proposal is submitted to Snapshot off-chain governance, where tokenholders can vote with their token balances.

If a Snapshot proposal is passed and no code is required to be implemented, the approved action can be taken.

If code deployment is required, the code will go to audit if necessary, and then be proposed via on-chain governance at which point tokenholders will vote on-chain to deploy.
