---
type: "interface"
---

# `PasswordHashingAlgorithm`

A generic interface for hashing and verifying passwords.

## Definition

```ts
interface PasswordHashingAlgorithm {
	hash(password: string): Promise<string>;
	verify(hash: string, password: string): Promise<boolean>;
}
```

### Methods

- `hash()`
- `verify()`

## Implemented by

- [`Argon2id`](ref:password)
- [`Bcrypt`](ref:password)
- [`Scrypt`](ref:password)
