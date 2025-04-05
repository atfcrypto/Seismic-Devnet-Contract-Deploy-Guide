# Seismic-Devnet-Contract-Deploy-Guide

## 🚀 How to Deploy a Seismic Contract

This guide walks you through setting up your environment and deploying a contract on the Seismic Devnet.

---

## 🧰 Dependencies (for Windows, Linux & VPS)

```bash
sudo apt update && sudo apt install -y build-essential
sudo apt install cargo -y
```

---

## ✅ Pre-Requirements

### 1. Install Rust
```bash
curl https://sh.rustup.rs -sSf | sh
. "$HOME/.cargo/env"
```

#### Verify Installation
```bash
rustc --version
```

### 2. Install jq
- **For WSL/Ubuntu:**
```bash
sudo apt install jq
```
- **For Mac:**
```bash
brew install jq
```

### 3. Install sfoundryup
```bash
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```

### 4. Run sfoundryup
```bash
sfoundryup
```

---

## 🛠️ Deploy an Encrypted Contract 🎶

### 1. Clone Repository
```bash
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

### 2. Deploy Contract
```bash
bash script/deploy.sh
```
> 📌 This script will generate a wallet and prompt a Faucet URL along with the wallet address. Use the faucet to fund your wallet. ✅

---

## 🤖 Interact with the Encrypted Contract

### 1. Navigate to Home Directory
```bash
cd $HOME
```

### 2. Install Bun
```bash
curl -fsSL https://bun.sh/install | bash
```

### 3. Install Node Dependencies
```bash
cd try-devnet/packages/cli/
bun install
```

### 4. Send Transactions
```bash
bash script/transact.sh
```

✅ Done! You’ve successfully deployed and interacted with a Seismic Devnet contract!

