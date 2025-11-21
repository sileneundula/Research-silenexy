# ESPHAND AUTHENTICATION IN DISTRIBUTED SYSTEMS

## Abstract

Distributed Systems and Decentralized Alternatives to the primary means of communication offer many security benefits, trust benefits, and some uses that can be applied to different areas of computer science to achieve a system that works independent of other pieces of software.

## 1. Introduction

## 2. ESPHAND AUTH

ESPHAND AUTH takes multiple pieces of cryptography and put them together to get a decentralized, transparent, authentication system that uses the following primitives:

- The Block Lattice
- Verifiable Random Functions (VRFs) like SchnorrVRFs
- Zero-Knowledge Proof of Preimages of Hash Functions (STARKS offering post-quantum or SNARKS)
- Digital Signatures (post-quantum or classical using hedged ED25519/ED448 signatures with a hybrid post-quantum algorithm)
- A Randomness Beacon Chain

## 2.1 Step 1: Construction of The Block Lattice

The Block Lattice is constructed using a consensus mechanism. Each address contains web services, clients, or other needed information. To authenticate with a web service, a tx is made in the block lattice using a verifiable random function (VRF) that is provided by the randomness beacon chain at the time of the transaction. This VRF is then hashed with the web services address, the clients address, and the VRF with extra metadata attached to it, then signed by the client and sent as a tx.

The web service then has the option to send extra metadata or communicate on-chain with specific attributes and specific information through the block lattice and a **derived address**. This derived address can be used for communicating important information securely and also in a decentralized manner.
