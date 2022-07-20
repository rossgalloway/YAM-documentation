# History

Official YAM (YamV3) Token: [Sushiswap] - [Etherscan] 0x0aacfbec6a24756c20d41914f2caba817c0d8521

## Yam Versions

The original YAM protocol was launched August 11, 2020, but had a critical bug that disabled any future governance and control of the treasury. Tokenholders migrated to YAMv2 in order to vote on the parameters for a V3 launch while the protocol was audited. On September 18, 2020, the fully functional YAM protocol was released and V2 tokenholders can now [migrate](https://yam.finance/farm#/Migrate) to the new YAM token.

Below are the correct token addresses for each version:

Official YAM (YamV3) Token: [Sushiswap] - [Etherscan] 0x0aacfbec6a24756c20d41914f2caba817c0d8521

### Obsolete Addresses

YAMv1: [Etherscan] 0x0e2298e3b3390e3b945a5456fbf59ecc3f55da16

YAMv2: [Etherscan] 0xAba8cAc6866B83Ae4eec97DD07ED254282f6aD8A

### YAMv1 Summary

YAMv1 experienced a critical bug that disabled governance. You can read [the post-mortem](https://medium.com/yam-finance/yam-post-rescue-attempt-update-c9c90c05953f) for full information.

Token address: 0x0e2298e3b3390e3b945a5456fbf59ecc3f55da16

### YAMv2 Summary

Following the successful audit funding in the wake of the V1 bug, the launch team deployed a migration contract enabling migration from V1 to a stable, vanilla ERC20 YAMv2. The V2 token was to be used for voting on key issues for the relaunch of YAM, while the protocol was being audited. A summary of the V2 interim governance period can be found [here](https://medium.com/yam-finance/the-road-to-v3-yamv2-interim-governance-summary-f17ba4a9d1aa).

Token address: 0xAba8cAc6866B83Ae4eec97DD07ED254282f6aD8A

### YAMv3 (current)

The recently launched YAM is the token of the fully functional Yam protocol and governance. It rebases every 12 hours and can be used to participate in Yam governance. December 29th, 2020 the Yam community has voted to disable the rebasing / elastic supply function of Yam and the scaling factor of Yam has been fixed at 2.50.

Token address: 0x0aacfbec6a24756c20d41914f2caba817c0d8521

## Rebase Basics

December 29th, 2020 the Yam community has voted to disable the rebasing / elastic supply function of Yam and the scaling factor of Yam has been fixed at 2.50.

Below is just for historical purposes:

Rebasing is a mechanism generally used to promote price stability by increasing the supply when the price is above the target price and decrease supply when price is below the target. YAM is currently pegged to 1 USDC, and uses the YAM/ETH  and ETH/USDC Sushiswap pools to generate a two-hop TWAP (Time-Weighted Average Price) oracle to determine the necessary change in supply.

- If YAM price is above 1.05 USDC, YAM supply increases. This is known as a positive rebase.
- If YAM price is below 0.95 USDC, YAM supply decreases. This is known as a negative rebase.
- If YAM price is between 0.95 and 1.05 USDC, YAM does not rebase.

When a rebase occurs, the `scalingFactor` within the token itself changes, which automatically updates the balance of the tokens. In other words, all YAMs are always rebased. In the Yam protocol, when a positive rebase occurs, 5% of the YAM rebase amount is minted and sold for ETH via the YAM/ETH Sushiswap pool. The ETH is subsequently deposited to the governance-controlled treasury.

### Rebase Calculation

To begin calculating the change in supply in a rebase, you can determine how far from the peg the current price is: (Current Price - TargetPrice) / Target Price = Deviation From Peg

Example: If Current Price is $1.10 and Target Price is $1, the deviation from the peg is  (1.10 - 1) / 1 = 0.10.

To smooth the rebasing mechanism, we divide this deviation by 20 rebase periods in the change in supply calculation below. This means if no other buys or sells occur, after 20 rebases, the price target will be met. This is called the RebaseLag.

If the current supply is 5,000,000, then the change in supply will be 5,000,000 *(0.10/20) = 25,000.

The new total supply would then be 5M + 25,000 = 5,025,000.

To calculate the amount of Yam minted for the treasury and sold to the YAM/ETH pool, you multiply the change in Supply by 5%. In this example, it would be 25,000* 0.05 = 1,250 YAM minted to the treasury.

### MaxSlippage Limit

To mitigate excess market impact of a treasury purchase during rebase, there is a cap on the amount of slippage the protocol will create with its sale, currently set to 5%.

It should be noted that if there is excess YAM in the treasury due to a rebase hitting MaxSlippage on a previous rebase, the treasury will sell YAM up to the MaxSlippage amount, which may be more than it would have minted.

### Liquidity Providing

Rebasing tokens are considered non-standard ERC20s, meaning they include functionality outside of the norm. In the case of protocols like Uniswap and Balancer, these platforms are not properly equipped to handle rebases. They do not recognize the changes in token balances properly, even though those balances have changed, and malicious actors and bots can steal the rebased tokens.

These platforms do have functions that can be called to prevent this behavior, which can be added to the rebase function. For Uniswap and Sushiswap, this is the sync() function and is currently called on the YAM/yUSD Uniswap and YAM/ETH Uniswap and Sushiswap pools during rebase.

All other Uniswap and Sushiswap pools are unsafe during rebases, as are all Balancer pools.

### TWAP Oracle

In order to perform the rebase calculation, the Yam protocol uses the TWAP (Time-Weighted Average Price) oracle provided by the Sushiswap pools. This measures the average price between each rebase and is used to determine the price used in the rebase calculation.

As the treasury purchase pool is YAM/ETH but the target price is 1 USDC, the TWAP is calculated using two hops; first calculating the TWAP of YAM:ETH and then ETH:USDC. This allows us to get the price of YAM:USDC by multiplying the TWAPs (thus cancelling out the ETH in the denominator and numerator).

### Gitcoin Grants Funding

During the YAMv2 interim governance period, a proposal was submitted and approved to donate 1% of all treasury purchases to Gitcoin Grants in order to help fund open source public goods for the Ethereum community.
