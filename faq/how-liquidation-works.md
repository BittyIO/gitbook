# How liquidation works

In Bitty, we have both ordinals and BTC/Runes/BRC20 can be collaterals to borrow money.

The liquidation rules of ordinals are:&#x20;

* `Different ordinals as collaterals can not share margin with each other, each loan has it's own loan id individually.`
* `If any` [`health factor`](what-is-health-factor.md) `of ordinals collateral is below 1, the` [`144 + 3 blocks auctions`](what-is-144-+-3-blocks-ordinals-auction.md) `could be started.`
* `Anyone can join the on-chain auction, the platform would not get any money from that auction.`

The liquidation rules of BTC/Runes/BRC20 are similar to [aave](https://docs.aave.com/faq/liquidations):

* `Different assets as collaterals can not share margin with each other, each loan has it's own loan id individually, user can keep many loans positions using same type of asset.`
* `If any` [`health factor`](what-is-health-factor.md) `of collateral is below 1, on-chain auction could be started.`
* `There is no 144 blocks liquidation protection for BTC/Runes/BRC20.`
* `Anyone can join the on-chain auction, the platform would not get any money from that auction.`
