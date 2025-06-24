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
