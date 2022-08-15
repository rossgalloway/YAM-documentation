# Rebasing

## Rebase Basics

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
