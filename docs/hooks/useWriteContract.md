---
sidebar_position: 4
---

# useWriteContract

Use this hook to send a transaction to any smart contract to write data or perform an action.

```ts
const { writeYourContractAsync } = useWriteContract({
  abi: [YourContractABI],
  address: "0xabca6bf26964af9f7eed9e03e53415d37aa90123",
});
```

The following configuration options can be passed to the hook:

## Configuration

| Parameter              | Type       | Required | Description                                             |
| :--------------------- | :--------- | :------- | ------------------------------------------------------- |
| **abi**                | `object[]` | Yes      | ABI of the contract to read from.                       |
| **address**            | `string`   | Yes      | Address of contract to read from.                       |
| **blockConfirmations** | `number`   | No       | Number of block confirmations to wait for (default: 1). |
| **gasLimit**           | `bigint`   | No       | Transaction gas limit.                                  |

To send the transaction, you can call the `writeYourContractAsync` function returned by the hook. Here's an example usage:

```tsx
<Button
  onPress={async () => {
    try {
      await writeYourContractAsync({
        functionName: "setGreeting",
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

This example sends a transaction to the `YourContract` smart contract to call the `setGreeting` function with the arguments passed in `args`. The `writeYourContractAsync` function sends the transaction to the smart contract.

Below is the configuration for `writeYourContractAsync` function:

## Configuration

| Parameter        | Type        | Required | Description                                                                                                          |
| :--------------- | :---------- | :------- | -------------------------------------------------------------------------------------------------------------------- |
| **functionName** | `string`    | Yes      | Name of the function to be called.                                                                                   |
| **args**         | `unknown[]` | No       | Array of arguments to pass to the function (if accepts any). Types are inferred from contract's function parameters. |
| **value**        | `bigint`    | No       | Value in ETH that will be sent with transaction (for payable functions only).                                        |

## Return Values

- The loading state is stored in the `isLoading` property.
- The mining state is stored in the `isMining` property.
- `writeContract` functions send the transaction to the smart contract but doesn't return a promise.
- `writeContractAsync` function sends the transaction to the smart contract and returns a promise that resolves when transactions is successful.
