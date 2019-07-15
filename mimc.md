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

# Third-Party Analysis
Since its publication in 2016, no attack on full-round MiMC was found. The only third-party analysis published regards an [interpolation attack on reduced-round MiMC in a low-memory scenario](https://eprint.iacr.org/2019/812.pdf){:target="_blank"}.