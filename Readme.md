# USDC Approval via Solana Wallet on Neon EVM (Devnet)

This script demonstrates how to use a Solana wallet to schedule a USDC `approve()` transaction on Neon EVM Devnet.  
It uses the `@neonevm/solana-sign` SDK to bridge Solana and Ethereum-compatible smart contract calls.

---

## ✨ Features

- Connects to Solana Devnet and Neon EVM Devnet
- Loads Solana wallet from Base58 private key
- Uses Ethers.js to interact with the USDC contract
- Sends a scheduled `approve()` transaction on Neon
- Checks USDC allowance before and after the transaction

---

## 📦 Installation

```bash
git clone https://github.com/MojeedFetuga/usdc-approval-on-neon-from-solana.git
cd usdc-approval-on-neon-from-solana
npm install


# ✅ USDC Approval on Neon EVM from Solana Wallet

This script demonstrates how to schedule a `USDC.approve()` transaction on **Neon EVM Devnet** using a **Solana wallet**. It leverages the [@neonevm/solana-sign](https://www.npmjs.com/package/@neonevm/solana-sign) SDK to sign and schedule transactions that interact with Ethereum-based contracts via the Neon EVM.

---

## 🔧 Prerequisites

- Node.js `v18+` or `v20+`
- A funded Solana wallet on Devnet
- `.env` file with your Base58 private key

---

## 📁 Folder Setup

```bash
git clone https://github.com/MojeedFetuga/usdc-approval-on-neon-from-solana.git
cd usdc-approval-on-neon-from-solana
npm install
Create a .env file and add:
PRIVATE_KEY_SOLANA=your_base58_private_key

🚀 Usage
Run the approval script:

npm start
✅ What Happens
Check Existing Allowance
The script fetches the current allowance from the Neon EVM Devnet:

Current USDC approval of 0x4e91835921a6a99e318fefa39b300d7ca318fa21 is 1750787869n

Schedule a USDC Approval Transaction
The script builds a transaction to approve 0x4e918359... to spend tokens and schedules it:

Scheduled transaction signature:
3FjKDDoLfMHsdkQkCNX4HyKggFsaNTVW69VaXnu7523B35P7ma4LuZbp3bAMBe9vwKLNxkPHq3iKjqePLv1y45yJ

Broadcast to Neon EVM Devnet
After submitting the scheduled transaction, the Neon EVM transaction hash is returned:

Neon EVM transaction hash:
0xb15ae8ef92da808757b1b98ff23bedb89b62773dd8cd90827a93d181f9f96ffc
View on Explorer (if available)
You can search the transaction hash on a Neon Devnet block explorer (if public).

