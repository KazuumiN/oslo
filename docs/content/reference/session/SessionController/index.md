---
type: "class"
---

# `SessionController`

Provides methods for handling sessions. Sessions should be stored in your own database.

Sessions do not have an absolute expiration. Instead, Oslo uses a sliding window expiration for sessions. When a session is used within half of the time the session is valid for, the expiration gets pushed back. For an example, if the session expires in 30 days and is used within 15 days before expiration, the expiration date gets pushed back another 30 days. This allows active users to stay signed in, while inactive users are signed out.

See [`oslo/session`](/reference/session) for a full example.

## Constructor

```ts
function constructor(expiresIn: TimeSpan): this;
```

### Parameters

- `expiresIn`: How long the session is valid for

## Methods

- [`createExpirationDate()`](ref:sessio/SessionController)
- [`getSessionState()`](ref:session/SessionController)

## Properties

```ts
//$ TimeSpan=ref:main
interface Properties {
	expiresIn: $$TimeSpan;
}
```

- `expiresIn`

## Example

```ts
import { SessionController } from "oslo/session";
import { TimeSpan } from "oslo";

const sessionController = new SessionController(new TimeSpan(30, "d"));
```
