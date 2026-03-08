# 📚 Blockchain Learning Notes

Personal documentation of my Web3 & Blockchain learning journey from fundamentals to smart contract development.

---

## 🗂️ Table of Contents

- [What is Blockchain?](#what-is-blockchain)
- [How Ethereum Works](#how-ethereum-works)
- [What is a Smart Contract?](#what-is-a-smart-contract)
- [Solidity Basics](#solidity-basics)
- [Web3 Key Concepts](#web3-key-concepts)
- [Tools I Use](#tools-i-use)
- [Resources](#resources)

---

## 🔗 What is Blockchain?

A **blockchain** is a distributed ledger a database that is shared and synchronized across many computers.

Key properties:
- **Decentralized** — No single authority controls it
- **Immutable** — Data cannot be altered once written
- **Transparent** — Anyone can verify transactions
- **Trustless** — No need to trust a third party

> Think of it like a Google Sheet that everyone can read, but nobody can delete or edit past rows.

---

## ⟠ How Ethereum Works

Ethereum is a programmable blockchain. Unlike Bitcoin (which only handles transactions), Ethereum lets developers deploy **smart contracts**.

| Component | Description |
|-----------|-------------|
| **ETH** | Native currency used to pay for transactions (gas) |
| **Gas** | Fee paid to miners/validators to process transactions |
| **Wallet** | Software that holds your private key (e.g. MetaMask) |
| **EVM** | Ethereum Virtual Machine — runs smart contract code |
| **Node** | A computer that stores and validates the blockchain |

---

## 📜 What is a Smart Contract?

A smart contract is **self-executing code** stored on the blockchain. Once deployed, it runs automatically when conditions are met — no middleman needed.

Example use cases:
- Sending tokens automatically when payment is received
- Minting an NFT when someone pays a price
- Locking funds until a certain date

```solidity
// Simple example: store and retrieve a number
pragma solidity ^0.8.0;

contract SimpleStorage {
    uint256 public storedNumber;

    function store(uint256 _number) public {
        storedNumber = _number;
    }

    function retrieve() public view returns (uint256) {
        return storedNumber;
    }
}
```

---

## 🧱 Solidity Basics

Solidity is the programming language for Ethereum smart contracts.

### Data Types
```solidity
uint256 number = 100;       // unsigned integer
int256 temp = -5;           // signed integer
bool isActive = true;       // boolean
address wallet = 0x123...; // Ethereum address
string name = "Roseanne";  // string
bytes32 hash;               // fixed-size bytes
```

### Functions
```solidity
// public = anyone can call
// view = doesn't change state (free to call)
// pure = doesn't read or change state

function add(uint a, uint b) public pure returns (uint) {
    return a + b;
}
```

### Mappings (like a dictionary/hashmap)
```solidity
mapping(address => uint256) public balances;
balances[msg.sender] = 1000;
```

### Events (logging to blockchain)
```solidity
event Transfer(address indexed from, address indexed to, uint256 value);
emit Transfer(msg.sender, recipient, amount);
```

---

## 🌐 Web3 Key Concepts

| Term | Meaning |
|------|---------|
| **DApp** | Decentralized Application (frontend + smart contract) |
| **DeFi** | Decentralized Finance — banking without banks |
| **NFT** | Non-Fungible Token — unique digital ownership proof |
| **DAO** | Decentralized Autonomous Organization |
| **ERC-20** | Token standard (fungible, like currencies) |
| **ERC-721** | NFT standard (non-fungible, each is unique) |
| **ABI** | Application Binary Interface — tells frontend how to call contracts |
| **Testnet** | Fake blockchain for testing (no real money) |
| **Mainnet** | Real blockchain with real value |
| **IPFS** | Decentralized file storage often used for NFT metadata |

---

## 🛠️ Tools I Use

| Tool | Purpose | Link |
|------|---------|------|
| Remix IDE | Write & deploy Solidity in browser | [remix.ethereum.org](https://remix.ethereum.org) |
| MetaMask | Browser wallet | [metamask.io](https://metamask.io) |
| Hardhat | Local dev environment | [hardhat.org](https://hardhat.org) |
| OpenZeppelin | Audited contract templates | [openzeppelin.com](https://openzeppelin.com) |
| Etherscan | Blockchain explorer | [etherscan.io](https://etherscan.io) |
| Alchemy | Node provider (RPC) | [alchemy.com](https://alchemy.com) |
| CryptoZombies | Learn Solidity by game | [cryptozombies.io](https://cryptozombies.io) |

---

## 📖 Resources

**Free Courses:**
- [CryptoZombies](https://cryptozombies.io) — Solidity for beginners via game
- [Alchemy University](https://university.alchemy.com) — Full Web3 bootcamp (free)
- [Patrick Collins - Solidity Course](https://www.youtube.com/watch?v=gyMwXuJrbJQ) — 32hr YouTube course

**Documentation:**
- [Solidity Docs](https://docs.soliditylang.org)
- [Ethereum Docs](https://ethereum.org/en/developers/docs/)
- [OpenZeppelin Docs](https://docs.openzeppelin.com)

---

## 📅 My Learning Progress

- [x] Understand what blockchain is
- [x] Learn how Ethereum and EVM work
- [x] Understand smart contracts
- [x] Learn Solidity fundamentals
- [ ] Deploy first contract on testnet
- [ ] Build a DApp frontend
- [ ] Learn DeFi protocols
- [ ] Contribute to an open source Web3 project

---

*This is a living document updated as I learn more. Feel free to fork and use for your own learning!*
