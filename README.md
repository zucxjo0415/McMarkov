# McMarkov
Python code to compute critical exponents / Hausdorff dimensions of limit sets $`\delta`$ and conformal densities using McMullen's eigenvalue algorithm. 

Algorithm to estimate critical exponent using expanding Markov partition is from McMullen's paper ["Hausdorff dimension and conformal dynamics III: Computation of dimension"](https://people.math.harvard.edu/~ctm/papers/home/text/papers/dimIII/dimIII.pdf).

Algorithm to estimate conformal density (of dimension = critical exponent) is from Gittins--Peyerimhoff--Stociu--Wirosoetisno, ["Some spectral applications of McMullen's Hausdorff dimension algorithm"](https://arxiv.org/pdf/1112.1020) (see Section 3.2).

We remark that these papers, at least in their titles, refer to Hausdorff dimension of limit sets and not critical exponents. For convex cocompact and geometrically finite Kleinian groups, this Hausdorff dimension is equal to the critical exponent. More generally, what McMullen's algorithm actually computes is the dimension of a conformal density. For Kleinian groups of divergent type (including convex cocompact and geometrically finite Kleinian groups), any conformal density has dimension equal to the critical exponent. 

## Dependencies
The code implementing the algorithm uses `numpy`, as well as `scipy.optimize.bisect` to numerically find the approximants for $\delta$ (Step 3 in McMullen's eigenvalue algorithm, see p.6 of [paper]((https://people.math.harvard.edu/~ctm/papers/home/text/papers/dimIII/dimIII.pdf)).)

The demo notebook uses parts of [Teddy Weisman's `geometry_tools` package](https://public.websites.umich.edu/~tjwei/geometry_tools/geometry_tools.html) to specify and compute with Fuchsian representations and visualize their orbits in the hyperbolic plane.

## Future work

### More examples
- Demo with a family of Fuchsian examples, not just one (may start by looking at examples in McMullen and in Gittins--Peyerimhoff--Stociu--Wirosoetisno)
- Demo with Kleinian example/s (ditto)
- Think about implementation for convex projective examples
- Potentially other groups of divergent type admitting conformal densities

### Efficiency improvements
- Implement some of the efficiencies described by McMullen under "Practical considerations" on p.8 of [his paper](https://people.math.harvard.edu/~ctm/papers/home/text/papers/dimIII/dimIII.pdf), in particular (4) adaptive refinement of partitions, (5) sparse matrix storage, and (6) computation of derivatives using affine charts.

### Code to compute Markov partitions

### Self-contained Python code + API documentation
