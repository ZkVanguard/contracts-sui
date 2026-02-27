# ZkVanguard Contracts (SUI)

Move smart contracts for ZkVanguard on SUI Network.

## Overview

This repository contains Move modules for ZkVanguard's multi-chain risk management:

- **zkvanguard.move** - Core portfolio and hedging logic
- **community_pool.move** - Shared liquidity pool
- **zk_verifier.move** - Zero-knowledge proof verification

## Deployments

### SUI Testnet
See deployment addresses in main repo.

## Development

### Prerequisites
- SUI CLI
- Move Prover (optional)

### Build
```bash
sui move build
```

### Test
```bash
sui move test
```

### Deploy
```bash
sui client publish --gas-budget 100000000
```

## License

Apache License 2.0

## Related Repositories

- [ZkVanguard](https://github.com/ZkVanguard/ZkVanguard) - Main application
- [contracts-evm](https://github.com/ZkVanguard/contracts-evm) - Solidity contracts
- [ai-agents](https://github.com/ZkVanguard/ai-agents) - AI agent swarm
- [zkp-engine](https://github.com/ZkVanguard/zkp-engine) - ZK-STARK proof engine
