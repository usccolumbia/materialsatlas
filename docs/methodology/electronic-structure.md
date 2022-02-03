# Electronic Structure Calculations

## Band Structure and DOS computations details

We used the relaxed structure from the total energy run to perform using
the same GGA functional (and U if any) a DOS and band structure run.
This data is available for many entries in
the materials explorer. We ran first a static run with a uniform
(Monkhorst Pack or $\Gamma$-centered for hexagonal systems) k-point grid.
From this run the DOS and the charge density were extracted. The charge
density was then used to perform a band structure computation for
k-points along the symmetry lines of the Brillouin zone. The symmetry
lines have been determined following the methodology from Curtarolo et
al.[^1] using the aconvasp software.

The band structure data is displayed with full lines for up spin and
dashed lines for down spin. For insulators, the band gap is computed
according to the band structure. The nature of the gap (direct or
undirect) as well as the k-points involved in the band gap transition
are displayed. The VBM and CBMs are displayed for insulators as well by
red and white dots. The web site does not display the 10% highest bands
as those higher energies bands tend to converge more slowly.

The DOS indicates the full DOS by default but projections along atoms or
orbitals are also available through a scroll down menu. Please note that
the DOS data and band structure can be slightly different as the k-point
grid is not the same. For instance, the k-point grid for the DOS might
not include Gamma while the band structure does.


## Citation

To cite the calculation methodology, please reference the following
works:

1. A. Jain, G. Hautier, C. Moore, S.P. Ong, C.C. Fischer, T.
   Mueller, K.A. Persson, G. Ceder., A High-Throughput Infrastructure
   for Density Functional Theory Calculations, Computational Materials
   Science, vol. 50, 2011, pp. 2295-2310.
   [DOI:10.1016/j.commatsci.2011.02.023](https://dx.doi.org/10.1016/j.commatsci.2011.02.023)
2. A. Jain, G. Hautier, S.P. Ong, C. Moore, C.C. Fischer, K.A.
   Persson, G. Ceder, Accurate Formation Enthalpies by Mixing GGA and
   GGA+U calculations, Physical Review B, vol. 84, 2011, p. 045115.
   [DOI:10.1103/PhysRevB.84.045115](https://doi.org/10.1103/PhysRevB.84.045115)

## Authors

1. Anubhav Jain
2. Shyue Ping Ong
3. Geoffroy Hautier
4. Charles Moore

## References

[^1]:
    Setyawan, W.; Curtarolo, S. Computational Materials Science 2010,
    49, 299-312.

[^2]:
    E.N. Brothers, A.F. Izmaylov, J.O. Normand, V. Barone, G.E.
    Scuseria, Accurate solid-state band gaps via screened hybrid
    electronic structure calculations., The Journal of Chemical Physics.
    129 (2008)

[^3]:
    R. Godby, M. Schluter, L.J. Sham, Self-energy operators and
    exchange-correlation potentials in semiconductors, Physical Review
    B. 37 (1988).

[^4]:
    M. Chan, G. Ceder, Efficient Band Gap Predictions for Solids,
    Physical Review Letters 19 (2010)

[^5]:
    J. Heyd, J.E. Peralta, G.E. Scuseria, R.L. Martin, Energy band
    gaps and lattice parameters evaluated with the
    Heyd-Scuseria-Ernzerhof screened hybrid functional, Journal of
    Chemical Physics 123 (2005)

[^6]:
    W. Setyawan, R.M. Gaume, S. Lam, R. Feigelson, S. Curtarolo,
    High-throughput combinatorial database of electronic band structures
    for inorganic scintillator materials., ACS Combinatorial Science.
    (2011).
