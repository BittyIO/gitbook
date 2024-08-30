# What is 144 + 3 blocks ordinals auction

The 144 + 3 blocks auction is that the ordinals will be liquidated by an on-chain auction system.

144 blocks is close to 24 hours (6 \* 24 blocks) , which make sure that every ordinals owner won't lose their ordinals after a sleep/flight, **the ordinals owner can only stop the auction in 144 blocks after the auction started, which means the +3 is not working for the liquidation protection for the ordinals owner**.

The +3 blocks means that if no higher bid in 3 blocks after 144 blocks, the auction ends.

Example 1:

* `Alice borrowed 0.1btc from Bitty when her ordinals floor price is 0.2btc`
* `Alice can't repay that loan when the floor price is close to 0.12 btc`
* `Alice's ordinals started been auction at bitcoin block height #1000`
* `The highest bid is 0.11btc at block height #1144 (the` [`liquidation protection`](../introduction/pros-for-borrower/liquidation-protection.md) `stop here)`
* `No more bid at block height #1147, the auction ends, the 0.11btc bidder win the auction`

Example 2:

* `Alice borrowed 0.1btc from Bitty when her ordinals floor price is 0.2btc`
* `Alice can't repay that loan when the floor price is close to 0.12 btc`
* `Alice's ordinals started been auction at bitcoin block height #1000`
* `The highest bid is 0.11btc at block height #1144 (the` [`liquidation protection`](../introduction/pros-for-borrower/liquidation-protection.md) `stop here)`
* `At block height #1147, a new bid with 0.12btc is been confirmed, the auction continue`
* `At block height #1150, no new bid is confirmed, the auction ends, the 0.12btc bid win the auction`



**Why bitty use block height instead of timestamp for auction?**&#x20;

Because we do not want user to risk on block time from block to block, sometimes, bitcoin block can generate two blocks at the same time, and the longest time between two block is two hours.

But it would be a very low chance that the bitcoin system to have three blocks at the same time.

So use the block height instead of timestamp can make sure that user can send auction transaction with high gas in mem-pool instead of lucky on block time to make auction, and it will reduce the advantage for mining pool if they want to take advantage on auction.
