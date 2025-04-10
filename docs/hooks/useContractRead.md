---
sidebar_position: 3
---

# useContractRead

Use this hook to read public variables and get data from read-only functions of any contract.

```ts
const { data: totalCounter } = useScaffoldContractRead({
  abi: [YourContractABI],
  address: "0xabca6bf26964af9f7eed9e03e53415d37aa90123",
  functionName: "userGreetingCounter",
  args: ["0xd8da6bf26964af9d7eed9e03e53415d37aa96045"],
});
```

This example retrieves the data returned by the `userGreetingCounter` function of the `YourContract` smart contract.

## Configuration

| Parameter           | Type        | Description                                                                                                         |
| :------------------ | :---------- | :------------------------------------------------------------------------------------------------------------------ |
| **abi**             | `object[]`  | ABI of the contract to read from.                                                                                   |
| **address**         | `string`    | Address of contract to read from.                                                                                   |
| **functionName**    | `string`    | Name of the function to call.                                                                                       |
| **args** (optional) | `unknown[]` | Array of arguments to pass to the function (if accepts any). Types are inferred from contract's function parameters |
| **enabled**         | `boolean`   | Should fetch data onMount. (default: true)                                                                          |
| **onError**         | `function`  | Function to handle errors.                                                                                          |

## Return Values

- The retrieved data is stored in the `data` property.
- The loading state is stored in the `isLoading` property.
- You can refetch the data by calling the `refetch` function.
- The `error` property stores any errors during reads.
- You can also use `readContract` function to read data by filling the object parameter with - `abi`,
  `address`,
  `functionName`,
  `args`
