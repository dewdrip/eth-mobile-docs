---
sidebar_position: 10
---

# useERC20Balance

Use this hook to retrieve the balance of a specified ERC20 token for a user address.

```ts
const { balance, isLoading, error, getBalance } = useERC20Balance({
  token: "0x...",
  userAddress: "0x...",
  watch: true,
});
```

## Usage

```tsx
import { useERC20Balance } from "~~/hooks/eth-mobile";

function TokenBalance() {
  const { balance, isLoading, error, getBalance } = useERC20Balance({
    token: "0xA0b86a33E6441b8c4C327D7d0c65Bfa0ECf0e651", // USDC
    userAddress: "0x1234...",
    watch: true,
  });

  if (isLoading) return <Text>Loading balance...</Text>;
  if (error) return <Text>Error: {error}</Text>;

  return (
    <View>
      <Text>Token Balance: {balance?.toString()}</Text>
      <Button onPress={() => getBalance()} title="Refresh Balance" />
    </View>
  );
}
```

## Configuration

| Parameter       | Type      | Required | Description                                                          |
| :-------------- | :-------- | :------- | -------------------------------------------------------------------- |
| **token**       | `Address` | No       | The ERC20 token contract address.                                    |
| **userAddress** | `Address` | No       | The address of the user to fetch the token balance for.              |
| **watch**       | `boolean` | No       | Whether to watch for balance changes on new blocks (default: false). |

## Return Values

| Property       | Type                                                                       | Description                                                     |
| :------------- | :------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **balance**    | `bigint \| null`                                                           | The current token balance of the user.                          |
| **isLoading**  | `boolean`                                                                  | Whether the balance is currently being fetched.                 |
| **error**      | `string \| null`                                                           | Any error message that occurred during balance fetching.        |
| **getBalance** | `(token?: Address, userAddress?: Address) => Promise<bigint \| undefined>` | Function to manually fetch the balance for specific token/user. |
