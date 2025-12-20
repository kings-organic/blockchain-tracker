# Blockchain Tracker (Built for Base)

Deployed on Base Mainnet.

Blockchain Tracker is a tool that enables wallet connection, Base chain validation, and monitoring blockchain activity, such as block details and address balances, using Coinbase Wallet SDK and Base RPC endpoints.

---

## Base ecosystem alignment

Built for Base.

Supported networks:
- Base Mainnet  
  chainId (decimal): 8453  
  Explorer: https://basescan.org  

- Base Sepolia  
  chainId (decimal): 84532  
  Explorer: https://sepolia.basescan.org  

The application is optimized for Base and interacts with official Base RPC endpoints.

---

## What the script does

The app.blockchain-tracker.ts script provides an in-browser interface that:

1) Connects to Coinbase Wallet using the SDK  
2) Reads and validates the active chainId  
3) Executes read-only Base RPC queries:
   - Latest block number  
   - ETH balance of the connected address  
4) Fetches block details (timestamp, gas usage)  
5) Allows ETH balance checking for any address  
6) Provides Explorer links for verification  

All actions are read-only, no transactions are sent.

---

## Repository structure

- app.blockchain-tracker.ts  
  Main script to connect a wallet, switch networks, and fetch blockchain data.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - contract.sol — minimal contract for deployment and verification  
  - control.sol — stateful contract for interaction  
  - storage.sol — contract for read-only queries  

- package.json  
  Dependency configuration including Coinbase SDKs and Base GitHub repositories.

- README.md  
  Full documentation including setup instructions, usage, and licensing.

---

## Libraries used

- @coinbase/wallet-sdk  
  Coinbase Wallet SDK to facilitate wallet connection.

- viem  
  RPC client used for interacting with Base's blockchain.

- Coinbase GitHub repositories  
  Dependencies referencing Coinbase's open-source ecosystem.

- Base GitHub repositories  
  Dependencies linking to Base-specific tools and infrastructure.

---

## Installation and execution

To set up the project:
1. Install dependencies via Node.js.
2. Run the development server.
3. Open the app in any modern browser.

Expected results:
- Connected wallet address displayed with Basescan link  
- Active chainId shown (8453 or 84532)  
- Blockchain data, including block stats and address balances, displayed  

---

## License

MIT License

Copyright (c) 2025 kings-organic

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED.

---
## Author
Github:https://github.com/kings-organic

Twitter:https://x.com/Christi16204442

Email:kings.organic_00@icloud.com

## Testnet Deployment (Base Sepolia)

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
0xec124430cc96615ae9189217d37180601c284fc5

Deployment and verification:
- https://sepolia.basescan.org/address/0xec124430cc96615ae9189217d37180601c284fc5
- https://sepolia.basescan.org/0xec124430cc96615ae9189217d37180601c284fc5/0#code  

Contract #2 address:  
0xd05a095967055dcb8f1919091bebbdf8328a43da

Deployment and verification:
- https://sepolia.basescan.org/address/0xd05a095967055dcb8f1919091bebbdf8328a43da
- https://sepolia.basescan.org/0xd05a095967055dcb8f1919091bebbdf8328a43da/0#code  

Contract #3 address:  
0xa23f36dadacbc52af5461d94c2831f6001b93084

Deployment and verification:
- https://sepolia.basescan.org/address/0xa23f36dadacbc52af5461d94c2831f6001b93084
- https://sepolia.basescan.org/0xa23f36dadacbc52af5461d94c2831f6001b93084/0#code  
