---
sidebar_position: 4
---

# 🪝 Hooks

Eth-Mobile provides a collection of custom React hooks for accounts, wallets, contracts, transactions, signing, and more

To ensure autocompletions function correctly, always update the [`networks` ](/deploying/deploy-reactnative-app#--networks) in `ethmobile.config.ts` to include the relevant network/chain whenever you deploy your contract using [`yarn deploy --network`](/deploying/deploy-smart-contracts#3-deploy-your-smart-contracts).

:::info
The custom hooks rely on three main files for their functionality and TypeScript autocompletion:

- `packages/reactnative/contracts/deployedContracts.ts`
- [`packages/reactnative/contracts/externalContracts.ts`](/external-contracts)
- `ethmobile.config.ts`

The `deployedContracts.ts` file is auto-generated/updated whenever you run `yarn deploy --network`. It organizes contract addresses and abi's based on chainId.

:::

:::note

When having multiple chains configured in [`networks`](/deploying/deploy-reactnative-app#--networks), make sure to have same contractName's on other chains as `networks[network].id`.This ensures proper functionality and autocompletion of custom hooks, as the current setup and types assumes that same contract's are present on other chains as `networks[network]`.

:::
