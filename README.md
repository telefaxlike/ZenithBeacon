# ZenithBeacon

Built for Base

ZenithBeacon is a Base-aligned repository created to provide a clear and repeatable signal of Base network health, wallet connectivity, and RPC correctness using official Coinbase tooling.

Rather than focusing on application logic, the repository acts as a technical checkpoint for Base environments.

## Purpose

ZenithBeacon helps validate:
- Base Mainnet and Base Sepolia availability
- Wallet onboarding flows via OnchainKit
- RPC accuracy for chainId, blocks, and balances
- Explorer alignment through Basescan references

## Supported Networks

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  
RPC: https://mainnet.base.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  
RPC: https://sepolia.base.org  

## Application Overview

Primary file: app/zenithBeacon.ts

The application:
- Initializes an OnchainKitProvider for the selected Base network
- Renders wallet connection UI
- Uses Viem for read-only Base RPC calls:
  - chainId
  - latest block number
  - native ETH balance
- Exposes Basescan explorer links for verification

## Repository Structure

app/  
- zenithBeacon.ts  
  React entry component combining wallet UX and Base JSON-RPC reads.

Expected companion files:
- package.json
- tsconfig.json
- index.html / main.tsx
- .env (optional)

## Tooling

OnchainKit  
https://github.com/coinbase/onchainkit  

Viem  
EVM client for Base JSON-RPC reads

## Installation and Usage

Requirements:
- Node.js 18+
- Browser environment with wallet support

Install dependencies using your preferred package manager and run the project with a standard React/Vite or Next.js development server.

Optional environment variables:
- VITE_BASE_RPC_URL
- VITE_BASE_SEPOLIA_RPC_URL

## Base Mainnet Deployment

Deployed on Base Mainnet

Network: Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Deployed contract address:  
your_adress  

Basescan deployment and verification links:
- https://basescan.org/address/your_adress  
- https://basescan.org/address/your_adress#code  

## License

MIT License

## Author

GitHub: https://github.com/telefaxlike
Public contact (email): likely.telefax.0k@icloud.com  
Public contact (X): https://x.com/markizdesaaad  

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract "control" address:  
0xc6749c4d2f826a8f61e2f95cdb96314d6ff13a77  

Deployment and verification:
- https://sepolia.basescan.org/address/0xc6749c4d2f826a8f61e2f95cdb96314d6ff13a77  
- https://sepolia.basescan.org/0xc6749c4d2f826a8f61e2f95cdb96314d6ff13a77/0#code  

Contract "array" address:  
0x71f25929a0ad761482e93c501003588b51ba9552  

Deployment and verification:
- https://sepolia.basescan.org/address/0x71f25929a0ad761482e93c501003588b51ba9552  
- https://sepolia.basescan.org/0x71f25929a0ad761482e93c501003588b51ba9552/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
