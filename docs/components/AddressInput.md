---
sidebar_position: 3
---

# AddressInput

Display an Ethereum address input that shows a blockie image for each address.

![AddressInput Example](/img/AddressInput.png)

## Import

```tsx
import { AddressInput } from "~~/components/eth-mobile";
```

## Usage

```tsx
const [address, setAddress] = useState("");
```

```tsx
<AddressInput onChange={setAddress} value={address} placeholder="Input your address" />
```

## Props

| Prop               | Type        | Default Value | Required | Description                                                                  |
| ------------------ | ----------- | ------------- | -------- | ---------------------------------------------------------------------------- |
| **value**          | `string`    | `undefined`   | Yes      | An Ethereum address in (`0x___` format) or an ENS domain.                    |
| **onChange**       | `function`  | `undefined`   | Yes      | A callback invoked when the data in the address input changes.               |
| **placeholder**    | `string`    | `undefined`   | No       | The string that will be rendered before address input has been entered.      |
| **onSubmit**       | `function`  | `undefined`   | No       | A callback function invoked when the data in the address input is submitted. |
| **containerStyle** | `ViewStyle` | `undefined`   | No       | A style object for the wrapper.                                              |
| **inputStyle**     | `TextStyle` | `undefined`   | No       | A style object for the container.                                            |
| **outlineStyle**   | `TextStyle` | `undefined`   | No       | A style object for the outlined wrapper.                                     |
| **contentStyle**   | `TextStyle` | `undefined`   | No       | A style object for the content.                                              |
| **scan**           | `boolean`   | `undefined`   | No       | If set to true, an icon will be displayed to scan addresses.                 |
