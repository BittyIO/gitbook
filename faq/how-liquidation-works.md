# How liquidation works?

Both of ordinals and BTC/Run can be used as collateral for borrowing funds.

#### Liquidation Rules for Ordinals:

* Different ordinals as collateral cannot share margins; each loan has its own unique loan ID.
* If the health factor of any ordinal collateral falls below 1, a [144 + 3 ](what-is-144-+-3-blocks-ordinals-auction.md)block auction may be initiated.
* Anyone can participate in the on-chain auction, and the platform does not receive any funds from these auctions.
* Each higher bid should be 1% more than last bid.
* The money (highest\_bid - debt) will go to the pool added to balance for original owner (Bitcoin has no smart contract to make it go back to owner directly because we can not know when the transaction will be confirmed).

#### Liquidation Rules for BTC/Runes:

* Similar to [Aave](../introduction/pros-for-borrowers/claim-airdrops-in-loan.md), different assets as collateral cannot share margins; each loan has its own unique loan ID. Users can maintain multiple loan positions using the same type of asset.
* If the health factor of any collateral drops below 1, an on-chain auction may be triggered by anyone.
* There is no 144-block liquidation protection for BTC/Runes

