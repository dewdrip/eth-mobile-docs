---
sidebar_position: 2
---

# Balance

Displays the balance of a given address in ether (ETH).

![Balance Example](/img/Balance.png)

## Import

```tsx
import { Balance } from "~~/components/eth-mobile";
```

## Usage

```tsx
<Balance address="0x34aA3F359A9D614239015126635CE7732c18fDF3" />
```

## Props

| Prop                 | Type        | Default Value | Description                                                                  |
| -------------------- | ----------- | ------------- | ---------------------------------------------------------------------------- |
| **address**          | `string`    | `undefined`   | Address in `0x___` format, it will resolve its ENS if it has one associated. |
| **style** (optional) | `TextStyle` | `undefined`   | Prop to pass additional styling to the component                             |
