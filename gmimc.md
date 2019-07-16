---
layout: page
title: GMiMC
permalink: /gmimc/
bibliography: references.bib
---

{% include lib/mathjax.html %}

# Description

Similar to the original version of MiMC, GMiMC also uses the function \\(f(x) = x^3\\) as the main component of its construction. However, where MiMC uses a simple encryption path or, alternatively, a balanced Feistel network, GMiMC uses a different approach, namely unbalanced Feistel networks.

The GMiMC family of block ciphers specifies various Feistel constructions, including, for example, the _expanding round function_, which has shown to be the most efficient one in most of our use cases.

All details about GMiMC can be found [in the paper](https://eprint.iacr.org/2019/397){:target="_blank"}.

# Implementations