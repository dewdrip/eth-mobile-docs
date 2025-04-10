---
sidebar_position: 5
---

# 📡 Interacting with External Contracts

If you need to interact with external contracts (i.e. not deployed with your ETH Mobile instance, e.g [`DAI`](https://etherscan.io/token/0x6b175474e89094c44da98b954eedeac495271d0f#code) contract) you can add external contract data to your `packages/reactnative/contracts/externalContracts.ts` file, which would let you use ETH Mobile [custom hooks](/hooks).

To achieve this, include the contract name, its `address`, and `abi` in `externalContracts.ts` for each chain ID. Ensure to update the [`networks`](/deploying/deploy-reactnative-app#--networks) in `ethmobile.config.ts` to your preferred chains to enable hooks typescript autocompletion.

This is the structure of `externalContracts` object:

```ts
const externalContracts = {
  1: {
    DAI: {
      address: "0x...",
      abi: [...],
    },
    WETH: {
      address: "0x...",
      abi: [...],
    },
  },
  5: {
    DAI: {
      address: "0x...",
      abi: [...],
    },
    WETH: {
      address: "0x...",
      abi: [...],
    },
  },
} as const;
```
