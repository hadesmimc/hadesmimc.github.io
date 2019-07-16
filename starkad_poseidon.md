---
layout: page
title: Starkad and Poseidon
permalink: /starkadposeidon/
---

# Introduction
Both Starkad and Poseidon are hash functions based on the permutations Starkad\\(^\pi\\) and Poseidon\\(^\pi\\) using a new design strategy called Hades. In contrast to classical SPN ciphers (e.g., Shark) and partial SPN (P-SPN) ciphers (e.g., LowMC), Hades makes use of rounds applying the nonlinear transformation to the whole state and rounds applying it only to part of the state. The main idea of this approach is to facilitate cryptanalysis regarding statistical attacks, while at the same time reducing the total number of expensive operations in the target use cases.

All details about these hash functions can be found [in the paper](https://eprint.iacr.org/2019/458).

# Implementations
Multiple reference implementations for the unkeyed permutations are available [here](https://extgit.iaik.tugraz.at/krypto/hadeshash).

# Applications
Poseidon is already implemented in the context of Zcash's "Sapling" upgrade [[1]][1] and zero-knowledge proofs with Bulletproofs ([[2]][2], [[3]][3]).

[1]: https://github.com/matter-labs/sapling-crypto/tree/hades
[2]: https://github.com/lovesh/bulletproofs-r1cs-gadgets
[3]: https://github.com/dusk-network/poseidon252
