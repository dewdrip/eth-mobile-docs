---
sidebar_position: 8
---

# Blockie

Show a blockie (bar code profile icon) component for a given public address.

![Blockie Example](/img/BlockieAvatar.png)

## Import

```tsx
import { Blockie } from "~~/components/eth-mobile";
```

## Usage

```tsx
<Blockie address="0x34aA3F359A9D614239015126635CE7732c18fDF3" size={24} />
```

## Props

| Prop      | Type     | Default Value | Description                                                                               |
| --------- | -------- | ------------- | ----------------------------------------------------------------------------------------- |
| `address` | `string` | `undefined`   | The address for which you want to display its blockie. Ensure it's in the `0x___` format. |
| `size`    | `number` | `undefined`   | Width and Height in pixels (square).                                                      |
