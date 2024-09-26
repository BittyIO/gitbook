# Get protected from defaulting

Lenders will not incur losses due to borrower defaults. In the event of bad debts, the protocol covers the losses instead of the individual lenders. This means that in a peer-to-pool lending model, lenders earn interest rather than taking on the role of liquidators.

### Examples

#### Peer-to-Peer Lending

1. Alice lends out 0.1 BTC secured by an asset.
2. The ordinals floor price drops to a 0.05 BTC during the 10-day loan period and the borrower defaults.
3. Alice end up with losing 0.05 BTC.

#### Peer-to-Pool Lending

1. Alice deposits 0.1 BTC into the peer-to-pool.
2. A borrower takes a loan of 0.05 BTC from the pool when the ordinals floor price is 0.1 BTC.
3. The ordinals is liquidated when their asset is valued at 0.06 BTC.
4. Alice can still withdraw her 0.1 BTC plus any accrued interest at any time from the pool.
