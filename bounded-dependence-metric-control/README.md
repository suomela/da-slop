# From bounded dependence to det-LOCAL

## Context

We study how to turn bounded dependence distributions over locally checkable labeling (LCL) solutions into fast deterministic LOCAL algorithms. 

Graph family: graphs of bounded Assouad-Nagata dimension at most one, and a lower bound on grids for a somewhat weaker definition of bounded dependent distributions.


## New results

- **Polylog n translation.** On bounded-degree graph classes of Assouad-Nagata dimension at most one, a bounded dependence distribution of locality $T$ with global success at least $1-1/n$ gives a deterministic LOCAL algorithm in $O(T\ \mathrm{polylog}\ n)$ rounds, for a fixed LCL and $T\geq 1$. This includes bounded-treewidth and bounded-treelength graph classes.
- **Grid lower bound.** There exists an LCL on grids with non-signaling locality three and dependence two (and 0 error), whose deterministic LOCAL complexity is $\Theta(\sqrt n)$. The distribution has the non-signaling property only on grids. This shows that, if one requires non-signaling only on grids, the first result above cannot be extended to graphs of Assouad-Nagata dimension at least two (as the family of grids has AN-dimension 2).

## Prior work and comparison

[Balliu et al.](https://arxiv.org/abs/2504.05191v2) give a general deterministic simulation in $\widetilde O(\sqrt{nT})$ rounds, with success strictly greater than $1-1/n$. The first result replaces the dependence on $\sqrt n$ by a polylogarithmic factor on AN-dimension 1 classes.

[d'Amore and Lievonen](https://arxiv.org/abs/2608.16854v1) obtain an $O(\log n)$ deterministic bound on trees from subpolynomial bounded dependence. Our translation applies beyond trees, and improves the dependency in $T$, but at the cost of an extra $\mathrm{polylog}\ n$ factor.


## Documents

- [Combined AI-generated write-up](writeup.pdf)
- [LaTeX source](writeup.tex)

## Discovered by

GPT-6 

## Communicated by

Francesco D'Amore and Timothé Picavet.

## Confidence

**H** for both results. We read, verified and understood the proof.

## Assigned to

Francesco D'Amore and Timothé Picavet.
