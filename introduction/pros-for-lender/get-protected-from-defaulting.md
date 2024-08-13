# Get protected from defaulting

Lender will not ends of losing money from the defaulting by borrowers.&#x20;

If any bad debts happened, it's covered by the protocol instead of the lenders.

For the peer-to-pool lending, lender is earning interests instead of being a liquidator at the same time.

For example:

* `Alice lender out 0.1btc for some asset in a peer-to-peer lending system`
* `The assets value drop to 0.05btc floor price in the 10 days loan`
* `The borrower defaulted the loan, Alice lose 0.05btc after the default`

When using peer-to-pool service, the example will be like:

* `Alice deposit 0.1btc into the peer-to-pool pool`
* `The borrower borrow 0.05btc from the pool when the floor price is 0.1btc`
* `The borrower got liquidated when his assets is valued at 0.06btc`
* `Alice can get 0.1btc + interests at anytime from the pool`
