# Security policy

## Current security status

Syberlock is under active development. **It has not undergone an independent security audit.** It must not yet be treated as a production-ready vault or used for real, sensitive, or irreplaceable passwords.

This repository contains public design documentation; the main application code is private.

## Reporting a vulnerability

Please avoid publishing exploitation steps, vaults, keys, passwords, sensitive screenshots, or personal data in public issues.

If a private reporting channel is enabled on this repository, use it. Otherwise, contact the maintainer through a private channel listed on their GitHub profile. If no private channel is available, post a public issue **only to request a private contact method**, without technical vulnerability details.

## Minimum review gates before release

- Review threat model and expected security guarantees.
- Verify Argon2id KDF, key handling, and parameter storage.
- Verify cryptographically secure nonce generation and uniqueness for AES-GCM.
- Verify tamper detection and failure handling.
- Check for accidental plaintext storage, logs, backups, or temporary artifacts.
- Review dependency supply-chain risk and reproducibility of builds.
- Review secure pairing separately, if enabled.
- Test corruption, update, migration, and recovery scenarios.
- Arrange independent review and fix relevant findings.
- Only then consider use with real credentials or store publication.

## No bug bounty commitment

No monetary bug bounty or response-time guarantee is currently offered.