# Liquidation-protection (ordinals)

If [health factor ](../../faq/what-is-health-factor.md)of your ordinals collateral is below 1, your collaterals may be triggered to be auctioned, you can repay half of the debt in [144 blocks](../../faq/what-is-144-+-3-blocks-ordinals-auction.md) before the auction been finished with a fine of max(0.005 BTC, 5% \* debt) to redeem your ordinals.

This is very important to make sure that you won't wake up with your ordinals been taken from you can hard to buy it back.

For example:

* Alice bought an ordinals at 0.2 BTC
* Alice borrow 0.1 BTC from Bitty by 50% of the floor price 0.2 BTC
* Alice forget to repay the loan before the ordinals get auctioned because she was too busy
* Alice repay some BTC and 0.005 BTC(5% of the debt) to end the auction, keeping her ordinals health factor > 1.5

**The auction protection is not working in the** [**+3 block**](../../faq/what-is-144-+-3-blocks-ordinals-auction.md)**, which means the ordinals owner can only end the auction in 144 blocks.**
