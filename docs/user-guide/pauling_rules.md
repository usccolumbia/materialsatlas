
# Pauling's Rule Check

## Manual

### Background on Pauling's Rule

The arrangement of atoms in a crystal structure not only depends on the charge on the ion and type of bonding between atoms, but also on the size of the atoms or ions.  In any given molecule or crystal structure each atom or ion will be surrounded by other atoms or ions.  The number of  ions or atoms that immediately surround an atom or ion of interest is called the coordination number,  - C.N.  As we shall see, the coordination number depends on the relative size of the atoms or ions. Linus Pauling studied crystal structures and the types of bonding and coordination that occurs within them.  His studies found that crystal structures obey the following rules, now known as Pauling's Rules [(Check details here)](https://www.tulane.edu/~sanelson/eens211/paulingsrules.htm).  Pauling's rules can be used to evaluate the feasibility of hypothetical materials structures.


Rule #1 - A coordinated polyhedron of anions is formed about each cation, the cation-anion
distance equaling the sum of their characteristic packing radii and the coordination
polyhedron being determined by the radius ratio.

Rule #2 - An ionic structure will be stable to the extent that the sum of the strengths of the 2
electrostatic bonds that reach an anion equal the charge on that anion.

Rule #3 - The sharing of edges and particularly faces by two anion polyhedra decreases the
stability of an ionic structure.

Rule #4 - In a crystal containing different cations, those of high valency and small coordination number tend not to share polyhedron elements with one another.

Rule #5 - The number of essentially different kinds of constituents in a crystal tends to be
small.


Crystal structure and compound prediction is an essential step of computational materials
design. Indeed, while many materials properties can be computed nowadays with _ab-initio_
computations. Those computed properties are only relevant if they are evaluated on a compound (i.e., a
stoichiometry and crystal structure) stable enough to be formed. Crystal structure prediction can be quite useful for experimentalists too.
For instance, when only powder XRD experiments are available after synthesis of a new compound, a theoretical suggestion of a likely structure can tremendously help the structure refinement and determination for example.


### The Method

The Pauling's rule check tool for structures here is implemented using the method as described in the paper "George, Janine, David Waroquiers, Davide Di Stefano, Guido Petretto, Gian‐Marco Rignanese, and Geoffroy Hautier. "The limited predictive power of the pauling rules." Angewandte Chemie 132, no. 19 (2020): 7639-7645". 

The composition based Pauling rule check is implemented using the [Smact](https://smact.readthedocs.io/en/stable/_modules/smact/screening.html#pauling_test) package which can check if a combination of ions makes chemical sense, (i.e. positive ions should be of lower Pauling electronegativity)

### The basic idea

![substitution example](img/structure-predictor/substitution-example.png)
_Figure 1: An example of ionic substitution._


![ionic substitution correlations](img/structure-predictor/ions-correlation.png)
_Figure 2: Data mined tendency for ionic substitutions.
Red indicates high substitution tendency.
Blue indicates that the tow ions tend to not substitute._



![substitution flowchart](img/structure-predictor/substitution-flowchart.png)
_Figure 3: Procedure for proposing new compound candidates in a quaternary system using the ionic substitution probability._



### Performance and Limitations

### Using the Pauling's Rule Check Tool

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Enter a formula/composition

2. or upload a cif structure file

3. Start the prediction: click 'Check Now' to begin the validation process.
   
4. Examine results: Upon completion of the task, you will be given a link to 

#### Interpreting the Results


<!-- The results pages provides a set of structure id's corresponding to the candidate structures.
A link is provided for each structure id, which provides structure visualization, lattice vectors, atomic positions, and simulated x-ray spectra.
Cif and POSCAR files for each candidate can be downloaded.
Typically, the candidates need to be tested for stability against each other (seeing what is the lowest energy structure amongst the candidates at a given composition) but also against other phases known in nature.
For instance, if a AB compound is proposed and its energy is higher than a combination of half A<sub>2</sub>B and half AB<sub>2</sub>.
This stability analysis can be performed using the convex hull construction that will effectively test the stability of the phases against each other and come with a set of stable phases that are on the hull.
Figure 4 shows a convex hull (in green) for an A-B system.
Blue points indicate phases that are not on the hull and therefore unstable and red points indicate stable phases.
For instance, the construction shows directly that the phase γ at AB will decompose into α<sub>1</sub> and β<sub>2</sub>.

![convex hull example](img/structure-predictor/convex-hull.png)
_Figure 4: An example of the convex hull construction._

More information about phase stability and convex hull can be obtained in the [phase diagram app manual](phase-diagram.md).

Please note that we only presented an approach for building zero K, zero pressure phase diagrams.
It is possible to use the candidates proposed by the model to perform more advanced stability studies for instance at finite temperature.
This is more expensive computationally though as the different entropy components (configuration, vibration, etc...) need to be taken into account.

Finally, as we present a usage of our candidates for computations, an experimentalist can also use these candidates to test different structures versus a powder diffraction pattern. -->

### Future features


<!-- In the future, we want to give the user the option to perform substitution of several ions for one ion in a starting structure.
For instance, if one is interested in ternary oxychlorides (M, O<sup>2-</sup>, Cl<sup>1-</sup>) there will be only few ternary compounds that will be good candidates for a substitution generating oxychlorides (e.g., oxybromides).
A strategy to increase the pool of possible structure is to allow substitution of one ion by O<sup>2-</sup> and Cl<sup>-</sup>.
For instance, we would start with an oxide and substitute the O<sup>2-</sup> by a mixture of O<sup>2-</sup> and Cl<sup>-</sup>.
The amount of O and Cl will be set to achieve charge balance and a simple model (electrostatics or other) could be used to pick an ordering of the two substituted species.

The only data mined model accessible now is the substitution predictor.
We have developed another model based on correlations between crystal structures at different compositions.[^3][^4] We plan to give access to this model in the future.
The two models are complimentary: the model based on correlations between structure is more efficient in data rich regions (e.g., ternary oxides) while the ionic substitution model is more efficient in data sparse regions (e.g., quaternaries). -->

### Citations

To cite the Pauling rule check App, please reference the following works:

- George, Janine, David Waroquiers, Davide Di Stefano, Guido Petretto, Gian‐Marco Rignanese, and Geoffroy Hautier. "The limited predictive power of the pauling rules." Angewandte Chemie 132, no. 19 (2020): 7639-7645.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).

[^1]: https://github.com/QuantumLab-ZY/PAMCARS
[^2]: https://www.science.smith.edu/geosciences/min_jb/PaulingRules.pdf
[^3]: https://www.tulane.edu/~sanelson/eens211/paulingsrules.htm
[^4]: https://github.com/JaGeo/PaulingPublication

### Authors

- Jianjun Hu
- Lai Wei
