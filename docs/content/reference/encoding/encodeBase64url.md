---
type: "function"
---

# `encodeBase64url()`

Encodes data into base64 URL string. Use [`decodeBase64url()`](ref:encoding) to decode base64 URL strings.

## Definition

```ts
function encodeBase64url(data: ArrayBuffer): string;
```

### Parameters

- `data`

## Example

```ts
import { encodeBase64url } from "oslo/encoding";

const data = new TextEncoder("hello, world");
const encoded = encodeBase64url(data);
```
