# What is Health Factor

The health factor has a good explanation by aave doc [here](https://docs.aave.com/faq/borrowing#what-is-the-health-factor) and  [here](https://docs.aave.com/risk/asset-risk/risk-parameters#health-factor).

Example for Ordinals:

* `Alice use 1 ordinal with floor price 0.2btc as collateral to borrow 0.1btc`
* `This ordinals collection has a liquidation threshold of 80%`
* `Health Factor for this loan is (0.2 * 0.8)/0.1 = 1.6`
* `When the debt is 0.16 or the floor price of this ordinals drop to 0.125, the health factor will be 1 which means anyone can start a auction for this ordinals`

Example for BTC/BRC20/Runes:

* `Alice use 1 btc with price 60k USD borrow 40k stablecoin`
* `BTC has a liquidation threshold of 80%`
* `Health Factor for this loan is (60k * 0.8) / 40k = 1.2`
* `When the debt is 48k or the price of BTC drop to 50k, the health factor will be 1 which means anyone can liquidate this loan`

The different thing in Bitty bitcoin lending is that since bitcoin has no smart contract that can make the multi-assets liquidation in one transaction provided by other swap protocol, all the HF in bitty is collaterals position based instead of wallet address based, which means you can not share margin between different collaterals.

