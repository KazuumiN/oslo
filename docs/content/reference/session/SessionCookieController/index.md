---
type: "class"
---

# `SessionCookieController`

Provides methods for handling session cookies. By default, session cookies have a `Secure` flag. This should be disabled when developing locally. See [`oslo/session`](/reference/session) for a full example.

## Constructor

```ts
function constructor(
	cookieName: string,
	expiresIn: TimeSpan,
	options?: {
		secure?: boolean;
		path?: string;
		domain?: string;
		sameSite?: "lax" | "strict";
	}
): this;
```

### Parameters

- `cookieName`
- `expiresIn`
- `options`
  - `secure` (default: `true`): `Secure` cookie attribute
  - `path` (default: `/`): `Path` cookie attribute
  - `domain`: `Domain` cookie attribute
  - `sameSite` (default: `"lax"`): `SameSite` cookie attribute

## Methods

- [`createBlankSessionCookie()`](ref:session/SessionCookieController)
- [`createSessionCookie()`](ref:session/SessionCookieController)
- [`parseCookies()`](ref:session/SessionCookieController)

## Example

```ts
import { SessionCookieController } from "oslo/session";
import { TimeSpan } from "oslo";

const controller = new SessionCookieController(cookieName, new TimeSpan(30, "d"), {
	secure: false // for localhost
});
```
