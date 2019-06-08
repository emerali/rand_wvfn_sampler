# rand_wvfn_sampler
Generate samples from a random wavefunction in a given basis, by rotating the wavefunction `psi` into the proper basis and then sampling from the distribution defined by `psi`. 

Wavefunction rotation is performed by efficiently multiplying the vector `psi` by the Kronecker product of the relevant unitary matrices. Refs: [1](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.379.9338&rep=rep1&type=pdf) and [2](https://www.irisa.fr/sage/bernard/publis/Kronecker99.pdf). Algorithm 2 in both papers (the so-called "shuffle algorithm") is the relevant one.

As a result, I am able to generate data for a random 8-qubit wavefunction in every combination of Pauli bases (XYZ) (200 samples per basis combination) in about 11 seconds on my laptop.
