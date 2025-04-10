---
sidebar_position: 4
---

# useContractWrite

Use this hook to send a transaction to any smart contract to write data or perform an action.

```ts
const { write: writeYourContractAsync } = useContractWrite({
  abi: [YourContractABI],
  address: "0xabca6bf26964af9f7eed9e03e53415d37aa90123",
  functionName: "setGreeting",
});
```

The following configuration options can be passed to the hook:

## Configuration

| Parameter                         | Type        | Description                                             |
| :-------------------------------- | :---------- | :------------------------------------------------------ |
| **abi**                           | `object[]`  | ABI of the contract to read from.                       |
| **address**                       | `string`    | Address of contract to read from.                       |
| **functionName**                  | `string`    | Name of the function to be called.                      |
| **args** (optional)               | `unknown[]` | Arguments for the function.                             |
| **value** (optional)              | `bigint`    | Value in ETH that will be sent with transaction.        |
| **blockConfirmations** (optional) | `number`    | Number of block confirmations to wait for (default: 1). |
| **gasLimit** (optional)           | `bigint`    | Transaction gas limit.                                  |

To send the transaction, you can call the `write` function returned by the hook (which we instance as `writeYourContractAsync`). Here's an example usage:

```tsx
<Button
  onPress={async () => {
    try {
      await writeYourContractAsync({
        args: ["The value to set"],
        value: parseEther("0.1"),
      });
    } catch (e) {
      console.error("Error setting greeting:", e);
    }
  }}
>
  Set Greeting
</Button>
```

This example sends a transaction to the `YourContract` smart contract to call the `setGreeting` function with the arguments passed in `args`. The `write` function (`writeYourContractAsync` instance) sends the transaction to the smart contract.

Below is the configuration for `write` function:

## Configuration

| Parameter            | Type        | Description                                                                                                          |
| :------------------- | :---------- | :------------------------------------------------------------------------------------------------------------------- |
| **args** (optional)  | `unknown[]` | Array of arguments to pass to the function (if accepts any). Types are inferred from contract's function parameters. |
| **value** (optional) | `bigint`    | Amount of ETH to send with the transaction (for payable functions only).                                             |

## Return Values

- The loading state is stored in the `isLoading` property.
- `write` function sends the transaction to the smart contract.
