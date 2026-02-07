# ZkVanguard Contracts (SUI)

> Move smart contracts for the ZkVanguard platform on SUI Network

[![SUI](https://img.shields.io/badge/SUI-Testnet-cyan)](https://sui.io)
[![Move](https://img.shields.io/badge/Move-2024.beta-blue)](https://move-language.github.io/move/)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue)](LICENSE)

## Deployed Modules

| Module | Shared Object ID |
|--------|-----------------|
| `rwa_manager` | `0x65638c3c5a5af66c33bf06f57230f8d9972d3a5507138974dce11b1e46e85c97` |
| `zk_verifier` | `0x6c75de60a47a9704625ecfb29c7bb05b49df215729133349345d0a15bec84be8` |
| `zk_proxy_vault` | `0x5a0c81e3c95abe2b802e65d69439923ba786cdb87c528737e1680a0c791378a4` |
| `zk_hedge_commitment` | `0x9c33f0df3d6a2e9a0f137581912aefb6aafcf0423d933fea298d44e222787b02` |
| `payment_router` | `0x1fba1a6a0be32f5d678da2910b99900f74af680531563fd7274d5059e1420678` |

**Package ID:** `0x142e6c41391f0d27e2b5a2dbf35029809efbf78e340369ac6f1ce8fb8aa080b6`

## Architecture

```
sources/
├── rwa_manager.move          # Portfolio management on SUI
├── zk_verifier.move          # ZK-STARK proof verification
├── zk_proxy_vault.move       # Escrow with ZK ownership proofs
├── zk_hedge_commitment.move  # Privacy-preserving hedge commitments
└── payment_router.move       # Sponsored transaction routing
```

## Setup

```bash
# Install SUI CLI
cargo install --locked --git https://github.com/MystenLabs/sui.git sui

# Build
sui move build

# Test
sui move test

# Deploy to testnet
sui client publish --gas-budget 100000000
```

## Dependencies

```toml
[dependencies]
Sui = { git = "https://github.com/MystenLabs/sui.git", subdir = "crates/sui-framework/packages/sui-framework", rev = "testnet-v1.46.0" }
```

## Related Repos

- [ZkVanguard](https://github.com/ZkVanguard/ZkVanguard) — Main application
- [contracts-evm](https://github.com/ZkVanguard/contracts-evm) — Cronos EVM contracts
- [ai-agents](https://github.com/ZkVanguard/ai-agents) — Multi-agent AI system
- [zkp-engine](https://github.com/ZkVanguard/zkp-engine) — ZK-STARK proof engine

## License

Apache 2.0
