# What is 144 + 3 blocks ordinals auction?

The 144 + 3 block auction system is designed for the liquidation of ordinals through an on-chain auction. The 144 blocks roughly equate to 24 hours (6 blocks per hour), ensuring that ordinals owners won’t lose their assets unexpectedly due to a brief absence, such as during sleep or travel. However, once the auction starts, **ordinals owners can only end the auction within the 144 blocks by redeem,** **the additional 3 blocks do not provide liquidation protection for them.**

The +3 blocks serve a specific purpose: if no higher bids are placed within 3 blocks after the initial 144 blocks, the auction concludes.

Higher bid should be 1% more than last highest bid.

#### Example 1:

* **Scenario**: Alice borrowed 0.1 BTC when the floor price of her ordinals was 0.2 BTC.
* **Situation**: Unable to repay the loan, the floor price drops to around 0.12 BTC.
* **Auction Start**: Alice's ordinals are put up for auction at Bitcoin block height #1000.
* **Bid Progress**: The highest bid of 0.11 BTC is placed at bitcoin block height #1140 by Bob (the liquidation protection ends here).
* **Auction End**: Alice redeem her ordinals by paying 0.001btc as fine to Bob and keep her HF >= 1.1 to stop the auction at bitcoin block height #1142

#### Example 2:

* **Scenario**: Alice borrowed 0.1 BTC when the floor price of her ordinals was 0.2 BTC.
* **Situation**: Unable to repay the loan, the floor price drops to around 0.12 BTC.
* **Auction Start**: Alice's ordinals are put up for auction at Bitcoin block height #1000.
* **Bid Progress**: The highest bid of 0.11 BTC is placed at block height #1144 (the liquidation protection ends here).
* **Auction End**: No further bids are made by block height #1147, so the auction concludes with the 0.11 BTC bidder winning.

#### Example 3:

* **Scenario**: Same as above, Alice borrows 0.1 BTC with the same conditions.
* **Auction Start**: Her ordinals begin auctioning at block height #1000.
* **Bid Progress**: The highest bid of 0.11 BTC is placed at block height #1144 (liquidation protection ends).
* **New Bid**: At block height #1147, a new bid of 0.12 BTC is confirmed, extending the auction.
* **Auction End**: At block height #1150, with no new bids confirmed, the auction concludes with the 0.12 BTC bid winning.

#### Why Use Block Height Instead of Timestamp?

We prefer block height over timestamps for auction management to mitigate risks associated with varying block times. Occasionally, Bitcoin can produce two blocks simultaneously, and the longest interval between two blocks can be up to two hours. However, the chance of three blocks being generated at the same time is exceedingly low.

Using block height ensures that users can submit auction transactions with higher gas fees in the mempool, reducing the reliance on luck regarding block timing and minimizing advantages for mining pools that might attempt to exploit auctions.
