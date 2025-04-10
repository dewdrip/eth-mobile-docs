---
sidebar_position: 1
---

# Address

Display an address along with a utility icon to copy the address. A blockie image representation of the address will be shown.

![Address Example](/img/AddressOnlyEnsOrAddress.png)

## Import

```tsx
import { Address } from "~~/components/eth-mobile";
```

## Usage

```tsx
<Address address="0x34aA3F359A9D614239015126635CE7732c18fDF3" />
```

## Props

| Prop                          | Type        | Default Value | Description                                                                  |
| ----------------------------- | ----------- | ------------- | ---------------------------------------------------------------------------- |
| **address**                   | `string`    | `undefined`   | Address in `0x___` format, it will resolve its ENS if it has one associated. |
| **containerStyle** (optional) | `ViewStyle` | `undefined`   | Style the component container.                                               |
| **textStyle** (optional)      | `TextStyle` | `undefined`   | Style the address.                                                           |
| **iconStyle** (optional)      | `TextStyle` | `undefined`   | Style the copy icon.                                                         |
