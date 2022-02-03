# Elasticity of Materials

## Introduction [^1]

The elastic constants from the Materials Project (MP) are calculated
from first principles Density Functional Theory (DFT). The process is
started by performing an accurate structural relaxation for each
structure, to a state of approximately zero stress. Subsequently,
perturbations are applied to the lattice vectors and the resulting
stress tensor is calculated from DFT, while allowing for relaxation of
the ionic degrees of freedom. Finally, constitutive relations from
linear elasticity, relating stress and strain, are employed to fit the
full 6x6 elastic tensor. From this, aggregate properties such as Voigt
and Reuss bounds on the bulk and shear moduli are derived. Multiple
consistency checks are performed on all the calculated data to ensure
its reliability and accuracy.


## Derived elastic properties

 elastic tensor, Voigt, Reuss and Voigt-Reuss-Hill [^2]
bounds on the bulk and shear moduli for polycrystalline materials, the elastic anisotropy index and isotropic Poisson ratio
.

| Property                              | Unit       | Description                                                                                                          | Equation                                                                                                                  |
| ------------------------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| Elastic tensor, $C_{ij}$              | GPa        | Tensor, describing elastic behavior, corresponding to IEEE orientation, symmetrized to crystal structure             | see main text                                                                                                             |
| Elastic tensor (original), $C_{ij}$   | GPa        | Tensor, describing elastic behavior, unsymmetrized, corresponding to POSCAR (conventional standard cell) orientation | see main text                                                                                                             |
| Compliance tensor, $s_{ij}$           | GPa$^{-1}$ | Tensor, describing elastic behavior                                                                                  | $s_{ij} = C_{ij}^{-1}$                                                                                                    |
| Bulk modulus Voigt average, $K_{V}$   | GPa        | Upper bound on $K$ for polycrystalline material                                                                      | $9K_{V}=\left(C_{11}+C_{22}+C_{33}\right) + 2\left(C_{12}+C_{23}+C_{31}\right)$                                           |
| Bulk modulus Reuss average, $K_{R}$   | GPa        | Lower bound on $K$ for polycrystalline material                                                                      | $1 / K_{R} = \left(s_{11}+s_{22}+s_{33}\right) + 2\left(s_{12}+s_{23}+s_{31}\right)$                                      |
| Shear modulus Voigt average, $G_{V}$  | GPa        | Upper bound on $G$ for polycrystalline material                                                                      | $15 G_{V} = \left(C_{11}+C_{22}+C_{33}\right)-\left(C_{12}+C_{23}+C_{31}\right) + 3\left(C_{44}+C_{55}+C_{66}\right)$     |
| Shear modulus Reuss average, $G_{R}$  | GPa        | Lower bound on $G$ for polycrystalline material                                                                      | $15 / G_{R} = 4\left(s_{11}+s_{22}+s_{33}\right)-4\left(s_{12}+s_{23}+s_{31}\right) + 3\left(s_{44}+s_{55}+s_{66}\right)$ |
| Bulk modulus VRH average, $K_{VRH}$   | GPa        | Average of $K_{R}$ and $K_{V}$                                                                                       | $2 K_{VRH} = \left(K_{V} + K_{R} \right)$                                                                                 |
| Shear modulus VRH average, $G_{VRH}$  | GPa        | Average of $G_{R}$ and $G_{V}$                                                                                       | $2 G_{VRH} = \left(G_{V} + G_{R} \right)$                                                                                 |
| Universal elastic anisotropy, $A^{U}$ | -          | Description of elastic anisotropy                                                                                    | $A^{U} = 5 \left(G_{V}/G_{R}\right) + \left(K_{V}/K_{R}\right) -6 \geq 0$                                                 |
| Isotropic Poisson ratio, $\mu$        | -          | Number, describing lateral response to loading                                                                       | $\mu = \left(3K_{VRH} - 2G_{VRH}\right)$ / $\left(6K_{VRH} + 2G_{VRH}\right)$                                             |



## Citation

To cite the elastic constants within the Materials Project, please
reference the following work:

- de Jong M, Chen W, Angsten T, Jain A, Notestine R, Gamst A, Sluiter M, Ande CK, van der Zwaag S, Plata JJ, Toher C, Curtarolo S, Ceder G, Persson KA, Asta M (2015) Charting the complete elastic properties of inorganic crystalline compounds. [Scientific Data 2: 150009](http://www.nature.com/articles/sdata20159)


## Authors

1. Maarten de Jong

## References

[^1]: https://docs.materialsproject.org/methodology/elasticity/
