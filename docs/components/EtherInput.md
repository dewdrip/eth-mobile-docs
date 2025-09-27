---
sidebar_position: 4
---

# EtherInput

A component that allows users to input an amount of ETH with real-time ETH/USD conversion and balance validation.

![EtherInput Example](/img/EtherInput.gif)

## Import

```tsx
import { EtherInput } from "@/components/eth-mobile";
```

## Usage

```tsx
const [ethAmount, setEthAmount] = useState("");
const userBalance = useBalance(); // Your balance hook

<EtherInput
  value={ethAmount}
  onChange={setEthAmount}
  onSubmit={() => console.log("Submitted:", ethAmount)}
  balance={userBalance}
/>;
```

## Props

| Prop         | Type                      | Default Value | Required | Description                                                                |
| ------------ | ------------------------- | ------------- | -------- | -------------------------------------------------------------------------- |
| **value**    | `string`                  | `undefined`   | Yes      | The current input value (ETH amount or USD amount based on currency mode). |
| **onChange** | `(value: string) => void` | `undefined`   | Yes      | Callback invoked when the input value changes.                             |
| **onSubmit** | `() => void`              | `undefined`   | Yes      | Callback function invoked when the user submits the input value.           |
| **balance**  | `bigint \| null`          | `undefined`   | No       | The user's ETH balance for validation (optional).                          |
| **disabled** | `boolean`                 | `false`       | No       | Whether the input is disabled.                                             |
