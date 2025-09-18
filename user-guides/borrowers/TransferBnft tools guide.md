TransferBnft tools guide
---

The lending bound-nft is non-transferable. However, in some special cases, you can contact the official team to transfer bnft using the transfer bnft tool.

1. Authorize NFT

   1. Identify the NFT that needs to be transferred, click on the NFT link (for example, if the loan borrowed against BAYC, click on the BAYC address). The browser will open the NFT contract on Etherscan

   | NFT      | address                                                      |
   | -------- | ------------------------------------------------------------ |
   | BAYC     | [0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D](https://etherscan.io/address/0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D) |
   | PUNK     | [0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6](https://etherscan.io/address/0xb7F7F6C52F2e2fdb1963Eab30438024864c313F6) |
   | MAYC     | [0x60e4d786628fea6478f785a6d7e704777c86a7c6](https://etherscan.io/address/0x60e4d786628fea6478f785a6d7e704777c86a7c6) |
   | AZUKI    | [0xed5af388653567af2f388e6224dc7c4b3241c544](https://etherscan.io/address/0xed5af388653567af2f388e6224dc7c4b3241c544) |
   | MEEBITS  | [0x7bd29408f11d2bfc23c34f18275bbf23bb716bc7](https://etherscan.io/address/0x7bd29408f11d2bfc23c34f18275bbf23bb716bc7) |
   | MIL      | [0x5af0d9827e0c53e4799bb226655a1de152a425a5](https://etherscan.io/address/0x5af0d9827e0c53e4799bb226655a1de152a425a5) |
   | PUDGY    | [0xbd3531da5cf5857e7cfaa92426877b022e612cf8](https://etherscan.io/address/0xbd3531da5cf5857e7cfaa92426877b022e612cf8) |
   | MFER     | [0x79fcdef22feed20eddacbb2587640e45491b757f](https://etherscan.io/address/0x79fcdef22feed20eddacbb2587640e45491b757f) |
   | LILP     | [0x524cab2ec69124574082676e6f654a18df49a048](https://etherscan.io/address/0x524cab2ec69124574082676e6f654a18df49a048) |
   | MOONBIRD | [0x23581767a106ae21c074b2276D25e5C3e136a68b](https://etherscan.io/address/0x23581767a106ae21c074b2276D25e5C3e136a68b) |
   | MoonCats | [0xc3f733ca98E0daD0386979Eb96fb1722A1A05E69](https://etherscan.io/address/0xc3f733ca98E0daD0386979Eb96fb1722A1A05E69) |
   | DOODLE   | [0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e](https://etherscan.io/address/0x8a90CAb2b38dba80c64b7734e58Ee1dB38B8992e) |
   | MYTHICS  | [0xC0FFee8FF7e5497C2d6F7684859709225Fcc5Be8](https://etherscan.io/address/0xC0FFee8FF7e5497C2d6F7684859709225Fcc5Be8) |

   2. Click Contract -> Write Contract (or Write as Proxy) -> setApprovalForAll, as shown in the figure below
      ![3a752932-4e86-4a60-8b33-29c9478be8ff](/imgs/3a752932-4e86-4a60-8b33-29c9478be8ff.png)
   
   
   
   3. Fill in the parameters
      ```
      operator: 0xF7b9F724E2255820316B9c0c1075aff08C038C1b
      approved: true
      ```
   
   4. Wallet switch to the **original address own the nft to be transferred** (hereinafter referred to as the **original address**), click "Connect to Web3" to connect the wallet plugin, and finally click "Write", sign and send the transaction, as indicated by the red arrow in the above figure.
   
2. Authorize debt Weth:

   1. Click [link](https://etherscan.io/address/0xa94CCAa71214338E86b9a9B6Ab1F8D71c6167d65)：

      Click Contract -> Write as Proxy -> approveDelegation
      ![34772418-a36d-4877-a6ce-9543280a0e14](/imgs/34772418-a36d-4877-a6ce-9543280a0e14.png)
   
   2. Fill in the parameters
   
      ```
      delegatee: 0xF7b9F724E2255820316B9c0c1075aff08C038C1b
      amount: 115792089237316195423570985008687907853269984665640564039457584007913129639935
      ```
   
   3. Wallet switch to the **new address that will receive the nft** (hereinafter referred to as the **new address**), and finally click "Write", click "Connect to Web3" to connect the wallet plugin,, sign and send the transaction.
   
3. Start the transfer

   1. Click [link](https://etherscan.io/address/0xF7b9F724E2255820316B9c0c1075aff08C038C1b)：
      Click Contract -> Write as Proxy -> transfer
      ![d698fc7f-f1c4-4502-bfb1-79d10fe244e7](/imgs/d698fc7f-f1c4-4502-bfb1-79d10fe244e7.png)
   
   2. Fill in the parameters:
   
      ```typescript
      nft: the NFT to be transferred
      tokenIds: the tokenId of the NFT to be transferred
      to: new address
      ```
   
   3. Wallet switch to the **original address**, click "Connect to Web3" to connect the wallet,  and finally click "Write", sign and send the transaction.
   
4. After the transfer
   It is recommended to revoke the authorizations in Steps 1 and 2 above.
   
   1. setApprovalForAll
      ```
      operator: 0xF7b9F724E2255820316B9c0c1075aff08C038C1b
      approved: false
      ```
   
   2. approveDelegation
   
      ```
      delegatee: 0xF7b9F724E2255820316B9c0c1075aff08C038C1b
      amount: 0
      ```
   
      
