
# Supercell Generator

## Manual

### Background

In solid-state physics and crystallography or materials science, a crystal structure is described by a unit cell. There are an infinite number of unit cells with different shapes and sizes which can describe the same crystal.  The supercell S of unit cell U is a cell which describes the same crystal, but has larger volume than cell U. Supercells are usually needed to compute more complex materials properties such as crystal defects to allow the use of periodic boundary conditions. 

This utility tool helps to create supercell from unit cell.

### The Method

The generator is implemented using the pacakge Supercell Program [^1]. The program includes algorithms for structure manipulation, supercell generation, permutations of atoms and vacancies, charge balancing, detecting symmetry-equivalent structures, electrostatic energy calculations and sampling output derivative structures. The software works with CIF files, therefore it is compatible with most of DFT software (VASP , CASTEP , Wien2k  etc)



### Using the Generator

#### Entering Input

Practically, the procedure for getting predictions consists in 3 steps

1. Upload a cif structure file

2. Set the supercell dimensions in the format of 2,2,2, indicating X,Y,Z directions repeats of unit cells.

3. Download the cif file.



### Citations

To cite the Generator App, please reference the following works:
- Okhotnikov, K., Charpentier, T., & Cadars, S. (2016). Supercell program: a combinatorial structure-generation approach for the local-level modeling of atomic substitutions and partial occupancies in crystals. Journal of Cheminformatics, 8(1), 17
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).

[^1]: Okhotnikov, K., Charpentier, T., & Cadars, S. (2016). Supercell program: a combinatorial structure-generation approach for the local-level modeling of atomic substitutions and partial occupancies in crystals. Journal of Cheminformatics, 8(1), 17


### Authors

- Dr. Hu
