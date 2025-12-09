#  DecentraPredict - A Decentralized Prediction Market

**A fully decentralized prediction market platform on Solana enabling users to create custom markets, add liquidity, place token-based bets, and automatically resolve outcomes using Switchboard oracles and Anchor smart contracts.**

DecentraPredict is an open-source decentralized prediction market built on Solana, allowing users to create, participate, add liquidity, and resolve prediction events using smart contracts.

>  Bet on real-world outcomes. Earn if you're right. Built for transparency, fairness, and community governance.

---

## Features

- **Create Custom Markets** – Users can create prediction markets with custom questions and outcomes
- **Add Liquidity** – Fund markets to increase liquidity and enable betting
- **Token-Based Betting** – Place bets on "Yes" or "No" outcomes using dynamic token pricing
- **Decentralized Smart Contracts** – Trustless and transparent market resolution on Solana
- **Oracle Integration** – Automatic result fetching using Switchboard oracles
- **Referral System** – Earn rewards through referral links
- **User Profiles** – Track your betting history and market participation
- **Real-time Market Data** – View active, pending, and resolved markets

---

## How it works

You can reference the guide video here:

https://github.com/user-attachments/assets/8f48a641-7edb-4af3-a17e-c5464bfef660

---##  Tech Stack

- **Blockchain**: Solana (Devnet/Mainnet)
- **Smart Contracts**: Anchor Framework 0.29.0 / Rust
- **Frontend**: Next.js 15.2.1 + React 19 + TailwindCSS 4.0
- **Backend**: Node.js + Express 5 + TypeScript
- **Database**: MongoDB
- **Oracles**: Switchboard
- **Wallet Integration**: Solana Wallet Adapter (Phantom)

---

##  Project Structure

```
Prediction-Market/
├── BackEnd/                 # Backend API server
│   ├── src/
│   │   ├── controller/      # Business logic controllers
│   │   ├── router/          # API routes
│   │   ├── model/           # MongoDB models
│   │   ├── prediction_market_sdk/  # Solana SDK integration
│   │   └── oracle_service/  # Oracle feed management
│   └── package.json
├── FrontEnd/                # Next.js frontend application
│   ├── src/
│   │   ├── app/             # Next.js app router pages
│   │   ├── components/      # React components
│   │   ├── providers/       # Context providers
│   │   └── utils/           # Utility functions
│   └── package.json
└── prediction-market-smartcontract/  # Anchor smart contract
    ├── programs/
    │   └── prediction/      # Rust program source
    └── tests/               # Contract tests
```

---

##  Getting Started

### Prerequisites

- **Node.js** v18 or higher
- **Anchor** 0.29.0
- **Solana CLI** (latest stable version)
- **MongoDB** (local or MongoDB Atlas)
- **Yarn** or **npm** package manager
- **Rust** (for smart contract development)

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/BlackSky-Jose/Prediction-market.git
cd Prediction-market-SOLANA
```

#### 2. Install Backend Dependencies

```bash
cd BackEnd
npm install
# or
yarn install
```

#### 3. Install Frontend Dependencies

```bash
cd ../FrontEnd
npm install
# or
yarn install
```

#### 4. Install Smart Contract Dependencies

```bash
cd ../prediction-market-smartcontract
npm install
# or
yarn install
```

---

## ⚙️ Configuration

### Backend Environment Variables

Create a `.env` file in the `BackEnd` directory:

```env
PORT=9000
DB_URL=your_mongodb_connection_string
PASSKEY=your_passkey
FEE_AUTHORITY=your_fee_authority_public_key
```

You can copy from the example file:
```bash
cd BackEnd
cp env.example .env
# Then edit .env with your actual values
```

### Frontend Configuration

The frontend is configured to connect to Solana Devnet by default. You can modify the RPC endpoint in `FrontEnd/src/app/layout.tsx` if needed.

### Smart Contract Configuration

The smart contract is configured for Solana Devnet. Check `prediction-market-smartcontract/Anchor.toml` for configuration details.

---

##  Running the Application

### Backend Server

```bash
cd BackEnd

# Development mode (with hot reload)
npm run dev
# or
yarn dev

# Production mode
npm start
# or
yarn start
```

The backend server will run on `http://localhost:9000` (or the port specified in your `.env` file).

### Frontend Application

```bash
cd FrontEnd

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

The frontend will be available at `http://localhost:3000`.

### Smart Contract

```bash
cd prediction-market-smartcontract

# Build the contract
anchor build

# Deploy to devnet
anchor deploy

# Run tests
anchor test
```

---

##  API Endpoints

The backend provides the following API endpoints (all prefixed with `/api`):

### Market Endpoints
- `POST /api/market/create` - Create a new prediction market
- `POST /api/market/add` - Add additional market information
- `POST /api/market/addLiquidity` - Add liquidity to a market
- `POST /api/market/betting` - Place a bet on a market
- `POST /api/market/liquidity` - Alternative liquidity endpoint
- `GET /api/market/get` - Get market data

### Oracle Endpoints
- `POST /api/oracle/registFeed` - Register a custom oracle feed

### Referral Endpoints
- `POST /api/referral/` - Get or generate referral code
- `POST /api/referral/claim` - Claim referral rewards

### Profile Endpoints
- `GET /api/profile/` - Get user profile data

---

##  How It Works

1. **Create Market** – A user creates a prediction event with a question (e.g., "Will BTC hit $80k by Dec 2025?")
2. **Add Liquidity** – Users can fund markets to increase liquidity. Once a threshold is reached, betting becomes active.
3. **Participants Bet** – Users place stakes on "Yes" or "No" outcomes by purchasing tokens. Token prices fluctuate based on market probability.
4. **Locking Period** – Market closes at deadline; no more bets are accepted.
5. **Resolution** – Oracle fetches real-world outcome automatically from Switchboard feeds.
6. **Payout** – Winners are rewarded proportionally based on their token holdings.

### Market States

- **Pending** – Market created but liquidity threshold not met
- **Active** – Market is open for betting
- **Resolved** – Oracle has determined the outcome, winners can claim rewards

---

##  Development

### Backend Development

The backend uses TypeScript with Express. Key directories:
- `src/controller/` - Business logic
- `src/router/` - API route definitions
- `src/model/` - MongoDB schemas
- `src/prediction_market_sdk/` - Solana blockchain interactions

### Frontend Development

The frontend uses Next.js 15 with the App Router. Key directories:
- `src/app/` - Pages and routes
- `src/components/` - Reusable React components
- `src/providers/` - Context providers for global state

### Smart Contract Development

The smart contract is written in Rust using the Anchor framework:
- `programs/prediction/src/` - Main program logic
- `programs/prediction/src/instructions/` - Individual instruction handlers
- `programs/prediction/src/states/` - Account state definitions

---

##  Testing

### Smart Contract Tests

```bash
cd prediction-market-smartcontract
anchor test
```

### Backend Tests

Currently, backend tests are not configured. You can add test scripts to `BackEnd/package.json`.

---

## License

ISC

---

## Contact

If you have any questions or would like a more customized app for specific use cases, please feel free to contact us:

- **GitHub**: [Prediction-market-SOLANA](https://github.com/BlackSky-Jose/Prediction-market.git)
- **Telegram**: [@blacksky_jose](https://t.me/blacksky_jose)
- **Twitter/X**: [@blacksky_jose](https://x.com/blacksky_jose)

---

## Acknowledgments

Built with:
- [Solana](https://solana.com/)
- [Anchor Framework](https://www.anchor-lang.com/)
- [Next.js](https://nextjs.org/)
- [Switchboard](https://switchboard.xyz/)
