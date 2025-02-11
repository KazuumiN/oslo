---
type: "class"
---

# `OAuth2Client`

Helper for OAuth 2.0, as defined in [RFC 6749](https://datatracker.ietf.org/doc/html/rfc6749). See [`oslo/oauth2`](/reference/oauth2) for a full example.

## Constructor

```ts
function constructor(
	clientId: string,
	authorizeEndpoint: string,
	tokenEndpoint: string,
	options?: {
		redirectURI?: string;
		responseMode?: "form_post" | "query" | "fragment";
	}
): this;
```

### Parameters

- `clientId`
- `authorizeEndpoint`
- `tokenEndpoint`
- `options`
  - `redirectURI`
  - `responseMode` (default: `"query"`)

## Methods

- [`createAuthorizationURL()`](ref:oauth2/OAuth2Client)
- [`refreshAccessToken()`](ref:oauth2/OAuth2Client)
- [`validateAuthorizationCode()`](ref:oauth2/OAuth2Client)

## Properties

```ts
interface Properties {
	clientId: string;
}
```

- `clientId`
