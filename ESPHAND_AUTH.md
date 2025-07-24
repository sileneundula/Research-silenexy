# ESPHAND AUTH: A Public-Key Authentication System Using Verifiable Random Functions and Post-Quantum Cryptography (ED25519 and SPHINCS+)

**Author:** silene
**Publication:** 7/22/2025-7/23/2025
**Last Update:** 7/24/2025

## Description

ESPHAND AUTH is a post-quantum, digital signature based authentication method using the algorithms ED25519 or ED448 (with hedged signatures) and SPHINCS+ (SHAKE256). It also uses Verifiable-Random Functions (VRFs).

It uses a **randomness beacon** derived from a public seed per instance of authentication service (so in other words, multiple services can use the same beacon).

Login can be decentralized due to the usage of Block Lattices.

## Styles

- Normal (Public Key Registration and Login)
- Decentralized Login
- Ephermal Keys

## How It Works

### Registration

1. Client Sends ESPHAND AUTH REGISTRATION (ESPH-R) with a chosen signature.
2. Server then reviews the chosen signature for allowability and sends their public key vrf.
3. If Server accepts, the user is registered. If not, they are rejected.

### Login

1. Client requests from server
2. Server then sends a cryptographically signed message.
3. The user then signs the message and sends back the signature with everything included.

### [Extension] Decentralized Esphand Auth

Using Esphand-Auth, a decentralized approach can be taken to ensure logins occur. This approach is known as `SyEsphandAuth`.

It involves public storage of keys using a database. These decentralized databases server as an easy way to store keys publically, due to the keys only being public keys.

#### Components

- Verifiable-Random Function (VRF) using Public Keys
- Randomness Beacon
- Node Network with Weighted Trust(using WOTS+ signatures/XMSS/SPHINCS+)


##### Verifiable Random Function

A **Verifiable-Random Function (VRF)** is setup.

For example, a schnorr VRF. This serves as verifiable random source that can be verified by the public key. The server holds the public key/secret key and is easily available.

##### Randomness Beacon

The randomness beacon is a beacon that derives randomness from an initial seed.

##### Post-Quantum Node Network With Weighted Trust For Confirming Logins

A Node Network is setup using XMSS or SPHINCS+.

In the case of SPHINCS+, the public key is only 32-64 bytes in size and stateless, making it able to store a reputation system based on the number of correct logins.

The **trust** is derived from:

- how long the key has been around for and registered
- how many valid logins the key has processed
- how many invalid logins the key has processed
- the services it has interacted with (making a web of trust)
- other data

## Why It Works

Due to the limited size of SPHINCS+ public keys / secret keys, it is allowable to authenticate this way in a new age.

### Conclusion

Should the public key be signed? We believe so :)
