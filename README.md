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
  - your_contract.sol — minimal deployment validation contract  
  - your_contract.sol — stateful contract for interaction testing  
  - your_contract.sol — read-only contract for queries  

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

Copyright (c) 2025 YOUR_NAME

---

## Author

GitHub: https://github.com/your-handle  
Email: you@example.com  
Public contact: https://x.com/your-handle  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

Contract #2 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

Contract #3 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
