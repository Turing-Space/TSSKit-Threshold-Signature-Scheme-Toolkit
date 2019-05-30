# TSSKit: Threshold Signature Scheme Toolkit
![](https://imgur.com/iJbwYW6.png)

## Description
TSSKit automatically selects the appropriate Threshold Signature Scheme based on a set of options required by the secret sharing needs of each application.   This comprehensive list of options includes private key splitting, multisig detection, HD derivation, signer privacy, and signature size, etc.

TSSKit also generates a set of ready-to-use codebase/scripts that are optimized based on a set of specified parameters.

> Welcome to create any number of pull requests to contribute more codebases that we've missed. BUIDL!

**Active curators: [yhuag](https://github.com/yhuag) and [tina1998612](https://github.com/tina1998612)**

## Codebases
## ECDSA
#### Javascript
1. Bitchain (npm / non-threshold):  https://github.com/bitchan/eccrypto
2. Elliptic (npm / non-threshold): https://www.npmjs.com/package/elliptic

#### C++
1. kmackay (non threshold): https://github.com/kmackay/micro-ecc

#### C
1. esxgx (non threshold): https://github.com/esxgx/easy-ecc
2. freifunk-gluon (non-threshold): https://github.com/freifunk-gluon/ecdsautils

#### Rust
1. KZen: https://github.com/KZen-networks/multi-party-ecdsa
2. Rust-bitcoin (non-threshold): https://github.com/rust-bitcoin/rust-secp256k1/

#### Go
1. bftkv: https://github.com/yahoo/bftkv/blob/master/crypto/threshold/ecdsa/ecdsa.go

#### Java
1. TwoFactorBtc: https://github.com/citp/TwoFactorBtcWallet/tree/master/EcdsaTwoPartyThresholdSignature/src/main/java/threshold/mr04

#### Python
1. Fernandolobato: https://github.com/fernandolobato/ecc_verifiable_threshold_cryptosystem

2. AntonKueltz: https://github.com/AntonKueltz/fastecdsa

3. warner (non threshold): https://github.com/warner/python-ecdsa

4. SolCrypto (non-threshold): https://github.com/HarryR/solcrypto

#### Swift
1. Sajjon (non-threshold): https://github.com/Sajjon/EllipticCurveKit

## Schnorr
#### Javascript
1. NPM: https://github.com/guggero/bip-schnorr

2. Bcoin: https://github.com/bcoin-org/schnorr

3. guggero (non-threshold): https://github.com/guggero/bip-schnorr

#### C

1. openssh: https://github.com/metacloud/openssh/blob/master/schnorr.c

2. metalicjames: https://github.com/metalicjames/cschnorr

3. OkCupid: https://github.com/OkCupid/sfslite/blob/master/crypt/schnorr.C

#### Rust
1. KZen: https://github.com/KZen-networks/multi-party-schnorr

2. W3f: https://github.com/w3f/schnorrkel

#### Go
1. hbakhtiyor (non-threshold): https://github.com/hbakhtiyor/schnorr

#### Java
1. DimonK95: https://github.com/DimonK95/schnorr-signature

#### Python
1. Yuntai: https://github.com/yuntai/schnorr-examples

2. Vihu: https://github.com/vihu/schnorr-python/blob/master/naive.py

3. SolCrypto (non-threshold): https://github.com/HarryR/solcrypto

## Ed25519
#### Javascript
1. NPM: https://github.com/dazoe/ed25519

2. Substack-Supercop-ref10: https://github.com/substack/ed25519-supercop

3. Ed25519 (npm): https://www.npmjs.com/package/ed25519

4. Ed25519-Supercop (npm): https://www.npmjs.com/package/ed25519-supercop

5. Ed25519-hap (npm): https://www.npmjs.com/package/ed25519-hap

6. Ed25519-hd-key: https://www.npmjs.com/package/ed25519-hd-key

7. Types (npm): https://www.npmjs.com/package/@types/ed25519

#### C++
1. Floodyberry: https://github.com/floodyberry/ed25519-donna

2. MIT DCI: https://github.com/mit-dci/CryptoKernel

#### C
1. Orlp: https://github.com/orlp/ed25519

#### Rust
1. Dalek: https://github.com/dalek-cryptography/ed25519-dalek

#### Go
1. Dcrd: https://github.com/decred/dcrd/blob/master/dcrec/edwards/ecdsa.go

2. Agl: https://github.com/agl/ed25519/blob/master/edwards25519/edwards25519.go

3. Golang: https://github.com/golang/crypto/tree/master/ed25519

#### Java
1. Crypto-rb: https://github.com/crypto-rb/ed25519

2. Str4d: https://github.com/str4d/ed25519-java

#### Python
1. warner (non threshold): https://github.com/warner/python-ed25519

2. official: https://ed25519.cr.yp.to/python/ed25519.py

3. official pip: https://pypi.org/project/ed25519/

## BLS
#### Javascript
1. Difnity (npm): https://github.com/dfinity/js-bls-lib

2. Kfichter: https://github.com/kfichter/solidity-bls

3. bls-signatures (npm): https://www.npmjs.com/package/bls-signatures

#### TypeScript
1. ChainSafe: https://github.com/ChainSafe/bls-js

#### C++
1. Herumi: https://github.com/herumi/bls

2. Leishman: https://github.com/leishman/bls_lib

3. Skale: https://github.com/skalenetwork/libBLS

#### C
1. Chia Network: https://github.com/Chia-Network/bls-signatures

#### Rust
1. Filecoin: https://github.com/filecoin-project/bls-signatures

2. Lovesh: https://github.com/lovesh/signature-schemes

3. Str4d: https://github.com/str4d/bls

#### Go
1. Enzoh: https://github.com/enzoh/go-bls

2. Prysmaticlabs: https://github.com/prysmaticlabs/go-bls

#### Python
1. Asonnino: https://github.com/asonnino/bls

2. pip: https://pypi.org/project/python-bls/

3. bls-lib doc: https://bls-lib.readthedocs.io/en/latest/
