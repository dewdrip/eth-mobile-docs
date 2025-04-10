---
sidebar_position: 8
---

# useSignMessage

Use this hook to sign messages.

```ts
const { signMessage } = useSignMessage({
  message: "I will rule the world... MuaHa! HA! ha! hA!",
});
```

## Configuration

| Parameter   | Type     | Description      |
| :---------- | :------- | :--------------- |
| **message** | `string` | Message to sign. |

## Return Values

- You can use the `signMessage` function to sign messages. Optionally, you can pass the above configuration as an argument
