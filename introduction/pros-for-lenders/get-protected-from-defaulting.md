# Get protected from defaulting

Lenders will not incur losses due to borrower defaults. In the event of bad debts, the protocol covers the losses instead of the individual lenders. This means that in a peer-to-pool lending model, lenders earn interest rather than taking on the role of liquidators.

**Example with Peer-to-Peer Lending:** Alice lends out 0.1 BTC secured by an asset. If the asset's value drops to a 0.05 BTC floor price during the 10-day loan period and the borrower defaults, Alice loses 0.05 BTC.

**Example with Peer-to-Pool Lending:** Alice deposits 0.1 BTC into the peer-to-pool. A borrower takes a loan of 0.05 BTC from the pool when the asset's floor price is 0.1 BTC. If the borrower is liquidated when their asset is valued at 0.06 BTC, Alice can still withdraw her 0.1 BTC plus any accrued interest at any time from the pool.
