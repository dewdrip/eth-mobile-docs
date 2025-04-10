---
sidebar_position: 1
---

# useScaffoldContractRead

Use this hook to read public variables and get data from read-only functions of your smart contract.

```ts
const { data: totalCounter } = useScaffoldContractRead({
  contractName: "YourContract",
  functionName: "userGreetingCounter",
  args: ["0xd8da6bf26964af9d7eed9e03e53415d37aa96045"],
});
```

This example retrieves the data returned by the `userGreetingCounter` function of the `YourContract` smart contract.

## Configuration

| Parameter           | Type        | Description                                                                                                         |
| :------------------ | :---------- | :------------------------------------------------------------------------------------------------------------------ |
| **contractName**    | `string`    | Name of the contract to read from.                                                                                  |
| **functionName**    | `string`    | Name of the function to call.                                                                                       |
| **args** (optional) | `unknown[]` | Array of arguments to pass to the function (if accepts any). Types are inferred from contract's function parameters |

## Return Values

- The retrieved data is stored in the `data` property of the returned object.
- You can refetch the data by calling the `refetch` function.
