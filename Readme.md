# 🧠 DecentraPredict - A Decentralized Prediction Market

DecentraPredict is an open-source decentralized prediction market built on Solana, allowing users to create, participate, add liquidity and resolve prediction events using smart contracts. 

> ⚖️ Bet on real-world outcomes. Earn if you're right. Built for transparency, fairness, and community governance.

---

## ✨ Features

-  Create custom markets with clear outcomes
-  Add fund to increase liquidity
-  Decentralized and trustless smart contracts
-  Transparent resolution and reward distribution
-  Supports token-based betting and rewards
-  Oracle integration for automatic result fetching
-  Referral link system

---

## 🎞 How it works
You can reference the guide video here:

https://github.com/user-attachments/assets/8f48a641-7edb-4af3-a17e-c5464bfef660

---

## 🏗️ Tech Stack

- **Blockchain**: Solana
- **Smart Contracts**: Anchor / Rust
- **Frontend**: Next.js + TailwindCSS
- **Backend**: Node.js + Express + MongoDB
- **Oracles**: Switchboard

---

## 🚀 Getting Started

### Prerequisites

- Node.js v18+
- Anchor 0.29.0
- Next.js v15.2.1+
- MongoDB Atlas (for backend data)
- Yarn or npm package manager

### Installation

```bash
# Clone the repository
git clone https://github.com/HyperBuildX/Solana-Prediction-Market
cd Solana-Prediction-Market

# Install backend dependencies
cd prediction-market-backend
npm install
# or
yarn install

# Install frontend dependencies
cd ../prediction-market-frontend
npm install
# or
yarn install
```

### Running the Application

#### Backend

```bash
cd prediction-market-backend

# Development mode
npm run dev
# or
yarn dev

# Production mode
npm start
# or
yarn start
```

#### Frontend

```bash
cd prediction-market-frontend

# Development mode
npm run dev
# or
yarn dev

# Production build
npm run build
npm start
# or
yarn build
yarn start
```

### Backend Environment Variables

Create a `.env` file in the `prediction-market-backend` directory:

```env
PORT=9000
DB_URL=your_mongodb_connection_string
PASSKEY=your_passkey
FEE_AUTHORITY=your_fee_authority_public_key
```

## 🧠 How It Works

1. **Create Market** – A user creates a prediction event: e.g., "Will BTC hit $80k by Dec 2025?"
2. **Add Liquidity** – Users can fund any market to increase liquidity
3. **Participants Bet** – Users place stakes on "Yes" or "No" outcomes
4. **Locking Period** – Market closes at deadline; no more bets accepted
5. **Resolution** – Oracle fetches real-world outcome automatically
6. **Payout** – Winners are rewarded proportionally based on their stakes

## 💬 Contact

If you have any questions or would like a more customized app for specific use cases, please feel free to contact us at the contact information below.
- E-Mail: admin@hyperbuildx.com
- Telegram: [@bettyjk_0915](https://t.me/bettyjk_0915)
