---
layout: page
title: Starkad and Poseidon
permalink: /starkadposeidon/
---

# Introduction
Both Starkad and Poseidon are hash functions based on the permutations Starkad\\(^\pi\\) and Poseidon\\(^\pi\\) using a new design strategy called Hades. In contrast to classical SPN ciphers (e.g., Shark) and partial SPN (P-SPN) ciphers (e.g., LowMC), Hades makes use of rounds applying the nonlinear transformation to the whole state and rounds applying it only to part of the state. The main idea of this approach is to facilitate cryptanalysis regarding statistical attacks, while at the same time reducing the total number of expensive operations in the target use cases.

All details about these hash functions can be found [in the paper](https://eprint.iacr.org/2019/458){:target="_blank"}.