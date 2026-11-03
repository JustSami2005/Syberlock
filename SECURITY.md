# Security

## Current status

Syberlock is a desktop password manager **in development**, and it has not received an independent security review. It is not ready to store real passwords.

## Current design

- The vault stores credentials locally in SQLite.
- Argon2id derives a 32-byte key from the master password and a per-vault random salt.
- AES-GCM encrypts stored **passwords** and authenticates their ciphertext.
- A new random 12-byte nonce is generated with `os.urandom(12)` for each encryption and stored separately with the ciphertext.
- Service names and usernames are currently **not encrypted**.

For implementation details, see [Architecture](docs/ARCHITECTURE.md).

## Before release

- Automated tests for incorrect passwords, modified ciphertext, and database errors.
- Nonce handling and key-management review.
- Review of plaintext storage, logging, backups, and temporary data.
- Verification of the future pairing protocol.
- Dependency audit and independent security review.

## Reporting a security issue

Please do **not** share secrets, passwords, vault files, or detailed exploits in public issues. Use GitHub's private vulnerability reporting if enabled; otherwise, ask for a private contact channel without disclosing vulnerability details.

No bug bounty program is offered at this time.
