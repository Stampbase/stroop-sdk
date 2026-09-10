# Stroop SDK

> Public integration SDK for resolving Stroop identities.

Part of [Stroop](https://github.com/Stampbase), an open identity layer for
Stellar, built by [Stampbase](https://github.com/Stampbase).

## Where this fits

The SDK is how third-party applications integrate Stroop. Passport uses the
same public interfaces available to everyone else — Stroop has no privileged
internal client.

## Status

**Pre-alpha.** Scaffolding only. No package has been published to npm.

Nothing here is deployed to Stellar mainnet. Do not use any part of this
repository to custody value.

### Planned packages

| Package | Purpose |
| --- | --- |
| `@stroop-id/sdk` | Resolution and profile reads |
| `@stroop-id/react` | React components over the SDK |

### Planned API

```ts
resolve("@bastian")
resolve("G...")
getProfile(...)
getAvatar(...)
getPaymentDestination(...)
```

```tsx
<Stroopy address={address} />
<StroopProfile address={address} />
<StroopName address={address} />
```

### Principles

- No telemetry, ever, by default.
- No API key required for ordinary public resolution.
- Mainnet and testnet are explicit in every public API surface.
- Critical identity data resolves without depending exclusively on
  Stroop-operated infrastructure.

## Testing

```bash
npm run lint
npx tsc --noEmit
npm test
npm run build
```

## Security

Do not report vulnerabilities through public issues. See
[`SECURITY.md`](./SECURITY.md) for private reporting.

## License

[Apache-2.0](./LICENSE).

## Related repositories

| Repository | Purpose |
| --- | --- |
| [`stroop-contracts`](https://github.com/Stampbase/stroop-contracts) | Soroban contracts: identity registry, usernames, wallet links |
| [`stroop-sdk`](https://github.com/Stampbase/stroop-sdk) | `@stroop-id/sdk` and `@stroop-id/react` |
| [`stroop-web`](https://github.com/Stampbase/stroop-web) | stroop.id — identity application |
| [`stroopy`](https://github.com/Stampbase/stroopy) | stroopy.me — character application |
| [`stroop-docs`](https://github.com/Stampbase/stroop-docs) | Protocol specifications |
