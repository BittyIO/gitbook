# Get value from the auctions (ordinals)

If your ordinals are liquidated, the process involves a fully on-chain auction lasting for [144 + 3](../../faq/what-is-144-+-3-blocks-ordinals-auction.md) blocks. The highest bid wins, and you will receive the funds after repaying the loan. This mechanism is particularly important for grail ordinals, as they won’t be liquidated at the floor price, unlike in peer-to-peer lending services.&#x20;

### Example

1. Alice purchased a grail ordinal for 0.3 BTC when the floor price was 0.2 BTC.
2. She borrowed 0.1 BTC from Bitty, using a 50% loan-to-value (LTV) based on the floor price.
3. Unfortunately, Alice was unable to repay the loan and was liquidated.
4. After the auction concluded, the winning bid for her grail ordinal was 0.27 BTC. After repaying her loan, Alice received 0.27 BTC - 0.1 BTC = 0.17 BTC back.&#x20;

This is a scenario she would not have experienced had she used a peer-to-peer service.
