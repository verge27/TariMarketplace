
# Tari Marketplace MVP

This is a minimal viable product (MVP) for a decentralized marketplace built on the Tari network. It mimics the core functionality of platforms like Etsy, but for digital assets represented as Tari Digital Assets (TDAs) and transacted in XTR.

## 📦 Project Structure

```
tari-marketplace-mvp/
├── smart_contract/            # Rust smart contract using Tari DAN Template
│   └── marketplace_template.rs
├── indexing_service/          # Rust backend with PostgreSQL for indexing and API
│   ├── Cargo.toml
│   └── src/
│       └── main.rs
├── frontend/                  # React web frontend
│   ├── package.json
│   └── src/
│       ├── App.js
│       └── App.css
```

---

## 🚀 Features

### 🧠 Smart Contract (Rust)
- Listing creation, purchase, cancellation
- Atomic TDA transfers
- Platform fee support
- Events for indexer

### 🌐 Frontend (React)
- Wallet connection (mocked)
- Browse listings
- Create listing
- View listing details
- Purchase flow

### 🗂️ Indexing Service (Rust + PostgreSQL)
- Listens to Tari DAN events (simulated)
- Stores listing data
- Serves JSON API via Warp

---

## 🛠️ Setup Instructions

### 1. Smart Contract
> Build and deploy to Tari Layer 2 (DAN)

Requires:
- Tari template SDK
- Rust toolchain

```
cd smart_contract
# Build & deploy instructions based on Tari SDK documentation
```

### 2. Indexing Service
> Rust backend with PostgreSQL

#### Requirements
- Rust
- PostgreSQL

#### Setup

```bash
cd indexing_service
cargo run
```

### 3. Frontend

#### Requirements
- Node.js + npm

#### Setup

```bash
cd frontend
npm install
npm start
```

---

## 🧪 Mock Components
- Wallet: Uses `mockWallet` for demo
- Event Listener: Polling stub for future Tari DAN integration

---

## 📌 Limitations (MVP Scope)
- Digital assets only (TDAs)
- No minting (assumed external)
- No advanced search/filtering
- XTR only, fixed price sales
- No physical goods support
- Centralized read indexing

---

## 🛣️ Future Work
- Real wallet integration (Aurora, Tari.js)
- Decentralized metadata via IPFS
- Event-driven backend from Tari nodes
- Auctions, reviews, categories

---

## ⚡ Built With
- [Tari DAN](https://www.tari.com/)
- Rust, React, PostgreSQL, Warp

---

## License
MIT
