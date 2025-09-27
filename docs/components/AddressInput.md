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

| Prop                        | Type                      | Default Value | Required | Description                                                                  |
| --------------------------- | ------------------------- | ------------- | -------- | ---------------------------------------------------------------------------- |
| **value**                   | `string`                  | `undefined`   | Yes      | An Ethereum address in (`0x___` format) or an ENS domain.                    |
| **placeholder**             | `string`                  | `undefined`   | No       | The string that will be rendered before address input has been entered.      |
| **error**                   | `string`                  | `undefined`   | No       | Error message to display below the input.                                    |
| **onChange**                | `(value: string) => void` | `undefined`   | Yes      | A callback invoked when the data in the address input changes.               |
| **onSubmit**                | `() => void`              | `undefined`   | No       | A callback function invoked when the data in the address input is submitted. |
| **containerClassName**      | `string`                  | `undefined`   | No       | Tailwind CSS class name for the main container wrapper.                      |
| **inputContainerClassName** | `string`                  | `undefined`   | No       | Tailwind CSS class name for the input container.                             |
| **inputClassName**          | `string`                  | `undefined`   | No       | Tailwind CSS class name for the input element.                               |
| **errorClassName**          | `string`                  | `undefined`   | No       | Tailwind CSS class name for the error message display.                       |
| **scan**                    | `boolean`                 | `undefined`   | No       | If set to true, an icon will be displayed to scan addresses.                 |
