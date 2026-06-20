<div align="center">

# AgroVest

### Empowering African Agriculture Through Blockchain Investment & Commerce

[![Website](https://img.shields.io/badge/🌐_Website-Coming_Soon-00C853?style=for-the-badge&logo=googlechrome&logoColor=white)]()
[![Twitter](https://img.shields.io/badge/🐦_Twitter-@AgroVest-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)]()
[![Discord](https://img.shields.io/badge/💬_Discord-Join_Us-5865F2?style=for-the-badge&logo=discord&logoColor=white)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

---

**Unlocking the $65 billion potential of African agriculture** through trust, transparency, and accessibility of blockchain technology.

</div>

---

## 🌍 The Problem

African agriculture employs over **60% of the continent's workforce**, yet farmers face systemic barriers:

- **No access to capital** — less than 3% of commercial lending goes to agriculture
- **No market access** — middlemen capture 40–60% of final prices
- **No proof of ownership** — land tenure disputes block loans and insurance
- **Zero supply chain transparency** — no way to verify product origin or practices

## 💡 The Solution

AgroVest is a **blockchain-powered platform** on Stellar Soroban that connects African farmers directly with global investors and consumers through four integrated pillars:

```
 ┌─────────────────────────────────────────────────────────────────┐
 │                       AgroVest Platform                         │
 ├────────────────┬────────────────┬────────────────┬──────────────┤
 │  🌾 Farm       │  💰 Investment │  🔒 Escrow     │  🗳️ DAO      │
 │  Marketplace   │  Platform      │  Protection    │  Governance  │
 │                │                │                │              │
 │ • Farm reg.    │ • Campaigns    │ • Hold funds   │ • Proposals  │
 │ • Products     │ • Invest XFI   │ • Delivery     │ • Voting     │
 │ • Cart         │ • Time-locks   │ • Disputes     │ • Delegation │
 │ • Reviews      │ • Claim        │ • Resolution   │ • Challenges │
 └────────────────┴────────────────┴────────────────┴──────────────┘
                            │
           ┌────────────────┴────────────────┐
           │   Stellar Soroban Smart Contracts │
           │     (Rust · WASM · Low Fees)      │
           └──────────────────────────────────┘
```

---

## 📦 Repositories

| Repository | Description | Language | Status |
|:-----------|:------------|:--------:|:------:|
| [`AgroVest-Contract`](https://github.com/AgroVestOfficial/AgroVest-Contract) | Stellar Soroban smart contracts — Farm, Investment, Escrow, DAO | **Rust** | ✅ Testnet |
| [`AgroVest-Backend`](https://github.com/AgroVestOfficial/AgroVest-Backend) | REST API server — Axum, PostgreSQL, Redis, JWT auth | **Rust** | ✅ Testnet |
| [`AgroVest-Frontend`](https://github.com/AgroVestOfficial/AgroVest-Frontend) | Web app — Next.js 14, TypeScript, Tailwind, Stellar SDK | **TypeScript** | ✅ Testnet |

---

## 🏗️ Architecture

```
┌──────────────────────────────────────────────────────────┐
│                     CLIENT LAYER                          │
│  Next.js 14 · TypeScript · Tailwind · shadcn/ui          │
│  Stellar SDK · Freighter Wallet · Pinata IPFS             │
├──────────────────────────────────────────────────────────┤
│                    BACKEND LAYER                           │
│  Axum 0.7 · PostgreSQL 16 · Redis 7                      │
│  JWT Auth (Ed25519) · Event Indexer                       │
├──────────────────────────────────────────────────────────┤
│                   BLOCKCHAIN LAYER                        │
│  Stellar Soroban · 4 Contracts (Rust/WASM)               │
│  AVT Token (Stellar Asset Contract)                       │
└──────────────────────────────────────────────────────────┘
```

**Data Flow:**
- **Writes** → Frontend → Wallet (signs tx) → Soroban contracts (on-chain state)
- **Reads** → Frontend → Backend API → PostgreSQL (indexed from chain events)
- **Files** → Frontend → Pinata IPFS → CID stored on-chain & in DB

---

## ✨ Key Features

| Feature | Description |
|:--------|:------------|
| 🌾 **Farm Marketplace** | Farmers list and sell agricultural products directly — no middlemen |
| 💰 **Farm Investment** | Anyone worldwide can invest in farm operations with time-locked funding |
| 🔒 **Escrow Protection** | Every transaction protected by smart contract escrow with dispute resolution |
| 🗳️ **DAO Governance** | Token holders vote on platform decisions with anti-whale weighting |
| 🔐 **Wallet Abstraction** | Email, social login, or crypto wallet via Freighter |
| 📸 **IPFS Storage** | Decentralized image hosting via Pinata |
| ⚡ **Low Fees** | Stellar's ~$0.00001 per transaction |
| 🌍 **African-First** | Built for the continent's 33M+ smallholder farmers |

---

## 🚀 Getting Started

Each repository is independent — see its own README for setup instructions.

### Smart Contracts
```bash
git clone https://github.com/AgroVestOfficial/AgroVest-Contract.git
cd AgroVest-Contract
soroban contract build    # Build all 4 contracts
cargo test --workspace    # Run 22 tests
```

### Backend
```bash
git clone https://github.com/AgroVestOfficial/AgroVest-Backend.git
cd AgroVest-Backend
docker-compose up -d postgres redis
cp .env.example .env
cargo run                  # Starts on :8080
```

### Frontend
```bash
git clone https://github.com/AgroVestOfficial/AgroVest-Frontend.git
cd AgroVest-Frontend
npm install
cp .env.example .env.local
npm run dev                # Starts on :3000
```

---

## 📊 By the Numbers

<div align="center">

| Metric | Value |
|:-------|:-----:|
| Smart Contracts | **4** |
| Contract Tests | **22** |
| Backend API Endpoints | **30+** |
| Database Tables | **13** |
| Transaction Fees | **~$0.00001** |
| Target Market | **$65B** |

</div>

---

## 🛠️ Tech Stack

<div align="center">

![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white)
![Stellar](https://img.shields.io/badge/Stellar-08B5E5?style=for-the-badge&logo=stellar&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)

</div>

---

## 📅 Roadmap

- [x] 4 smart contracts deployed on testnet
- [x] Full-stack application (Frontend + Backend)
- [x] Wallet integration with Freighter
- [x] IPFS image storage via Pinata
- [x] 22 contract tests with CI/CD
- [ ] Smart contract audit & mainnet deployment
- [ ] Insurance for farmers and investors
- [ ] Supply chain tracking (farm-to-table)
- [ ] Account abstraction (gasless transactions)
- [ ] Mobile app (React Native)
- [ ] Multi-chain expansion

---

## 🤝 Contributing

We welcome contributions! Please read our contributing guidelines before submitting a PR.

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">


*Every African farmer deserves access to global capital, fair markets, and transparent commerce.*

</div>
