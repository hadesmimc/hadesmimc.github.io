---
layout: page
title: MiMC
permalink: /mimc/
---

{% include lib/mathjax.html %}

# Description

MiMC is block cipher and hash function family designed specifically for SNARK applications. The low multiplicative complexity of MiMC over prime fields makes it suitable for ZK-SNARK applications such as ZCash.

The core component of MiMC is the function $$ f(x) = x^3 $$. The computation of this function takes place in \\(\mathbb{F}_q\\), where \\(q = p\\) or \\(q = 2^n\\) for a prime number \\(p\\) and a natural number \\(n\\). 

There exist two variants of MiMC, namely MiMC-\\(n/n\\) (or MiMC-\\(p/p\\) for prime fields) and MiMC-\\(2n/n\\) (or MiMC-\\(2p/p\\) for prime fields), where the latter is built using a Feistel construction.

For an \\(n\\)-bit key, the key scheduling adds the same \\(n\\)-bit key at each round and is followed by the round constant addition. For a \\(2n\\)-bit key, the two \\(n\\)-bit keys are added alternately.

The precise definition of the round function of MiMC and all other details can be found [in the paper](https://eprint.iacr.org/2016/492.pdf){:target="_blank"}.

# Implementations
Reference implementations are available for both the block cipher and the hash function in a sponge mode. The block cipher uses a block size of 129 bits, where computations take place in \\(\mathbb F_{2^n}\\), and the permutation in the sponge mode uses a block size of \\(r + c = 769 bits\\), where \\(r = 512\\) and \\(c = 257\\). All resources, together with a script to create round constants using the [Grain LFSR][1], can be found [in our repository](https://extgit.iaik.tugraz.at/krypto/mimc/tree/master/code/implementations){:target="_blank"}.

All resources can be found in our repository. https://extgit.iaik.tugraz.at/krypto/mimc/tree/master/code

# Third-Party Analysis
Since its publication in 2016, no attack on full-round MiMC has been found. The only third-party analysis published regards an [interpolation attack on reduced-round MiMC in a low-memory scenario](https://eprint.iacr.org/2019/812.pdf){:target="_blank"}.

# Use Cases
Due to its simple structure and absence of any attacks since its publication, MiMC has been considered to be used in various scenarios which benefit from its algebraic structure. For example, it can be used as a verifiable delay function ([2], [3]). It is also currently being evaluated as a candidate for Zcash [4].


[1]: https://www.ecrypt.eu.org/stream/ciphers/grain/grain.pdf
[2]: https://eprint.iacr.org/2018/601.pdf
[3]: https://vitalik.ca/general/2018/07/21/starks_part_3.html
[4]: https://github.com/zcash/zcash/issues/2233