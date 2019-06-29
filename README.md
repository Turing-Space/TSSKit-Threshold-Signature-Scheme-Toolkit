# TSSKit: Threshold Signature Scheme Toolkit
![](https://img.shields.io/badge/Funds-Binance%20Labs-yellow.svg)
![](https://img.shields.io/badge/Grants-Gitcoin-green.svg)
![](https://img.shields.io/badge/Build-Turing%20Chain-red.svg)

![](https://imgur.com/iJbwYW6.png)


## Table of Contents 
- [Description](##Description)

## Description
TSSKit automatically selects the appropriate Threshold Signature Scheme based on a set of options required by the secret sharing needs of each application.   This comprehensive list of options includes private key splitting, multisig detection, HD derivation, signer privacy, and signature size, etc.

TSSKit also generates a set of ready-to-use codebase/scripts that are optimized based on a set of specified parameters.

> Welcome to create any number of pull requests to contribute more codebases that we've missed. BUIDL!

**Active curators: [yhuag](https://github.com/yhuag) and [tina1998612](https://github.com/tina1998612)**

## Types fo Schemes
- Shamir's Secret Sharing (SSS)
- Threshold ECDSA
- Threshold Ed25519
- Schnorr Signatures
- BLS Signatures

## Options
| Option                    | Choice                    |
| ------------------------- | ------------------------- |
| Private Key Splitting     | True / False              |
| Multi-signature Detection | True / False              |
| HD Derivation             | True / False              |
| Weight                    | True / False              |
| Signer Privacy            | True / False              |
| Signature Size            | Linear Growth / Constant  |
| Key Generation Time       | Linear Growth / Constant  |
| Key Generation Round      | Value                     |
| Key Generation Role       | Single Party / DKG Scheme |
| Verification Time         | Strict / Relax            |
| Signing Time              | Strict / Relax            |
| Signing Round             | Value                     |
| Curve                     | Curve Choice              |

> Free to create pull request to add more

## Conceptual Comparisons across Schemes

<table>
  <tr>
    <td></td>
    <td>t-ECDSA</td>
    <td>t-Schnorr</td>
    <td>Ed25519</td>
    <td>BLS</td>
  </tr>
  <tr>
    <td><b>Variants</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Has non-threshold variant</td>
    <td>✔︎</td>
    <td>✔︎</td>
    <td>✔︎

</td>
    <td>✘
</td>
  </tr>
  <tr>
    <td><b>Curve</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Curve Family</td>
    <td>Elliptic</td>
    <td>Elliptic</td>
    <td>Twisted Edwards</td>
    <td>Pairing-friendly</td>
  </tr>
  <tr>
    <td><b>Signature</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Size (bytes)</td>
    <td>71 - 75</td>
    <td>64</td>
    <td>64</td>
    <td>33</td>
  </tr>
  <tr>
    <td>Aggregation</td>
    <td>X</td>
    <td>Entire multi-sig</td>
    <td>Entire multi-sig (variant)</td>
    <td>Entire block</td>
  </tr>
  <tr>
    <td>Format</td>
    <td>Pair</td>
    <td>Pair</td>
    <td>Pair</td>
    <td>Single Curve Point</td>
  </tr>
  <tr>
    <td>Multisignature Differentiable</td>
    <td>✔︎</td>
    <td>✘</td>
    <td>✘</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td><b>Signing</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Time Complexity</td>
    <td>High</td>
    <td>Medium</td>
    <td>Low</td>
    <td>Low</td>
  </tr>
  <tr>
    <td>Interaction Rounds</td>
    <td>Multiple</td>
    <td>Two</td>
    <td>Three</td>
    <td>✘</td>
  </tr>
  <tr>
    <td><b>Verifying</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Verification Targets</td>
    <td>Separately</td>
    <td>Aggregated</td>
    <td>Batch / Single</td>
    <td>Aggregated</td>
  </tr>
  <tr>
    <td>Time Complexity</td>
    <td>Medium</td>
    <td>Low</td>
    <td>Low</td>
    <td>High</td>
  </tr>
  <tr>
    <td><b>Block</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Block Capacity Usage</td>
    <td>Large </td>
    <td>Medium </td>
    <td>Medium</td>
    <td>Small </td>
  </tr>
  <tr>
    <td>Block Content</td>
    <td>Signature + Public Key + Data</td>
    <td>Several Combined Signatures + Public Key + Data</td>
    <td>Several Combined Signatures + Public Key + Data</td>
    <td>One Aggregated Signature + Public Key + Data</td>
  </tr>
  <tr>
    <td><b>Randomness</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Random Number Generator (k)</td>
    <td>Deterministic</td>
    <td>Strictly Dependent</td>
    <td>Deterministic</td>
    <td>Not Required</td>
  </tr>
  <tr>
    <td>New Randomness Consumption</td>
    <td>Key Generation, Signing</td>
    <td>Key Generation, Signing</td>
    <td>Key Generation</td>
    <td>Not Required</td>
  </tr>
  <tr>
    <td><b>Setup</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Key Generation</td>
    <td>DKG</td>
    <td>DKG</td>
    <td>DKG</td>
    <td>Membership</td>
  </tr>
  <tr>
    <td>Key Storage</td>
    <td>N/A</td>
    <td>Merkle Tree (Verifying)</td>
    <td>N/A</td>
    <td>Pre-generate all the keys (Signing)</td>
  </tr>
  <tr>
    <td>Space Complexity</td>
    <td>Low</td>
    <td>High</td>
    <td>Low</td>
    <td>Positively correlated with the number of signing cycles</td>
  </tr>
  <tr>
    <td>Time Complexity</td>
    <td>High </td>
    <td>Medium</td>
    <td>Low</td>
    <td>High</td>
  </tr>
  <tr>
    <td>Time Bottleneck</td>
    <td>The curve used for generating key public / private pairs</td>
    <td>1. The curve used for generating key public / private pairs
1. n and m for merkle tree </td>
    <td>Random Number Generator</td>
    <td>Takes time to generate membership keys</td>
  </tr>
  <tr>
    <td><b>Security</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Hash Collision Resilience</td>
    <td>Low</td>
    <td>High</td>
    <td>High</td>
    <td>N/A</td>
  </tr>
  <tr>
    <td>Side-channel Attack Resilience</td>
    <td>Low</td>
    <td>High (variant)</td>
    <td>High</td>
    <td>High</td>
  </tr>
  <tr>
    <td>Other Possible Attacks</td>
    <td>Secp112r1 Leakage Attacks,
Weak RNG Attacks</td>
    <td>Rogue Key Attacks</td>
    <td>Single Fault Attacks</td>
    <td>MOV Attacks, Rogue Key Attacks</td>
  </tr>
  <tr>
    <td><b>Hashing</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Hash Output</td>
    <td>Number</td>
    <td>Number</td>
    <td>Number</td>
    <td>Curve Point</td>
  </tr>
  <tr>
    <td><b>Privacy</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Public Key</td>
    <td>Revealed</td>
    <td>Hidden</td>
    <td>N/A</td>
    <td>N/A</td>
  </tr>

  <tr>
    <td><b>Codebase</b></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>Javascript</td>
    <td> 
- Bitchain (npm / non-threshold): https://github.com/bitchan/eccrypto

- Elliptic (npm / non-threshold): https://www.npmjs.com/package/elliptic

</td>
    <td>Hidden</td>
    <td>N/A</td>
    <td>N/A</td>
  </tr>
</table>

## Multi Signature vs Threshold Signature
|                                                                                                      | Multi-sig                                                                                                  | Threshold-sig                                                      |
| ---------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| Relationship between (number of signers) and  (signature length, generation time, verification time) | Scales linearly                                                                                            | Independent                                                        |
| Reveal the identities of signers                                                                     | Yes                                                                                                        | No                                                                 |
| Signature verification                                                                               | Use all public keys                                                                                        | Use a unique fixed public key                                      |
| Can do m-out-of-n signing                                                                            | Yes                                                                                                        | Yes                                                                |
| Signature is composed of                                                                             | Concatenation of ( description of the subgroup + regular signatures computed by each member’s secret key ) | Regular signatures computed by all members' aggregated private key |

### References
1. https://bitcoin.stackexchange.com/questions/50836/multi-signature-public-key-validation 
2. https://www.iacr.org/archive/pkc2003/25670031/25670031.pdf 