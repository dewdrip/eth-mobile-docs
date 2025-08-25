---
sidebar_position: 12
---

# useERC721Metadata

Use this hook to retrieve metadata (name, symbol, and tokenURI) of a specified NFT (ERC721) token.

```ts
const { data, isLoading, error, getERC721Metadata } = useERC721Metadata({
  nft: "0x...",
  tokenId: "123",
});
```

## Usage

```tsx
import { useERC721Metadata } from "~~/hooks/eth-mobile";

function NFTInfo() {
  const { data, isLoading, error, getERC721Metadata } = useERC721Metadata({
    nft: "0xBC4CA0EdA7647A8aB7C2061c2E118A18a936f13D", // BAYC
    tokenId: "123",
  });

  if (isLoading) return <Text>Loading NFT info...</Text>;
  if (error) return <Text>Error: {error}</Text>;
  if (!data) return <Text>No NFT data available</Text>;

  return (
    <View>
      <Text>Collection Name: {data.name}</Text>
      <Text>Symbol: {data.symbol}</Text>
      <Text>Token URI: {data.tokenURI}</Text>
      <Button onPress={() => getERC721Metadata()} title="Refresh Metadata" />
    </View>
  );
}
```

## Configuration

| Parameter   | Type               | Required | Description                                  |
| :---------- | :----------------- | :------- | -------------------------------------------- |
| **nft**     | `Address`          | No       | The ERC721 NFT contract address.             |
| **tokenId** | `string \| number` | No       | The specific token ID to fetch metadata for. |

## Return Values

| Property              | Type                                                                                  | Description                                                   |
| :-------------------- | :------------------------------------------------------------------------------------ | ------------------------------------------------------------- |
| **data**              | `ERC721Metadata \| null`                                                              | The NFT metadata containing name, symbol, and tokenURI.       |
| **isLoading**         | `boolean`                                                                             | Whether the metadata is currently being fetched.              |
| **error**             | `string \| null`                                                                      | Any error message that occurred during metadata fetching.     |
| **getERC721Metadata** | `(nft?: Address, tokenId?: string \| number) => Promise<ERC721Metadata \| undefined>` | Function to manually fetch metadata for a specific NFT/token. |
