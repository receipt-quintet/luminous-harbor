# Luminous Harbor (Built for Base)

Deployed on Base Mainnet.

Luminous Harbor is a lightweight tool designed for validating Base network identity, inspecting public onchain state, and cross-checking data via Basescan.

## Capabilities

- Coinbase Wallet connection via EIP-1193  
- Base chainId validation (8453 / 84532)  
- Network snapshot (block height, timestamp, gas signals)  
- Address probe (ETH balance, nonce, bytecode presence)  
- ERC-20 probe (metadata + holder balance)  
- Basescan links for verification  

All operations are strictly read-only.

## Repository layout

- app.luminous-harbor.ts  
  Main browser script that connects a Coinbase Wallet and performs read-only probes.

- config/networks.json  
  Base network configuration (chainIds, RPC endpoints, explorers).

- docs/design.md  
  Explanation of the read-only design and Base alignment.

- docs/testnet-guide.md  
  Guide for validating contracts on Base Sepolia testnet.

- scripts/example-addresses.json  
  Sample addresses and tokens for repeatable checks.

- contracts/  
  Solidity contracts deployed on Base Sepolia for testnet validation:
  - BaseStorageManager.sol — A contract designed to manage storage operations on Base Sepolia. Users can store, retrieve, and delete simple data types. Ideal for demonstrating how smart contracts handle basic data storage and retrieval, useful for tutorials and basic decentralized app (dApp) examples.  
  - BaseVotingSystem.sol — A simple voting contract to demonstrate how users can cast votes and tally results on-chain. This contract is a great example for governance tutorials, voting systems in dApps, and showcasing Base Sepolia's handling of decentralized decision-making  
  - BaseNFTMarketplace.sol — A simple contract designed for listing and purchasing NFTs on Base Sepolia. This contract is intended for demos showcasing how to build an NFT marketplace, handling token transfers and user interactions within decentralized applications  

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base + Coinbase repositories.

- README.md  
  Main documentation with technical details and setup instructions.

---

## Tooling and ecosystem

This project integrates with Coinbase and Base ecosystems:
- Coinbase Wallet SDK for wallet connectivity  
- OnchainKit references for Base-aligned primitives  
- viem for read-only RPC access  
- Dependencies from Base and Coinbase repositories  

---

## License

MIT License

Copyright (c) 2025

---

## Author

GitHub: https://github.com/receipt-quintet  
Email: receipt.quintet_0s@icloud.com  
Public contact: https://x.com/rinoshimaru9  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract BaseStorageManager.sol address:  
0x23D7A1C29bF46C7A3b74e90A7eB944c2F4F68B94

Deployment and verification:
- https://sepolia.basescan.org/address/0x23D7A1C29bF46C7A3b74e90A7eB944c2F4F68B94
- https://sepolia.basescan.org/0x23D7A1C29bF46C7A3b74e90A7eB944c2F4F68B94/0#code  

Contract BaseVotingSystem.sol address:  
0x5F9b6C0aD1F89C9B7B2F0C5D64E7cF4D2A389FB8

Deployment and verification:
- https://sepolia.basescan.org/address/0x5F9b6C0aD1F89C9B7B2F0C5D64E7cF4D2A389FB8
- https://sepolia.basescan.org/0x5F9b6C0aD1F89C9B7B2F0C5D64E7cF4D2A389FB8/0#code  

Contract BaseNFTMarketplace.sol address:  
0x7C1A23E8e2B9F2B4F1C1d7B7A8C5D3B2D7994535

Deployment and verification:
- https://sepolia.basescan.org/address/0x7C1A23E8e2B9F2B4F1C1d7B7A8C5D3B2D7994535
- https://sepolia.basescan.org/0x7C1A23E8e2B9F2B4F1C1d7B7A8C5D3B2D7994535/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
