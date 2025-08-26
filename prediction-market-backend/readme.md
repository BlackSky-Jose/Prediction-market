# Prediction Market Backend

This is the backend service for a prediction market application. It is built using Node.js, TypeScript, Express, and MongoDB. The backend interacts with the Solana blockchain to manage prediction markets, handle liquidity, and process bets.

## Features

- **Prediction Market Management**: Create and manage prediction markets.
- **Liquidity Management**: Add liquidity to markets.
- **Betting**: Place bets on prediction outcomes.
- **Blockchain Integration**: Interacts with the Solana blockchain using Anchor and SPL Token libraries.
- **MongoDB Integration**: Stores market and user data in MongoDB.
- **MongoDB Integration**: Oracle Inegration for custom feed registeration and fetch result

---

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/HyperBuildX/Solana-Prediction-Market.git
    cd Prediciton-market-backend
    ```
2. Install module and run:
    ```bash
    yarn && yarn dev
    ```
