# Syberlock roadmap

This roadmap tracks practical milestones for the desktop password manager.

## Desktop vault

- [x] Define the offline-first application architecture.
- [x] Build the Python / PyQt5 interface and SQLite storage.
- [x] Add vault operations for storing and managing credentials.
- [x] Integrate Argon2id for key derivation and AES-GCM for password encryption.
- [ ] Add automated tests for unlocking, encryption/decryption, wrong passwords, and modified ciphertext.
- [ ] Improve failure handling and database migration tests.

## Multi-device support

- [ ] Complete authenticated device pairing.
- [ ] Implement and test protected data transfer between authorized devices.
- [ ] Handle pairing failure, lost devices, and revocation.

## Release preparation

- [ ] Finalize encrypted backup and recovery.
- [ ] Review cryptographic implementation, dependencies, and threat model.
- [ ] Obtain an independent security review.
- [ ] Test packaging and distribution on Windows and macOS.
- [ ] Release the application after security and reliability checks.
