# Interest rate

Holds the information needed to calculate and update the interest rates of specific reserves. Each contract stores the optimized base curves using the corresponding parameters of each asset.

The parameters for the optimized base curves are:

* baseVariableBorrowRate
* variableRateSlope1
* variableRateSlope2
* stableRateSlope1
* stableRateSlope2

The interest rates are calculated depending on the available liquidity and the total borrowed amount from block to block.

If you want to know more details about the algorithm about how to calculate the interest rate from block to block, check [this](https://www.rareskills.io/post/aave-interest-rate-model) article.
