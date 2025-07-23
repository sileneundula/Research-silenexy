# ESPHAND AUTH

## Description

ESPHAND AUTH is a post-quantum, digital signature based authentication method using the algorithms ED25519 or ED448 (with hedged signatures) and SPHINCS+ (SHAKE256).

## Extensions

- Decentralized Login

## Why It Works

Due to the limited size of SPHINCS+ public keys / secret keys, it is allowable to authenticate this way in a new age.

## How It Works

### Registration

1. Client Sends ESPHAND AUTH REGISTRATION (ESPH-R) with a chosen signature.
2. Server then reviews the chosen signature for allowability.
3. If Server accepts, the user is registered. If not, they are rejected.

### Login

1. Client requests from server
2. Server then sends a cryptographically signed message.
3. The user then signs the message and sends back the signature with everything included.

### Conclusion

Should the public key be signed? We believe so :)
