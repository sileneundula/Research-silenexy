# Research-silenexy

Research covered by silene (named after the plant Silene Undula, a shamanistic plant that induces vivid dreams)

## Research

- [X] **Oblivious Data Integrity Verification:** A method of obliviously verifying data between two parties without revealing the data using homomorphic encryption.

- [X] **RustySigs-Ephermal-Signatures:** A secure, ephermal, cryptographically random way of signing data using cryptographic randomness and the public key, thus creating an id that changes per each signature which can be used to verify public key through the signature. It uses secure cryptographic randomness to produce ephermal signatures. The current implementation uses ED25519 and SPHINCS+ (ShulginSigning) with hedged signatures. The implementation can be found in `librustysigs`

- [X] **ShulginSigning:** A Secure, Post-Quantum, Long-Term, Sustainable Signing Algorithm based on ED25519/ED448 and SPHINCS+ (SHAKE256) (Level 5) with hedged signatures and small public key / secret key sizes. It is named after Alexander Shulgin, the creator of TIHKAL and PIHKAL. It's security is based around well-known assumptions in hash functions and elliptic curves.

- [X] **EsphandAuth:** A type of authentication process.
