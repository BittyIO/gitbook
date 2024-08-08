# 24-hours-liquidation-protection (ordinals)

If you ordinals accidentally be triggered to liquidation, you can repay half of the debt in 24 hours before the auction been finished with fine of max(0.005btc, 5% \* debt) to redeem your ordinals.

This is very important to make sure that you won't wake up with your ordinals been taken from you can hard to buy it back.

For example:

* Alice bought a NodeMonke at 0.2btc
* Alice borrow 0.1btc from Bitty by 50% of the floor price 0.2btc
* Alice forget to repay the loan before the NodeMonke get auctioned because she was too busy
* Alice repay some BTC and 0.005btc(5% of the debt) to end the auction, keeping her NodeMonke health factor > 1.5
