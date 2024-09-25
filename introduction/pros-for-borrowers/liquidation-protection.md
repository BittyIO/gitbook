# Liquidation-protection (ordinals)

If the [health factor](../../faq/what-is-health-factor.md) of your ordinals collateral falls below 1, your collateral may be triggered for auction. However, you can repay half of the debt within [144 blocks](../../faq/what-is-144-+-3-blocks-ordinals-auction.md) before the auction concludes, with a fee of either 0.005 BTC or 5% of the debt—whichever is greater—to redeem your ordinals.

This feature is crucial, as it ensures you won't wake up to find your ordinals taken, making it difficult to buy them back.

**Example:** Alice purchased an ordinal for 0.2 BTC and borrowed 0.1 BTC from Bitty, using 50% of the floor price as collateral. Due to her busy schedule, Alice forgot to repay the loan before the auction started. To stop the auction, she repaid some BTC along with a 0.005 BTC fee (5% of the debt), successfully keeping her ordinals' health factor above 1.5.

**Note that auction protection is not available during the first** [**3 blocks**](../../faq/what-is-144-+-3-blocks-ordinals-auction.md)**, meaning the ordinals owner has only 144 blocks to end the auction.**
