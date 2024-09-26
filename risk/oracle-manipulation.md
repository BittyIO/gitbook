# Oracle manipulation

We use price data from both centralized exchanges, like Binance, and decentralized platforms, such as MagicEden, for BRC20 tokens, Runes, and Ordinals. Our oracle algorithm remains proprietary, and until a stable oracle service for Bitcoin, like Chainlink, is available, Bitty will maintain the oracle to ensure accountability for our users.

#### Security Considerations on Bitcoin

Due to Bitcoin's average block time of 10 minutes:

* **Attacks to Liquidate Assets**: It is more challenging to attack a lending service by artificially lowering prices to liquidate borrowers’ assets compared to other chains like Ethereum. Attackers must sustain a low price for a longer duration, allowing other buyers to step in and purchase the undervalued assets more easily.
* **Attacks to Inflate Prices**: Similarly, attempting to inflate prices to siphon funds from the lending pool is difficult. Our lending service supports a loan-to-value (LTV) ratio of only 30% to 50%, meaning attackers would need a substantial amount of capital to maintain prices at 200% to 300% higher than normal for the attack to be profitable. Additionally, each asset listed on Bitty has a lending cap, limiting the potential damage from any single asset's attack.

This combination of longer block times and structured lending mechanisms contributes to Bitcoin's security, fostering a sense of safety for users to store value and for us to build on the Bitcoin network.
