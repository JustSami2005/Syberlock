# Roadmap

This is a living plan; it is not a release schedule.

## Stage 1 — Prototype

- [x] Define offline-first desktop product scope.
- [x] Select Python / PyQt5 / SQLite.
- [x] Select Argon2id and AES-GCM for the cryptographic design.
- [ ] Verify every basic vault action against the implementation and automated tests.
- [ ] Review login/unlock failure modes.

## Stage 2 — Reliability and security

- [ ] Test AES-GCM round trips and tampering rejection.
- [ ] Test KDF settings, wrong passwords, and migration behavior.
- [ ] Check nonce uniqueness and secret-free logging.
- [ ] Add safe backup/export and recovery design.
- [ ] Define threat model and perform dependency audit.
- [ ] Obtain an independent review before real-world password use.

## Stage 3 — Device support

- [ ] Specify an authenticated device enrollment protocol.
- [ ] Securely transfer vault data between authorized devices.
- [ ] Test revocation, replay attacks, and network failures.

## Stage 4 — Distribution

- [ ] Test Windows and macOS installers.
- [ ] Sign distributable binaries as applicable.
- [ ] Add release notes, support documentation, and update strategy.
- [ ] Publish only after release gates pass.

A checked design decision **does not** mean the corresponding code has passed a security audit.
