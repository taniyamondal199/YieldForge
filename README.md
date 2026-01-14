# YieldForge
YieldForge is a DeFi-native protocol on Mantle that converts real-world asset cash flows into composable yield tokens. Using ERC-4626 vaults, it splits deposits into Principal and Yield tokens, enabling tradable yield with privacy-preserving compliance via ZK-KYC and oracle-driven updates.
## 🚨 Problem

Real-world assets like treasury bills, invoices, and rental income generate stable yield, but:

- Access is permissioned and centralized
- Yield is locked and non-composable
- Compliance relies on surveillance and wallet whitelists
- DeFi protocols cannot easily integrate real-world yield

As a result, RWAs fail to behave like true DeFi primitives.
## 💡 Solution

YieldForge turns verified real-world cash flows into **DeFi-native yield tokens**.
### Key Innovations:
- Real-world assets are represented as **Asset NFTs**
- Assets back **ERC-4626 yield vaults**
- Deposits mint:
  - **Principal Tokens (PT)** — representing deposited capital
  - **Yield Tokens (YT)** — representing future yield
- Access control is enforced via **ZK-KYC proofs**
- **Chainlink oracles** provide pricing, yield updates, and reserve proofs

YieldForge is deployed on **Mantle** to leverage low fees, EVM compatibility, and high throughput for RWA settlement.
## 🏗 Architecture Overview
User Wallet (MetaMask)
|
v
YieldVault (ERC-4626)
/
PrincipalToken YieldToken
|
v
AssetNFT (RWA Anchor)
|
v
Chainlink Oracle + ZK-KYC Verifier
## 🔐 Compliance (ZK-KYC)

Instead of whitelisting wallets, YieldForge uses a **ZK-KYC verifier interface**.

- Users prove eligibility without revealing identity
- Smart contracts verify proofs, not personal data
- In this MVP, ZK verification is mocked to demonstrate the architecture
## 🔗 Chainlink Integration

Chainlink oracles are used to:
- Update yield rates
- Verify asset value
- Signal maturity or default events

In the hackathon MVP, oracle data is simulated via mock feeds.
## 🧪 Hackathon MVP Scope

✅ Implemented:
- Asset NFT contract
- ERC-4626 Yield Vault
- Principal Token (PT)
- Yield Token (YT)
- Mock ZK-KYC verifier
- Mock Chainlink oracle
- MetaMask wallet integration
- Deployment on Mantle testnet

🚧 Simulated:
- Real-world asset data
- Legal KYC verification
- Live oracle feeds
## 🚀 Why Mantle

- Low transaction fees enable scalable RWA yield
- Modular Ethereum stack supports complex infra
- Ideal settlement layer for RealFi applications
- Strong alignment with Mantle ecosystem vision
## 🛣 Roadmap

**Phase 1 (Hackathon MVP)**
- Single asset type (mock treasury/invoice)
- Yield tokenization
- ZK-KYC interface
- Mantle testnet deployment

**Phase 2**
- Multiple asset types
- Risk tranching (senior / junior)
- Live Chainlink oracles
- DEX liquidity for Yield Tokens

**Phase 3**
- DAO-curated asset marketplace
- On-chain credit scoring
- Institutional privacy pools
- Cross-chain yield routing
## 🏁 Vision

Make real-world yield as programmable, private, and composable as DeFi itself.
## ⚙️ Deployment Instructions

### Prerequisites
- Node.js (v18+)
- MetaMask wallet
- Mantle Testnet RPC
- Test ETH on Mantle Testnet
1️⃣ Clone the Repository

git clone https://github.com/taniyamondal199/yieldforge.git
cd yieldforge
2️⃣ Install Dependencies

npm install
4️⃣ Compile Contracts

npx hardhat compile
5️⃣ Deploy to Mantle Testnet

npx hardhat run scripts/deploy.js --network mantleTestnet
Deployment outputs:

AssetNFT address 

YieldVault address

PT and YT token addresses

🚀 Launch Status: ACTIVE

Frontend: Running on port 3000 ✅
Backend: Running on port 4000 ✅
Browser: Multiple tabs already open at http://localhost:3000/vaults ✅
Access URLs

Local: http://localhost:3000
Network: http://169.254.191.127:3000 (for devices on same Wi-Fi)
Public Tunnel: Check the localtunnel window for your public URL







