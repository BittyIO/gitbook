# What is Health Factor?

The health factor is a crucial concept in cryptocurrency lending, as explained in the AAVE documentation [here](https://docs.aave.com/faq/borrowing#what-is-the-health-factor) and  [here](https://docs.aave.com/risk/asset-risk/risk-parameters#health-factor).

### Examples

#### Ordinals

1. Alice uses 1 ordinal with a floor price of 0.2 BTC as collateral to borrow 0.1 BTC.
2. This ordinals collection has a liquidation threshold of 80%.
3. Health Factor calculation: (0.2 \* 0.8) / 0.1 = 1.6
4. Liquidation risk:
   * If the debt increases to 0.16 BTC, or
   * If the floor price of this ordinal drops to 0.125 BTC, the health factor will reach 1, allowing anyone to initiate an auction for this ordinal.

#### BTC/BRC20/Runes

1. Alice uses 1 BTC (priced at $60,000 USD) as collateral to borrow $40,000 in stablecoins.
2. BTC has a liquidation threshold of 80%.
3. Health Factor calculation: (60,000 \* 0.8) / 40,000 = 1.2
4. Liquidation risk:
   * If the debt increases to $48,000, or
   * If the price of BTC drops to $50,000, the health factor will reach 1, allowing anyone to liquidate this loan.

### Unique Aspect of Bitty Bitcoin Lending

Unlike other platforms, Bitty bitcoin lending calculates the Health Factor (HF) on a per-collateral basis rather than a per-wallet basis. This is due to Bitcoin's lack of smart contract functionality, which prevents multi-asset liquidation in a single transaction (as provided by other swap protocols).

Key point: on Bitty v1.0, you cannot share margin between different collaterals, we will implement the BTC, BRC20, Runes share margin first, and do the margin share for ordinals as well in the future.

