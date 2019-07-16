---
layout: home
---

{% include lib/mathjax.html %}

# Introduction
On this website we provide the specifications, codes, documentation and updates about a novel class of block ciphers and hash functions, designed for MPC, zero-knowledge, SNARK and STARK applications. 

## MiMC
MiMC is a family of block ciphers and hash functions primarily designed for SNARK applications. Its simple algebraic structure is advantageous for applications which benefit from a low multiplicative complexity. Details about MiMC can be found [here](https://hadesmimc.github.io/mimc/).

## GMiMC, Starkad and Poseidon
GMiMC borrows MiMC's core component -- a low-degree round function -- and uses it in various unbalanced Feistel constructions. More details about this approach can be found [here](https://hadesmimc.github.io/gmimc/).

While MiMC and GMiMC are defined as block ciphers, Starkad and Poseidon are unkeyed permutations. They are built using a novel SPN approach to further improve the applicability in the use cases mentioned above. Both Starkad and Poseidon a described in more detail [here](https://hadesmimc.github.io/starkad_poseidon/).
