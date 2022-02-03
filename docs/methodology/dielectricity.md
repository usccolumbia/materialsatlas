# Dielectric datasets of Materials Project database

## Introduction [^2]

A dielectric is a material that can be polarized by an applied electric
field. This limits the dielectric effect to materials with a non-zero
band gap. The mathematical description of the dielectric effect is a
tensor constant of proportionality that relates an externally applied
electric field to the field within the material. Along with the
elastic and piezoelectric tensors, the dielectric tensor provides all
the information necessary for the solution of the constitutive equations
in applications where electric and mechanical stresses are coupled.

The dielectric tensors from the Materials Project (MP) are calculated
from first principles Density Functional Perturbation Theory (DFPT) [^1]
and are approximated as the superimposed effect of an electronic and
ionic contribution. From the full piezoelectric tensor, several
properties are derived such as the refractive index and potential for
ferroelectricity. Just as with the piezoelectric and elastic constants,
multiple consistency checks are performed on all the calculated
dielectric data to ensure its reliability and accuracy.

![Benchmarking DFPT dielectric constants](/methodology/img/dielectricity/Dielectric_benchmarking.png)

## Citation

To cite the dielectric properties within the Materials Project, please
reference the following work:

- Benchmarking density functional perturbation theory to enable
  high-throughput screening of materials for dielectric constant and
  refractive index. Ioannis Petousis, Wei Chen, Geoffroy Hautier, Tanja
  Graf, Thomas D. Schladt, Kristin A. Persson, and Fritz B. Prinz. Phys.
  Rev. B 93(11). [DOI:10.1103/PhysRevB.93.115151](https://doi.org/10.1103/PhysRevB.93.115151)

- High-throughput screening of inorganic compounds for the discovery of
  novel dielectric and optical materials. Ioannis Petousis, David
  Mrdjenovich, Eric Ballouz, Miao Liu, Donald Winston, Wei Chen, Tanja
  Graf, Thomas D. Schladt, Kristin A. Persson, and Fritz B. Prinz.
  Scientific Data 4. [DOI:10.1038/sdata.2016.134](https://doi.org/10.1038/sdata.2016.134)

These papers present the results of our dielectric constant-calculations
for the first batch of 1,056 compounds. Our DFT-parameters, the
workflow, the workflow filters used for detecting anomalies in the
calculations and comparison to experiments are described in detail.

## Authors

1. Shyam Dwaraknath
2. Ioannis Petousis

## References

[^1]:
    Baroni, Giannozzi S. P. and Testa, A. Phys. Rev. Lett. 58, 1861
    (1987)

[^2]:https://docs.materialsproject.org/methodology/dielectricity/
    
[^27]:
    A. Dal Corso, S. Baroni, and R. Resta, Phys. Rev. B 49, 5323
    (1994).

[^28]:
    W. G. Aulbur, L. Jönsson, and J. W. Wilkins, Phys. Rev. B 54,
    8540 (1996).

[^29]:
    Ph. Ghosez, X. Gonze, and R. W. Godby, Phys. Rev. B 56, 12811
    (1997).

[^30]:
    V. Olevano, M. Palummo, G. Onida, and R. Del Sole, Phys. Rev. B
    60, 14224 (1999).
