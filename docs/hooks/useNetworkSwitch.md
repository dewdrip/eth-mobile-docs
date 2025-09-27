---
sidebar_position: 9
---

# useNetworkSwitch

Use this hook to switch between configured networks.

```ts
const { switchNetwork } = useNetworkSwitch();
```

## Usage

```tsx
import { useNetworkSwitch } from "@/hooks/eth-mobile";

function NetworkSwitcher() {
  const { switchNetwork } = useNetworkSwitch();

  return <Button onPress={switchNetwork}>Switch Network</Button>;
}
```

## Return Values

- The `switchNetwork` function lists configured networks to switch to.
