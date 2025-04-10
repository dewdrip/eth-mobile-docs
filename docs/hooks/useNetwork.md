---
sidebar_position: 8
---

# useNetwork

Use this hook to read the connected network data.

```ts
const connectedNetwork = useNetwork();
```

## Return Values

- The `name` property stores the name of the network.
- The `provider` property stores the network provider url.
- The `id` property stores the chain id.
- The `currencySymbol` property stores the network currency symbol.
- The `coingeckoPriceId` property stores the [coingecko price id](https://docs.google.com/spreadsheets/d/1wTTuxXt8n9q7C4NDXqQpI3wpKu1_5bGVmP9Xz0XGSyU/edit?gid=0#gid=0) for reading crypto prices.
- The `blockExplorer` property stores the url to the network block explorer
