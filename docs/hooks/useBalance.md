---
sidebar_position: 7
---

# useBalance

Use this hook to read the balance of any address.

```ts
const { balance } = useBalance({
  address: "0xabca6bf26964af9f7eed9e03e53415d37aa90123",
});
```

## Configuration

| Parameter   | Type     | Description           |
| :---------- | :------- | :-------------------- |
| **address** | `string` | Address to read from. |

## Return Values

- The balance is stored in the `balance` property.
- The loading state is stored in the `isLoading` property.
- The refetching state is stored in the `isRefetching` property.
- You can refetch the balance by calling the `refetch` function.
- The `error` property stores any errors during reads.
