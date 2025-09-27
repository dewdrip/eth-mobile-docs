---
sidebar_position: 11
---

# useERC20Metadata

Use this hook to retrieve metadata (name, symbol, and decimals) of a specified ERC20 token.

```ts
const { data, isLoading, error, getERC20Metadata } = useERC20Metadata({
  token: "0x...",
});
```

## Usage

```tsx
import { useERC20Metadata } from "@/hooks/eth-mobile";

function TokenInfo() {
  const { data, isLoading, error, getERC20Metadata } = useERC20Metadata({
    token: "0xA0b86a33E6441b8c4C327D7d0c65Bfa0ECf0e651", // USDC
  });

  if (isLoading) return <Text>Loading token info...</Text>;
  if (error) return <Text>Error: {error}</Text>;
  if (!data) return <Text>No token data available</Text>;

  return (
    <View>
      <Text>Token Name: {data.name}</Text>
      <Text>Symbol: {data.symbol}</Text>
      <Text>Decimals: {data.decimals}</Text>
      <Button onPress={() => getERC20Metadata()} title="Refresh Metadata" />
    </View>
  );
}
```

## Configuration

| Parameter | Type      | Required | Description                       |
| :-------- | :-------- | :------- | --------------------------------- |
| **token** | `Address` | No       | The ERC20 token contract address. |

## Return Values

| Property             | Type                                                       | Description                                               |
| :------------------- | :--------------------------------------------------------- | --------------------------------------------------------- |
| **data**             | `ERC20Metadata \| null`                                    | The token metadata containing name, symbol, and decimals. |
| **isLoading**        | `boolean`                                                  | Whether the metadata is currently being fetched.          |
| **error**            | `string \| null`                                           | Any error message that occurred during metadata fetching. |
| **getERC20Metadata** | `(token?: Address) => Promise<ERC20Metadata \| undefined>` | Function to manually fetch metadata for a specific token. |
