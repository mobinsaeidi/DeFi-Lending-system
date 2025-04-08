# DeFiLending

A simple DeFi lending protocol built on Ethereum using Solidity. Users can deposit ETH, borrow against their collateral, repay loans with interest, and trigger liquidations if collateral becomes underfunded. Great for learning how decentralized lending protocols work under the hood.

## Features

- Lend and borrow using ETH
- Collateral-based borrowing (150% collateral ratio)
- 5% fixed interest on loans
- Liquidation if collateral falls below 120%
- Modular math library for clean logic
- ReentrancyGuard for safety
- Built for simplicity and clarity

## Project Structure


## Getting Started

### Prerequisites

- Node.js
- Hardhat (or use Remix)
- MetaMask / Wallet setup

### Local Setup (Hardhat)

```bash
git clone https://github.com/yourusername/defi-lending.git
cd defi-lending
npm install
npx hardhat compile
npx hardhat node
npx hardhat run scripts/deploy.js --network localhost
defiLending.deposit{value: 1 ether}();
defiLending.borrow{value: 1.5 ether}(1 ether);
defiLending.repay{value: 1.05 ether}();
defiLending.liquidate(borrowerAddress);

---
