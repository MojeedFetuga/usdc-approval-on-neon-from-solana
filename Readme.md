# 🔄 USDC Approval & Transfer from Solana to Neon EVM

This project demonstrates how to approve and transfer USDC tokens from a Solana native wallet to a Neon EVM-compatible address using the [@neonevm/solana-sign](https://www.npmjs.com/package/@neonevm/solana-sign) SDK and Solana's SPL Token standard.

---

## ✅ Features

- Approve a Solana user's USDC for use on Neon EVM
- Transfer USDC from a Solana ATA to a Neon EVM wallet
- Auto-create associated token accounts and balance accounts if missing
- Interact with Neon EVM's JSON-RPC API
- Includes full transaction flow, gas estimation, and signature logging

---

## 🧰 Tech Stack

- Solana Web3.js
- SPL Token SDK
- Neon EVM Solana Signer SDK
- Node.js + dotenv
- Ethereum's Ethers.js
- JSON-RPC via Curl or Fetch

---

## ⚙️ Setup Instructions

1. **Clone the Repo**

```bash
git clone https://github.com/MojeedFetuga/usdc-approval-on-neon-from-solana.git
cd usdc-approval-on-neon-from-solana
```

2. **Install Dependencies**

```bash
npm install
```

3. **Setup Environment Variables**

Create a `.env` file and add your Solana private key (Base58-encoded):

```env
PRIVATE_KEY_SOLANA=YOUR_BASE58_ENCODED_SECRET_KEY
```

You can find a template in `.env.example`.

4. **Run Approval Script**

```bash
node token-approval-solana-signer-sdk.js
```

---

## ✅ Execution Proof

- USDC Approval Transaction initiated:

  ```
  Scheduled transaction signature: 3FjKDDoLfMHsdkQkCNX4HyKggFsaNTVW69VaXnu7523B35P7ma4LuZbp3bAMBe9vwKLNxkPHq3iKjqePLv1y45yJ
  ```

- Neon EVM TX hash (confirmation):

  ```
  Neon EVM transaction hash: 0xb15ae8ef92da808757b1b98ff23bedb89b62773dd8cd90827a93d181f9f96ffc
  ```

- Curl requests confirmed:
  - `eth_chainId`
  - `neon_getEvmParams`
  - `neon_getNativeTokenList`
  - `eth_getTransactionCount`
  - `eth_maxPriorityFeePerGas`
  - `eth_getBlockByNumber`
  - `neon_estimateScheduledGas`

- ✅ **Token balance verified before and after transfer**
- ✅ **Gas estimate returned and included**
- ✅ **Solana ATA auto-created if missing**
- ✅ **Transaction submitted and processed successfully on Neon Devnet**

---

## 🧪 Transaction Testing (Using Curl)

You can verify Neon EVM status using:

```bash
curl https://devnet.neonevm.org/sol -X POST \
-H 'Content-Type: application/json' \
-d '{{"jsonrpc":"2.0","id":1,"method":"eth_chainId","params":[]}}' | jq .
```

Also use `neon_getTransactionBySenderNonce` to confirm transaction:

```bash
curl https://devnet.neonevm.org/sol -X POST \
-H 'Content-Type: application/json' \
-d '{{"method":"neon_getTransactionBySenderNonce","params":["0xYourNeonWallet", nonce],"id":1,"jsonrpc":"2.0"}}' | jq .
```

---

## 🔒 Security Note

Do **not** commit your private keys. Use `.env` and `.gitignore` wisely.

---

## 📜 License

MIT License
