# @permission-protocol/cli [![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](./LICENSE)

```bash
npm i -g @permission-protocol/cli
pp verify ./receipt.json --key-file ./public-key.pem
pp verify rcpt_abc123
```

Verify Permission Protocol receipts locally with Ed25519 signature checks and canonicalized payload validation.

## Exit codes

| Code | Meaning |
| --- | --- |
| 0 | Receipt valid |
| 1 | Signature invalid |
| 2 | Receipt expired or revoked |
| 3 | Receipt malformed |
| 4 | Key resolution failed |
| 64 | Usage error |

## What does this prove?

`pp verify` proves a receipt was signed by the matching public key over the canonical signed fields, and that the receipt is still valid (not expired/revoked). This is local cryptographic verification, not a trust-me API response.

`pp` is the reference verifier for the [**`pp-receipt-v1`**](https://github.com/permission-protocol/receipt-spec) open specification.

See https://permissionprotocol.com/trust.
