# Immutable-Storage-Solution (Standard) with Lemur

## Abstract

The idea of bitcoin as a decentralized, verifiable, decentralized ledger has sparked interest in many applications of blockchains. In the case of bitcoin, time-stamping and monetary incentives are addressed, while other projects like Filecoin and Arweave have looked to use blockchains for storing data. These blockchains come at a cost though, often requiring monetary incentives to store data. In the case of Filecoin, the storage is not permenant like Arweave, which both require monetary transactions to store data on-chain. Projects like IPFS have addressed issues with storage, although files need to be pinned to be held onto and there are times when this is not neccessary and instead, a cryptographic historical archive is needed.

In this whitepaper, I will detail out `Immutable Storage Solution (ISS) Standard`, a decentralized standard for immutable storage solution with quick lookups that uses a form of *Proof-of-History* for timestamping and *MiniPoW* for spam-protection. To add to this, `LEMUR`, a content-sharing platform that uses `ISS` to rebuild data/files or more complex types of data with security interact and extensible features, is explained/developed similar to how other platforms like bittorrent work. The main focus on this project is developing a standard that does not require monetary incentives to store data on the chain, remaining decentralized and censorship-resistant, and having modularity to include other features.

## 1. Introduction

Bitcoin introduced us the blockchain technology. The idea that a time-stamping server could be used to solve the double-spend problem in currency allowed for this to be used as a currency. It also came with many benefits, like introducing new concepts and the usage of proof-of-work to reach consensus.

Later, came Ethereum, a Smart Contract Platform, that introduced the public to smart contracts, programs that can be run on chain and verified by decentralization. This project proved to be beneficial to many.

In the storage realm, ideas like IPFS, Arweave, Filecoin and others began to introduce a new market for data storage. This data could be permentantly or temporarily stored on the chain and secured by hash functions through the use of blocks, or in IPFS's case, just hash functions. These came with limitations as requiring monetary incentives to be used.

Nano introduced a concept that uses Proof-of-Work as spam protection, as a unsigned-integer of 64 bytes against a certain threshold, allowing for new concepts to arise.

## 1.1 Inspiration

This project was inspired by:

- Bitcoin (Blockchain)
- IPFS (Storage)
- Git (Version Control Management)
- Arweave (Storage)
- Nano (Proof-of-Work)
- Solana (Proof-of-History)

## 2. Immutable Storage Solution

## 2.1 Pieces

In the immutable storage solution, each **piece** is one of the following -> {4kb,16kb,256kb} with 256kb being the most common for larger files.

## 2.2 Storage Solution

Each chain has the following options:

- u4 (4-bit space) (0x0-0xF)
- u8 (1-byte space) (0x00-0xFF)
- u16 (2-byte space) (0x0000-0xFFFF)

## 2.3 MiniaturePoW

nano-inspired proof-of-work using an unsigned 64-bit integer is employed against a certain threshold to protect against spam and ddos attacks. These can easily be verified by the user making sure the piece has had enough proof-of-work put in.
