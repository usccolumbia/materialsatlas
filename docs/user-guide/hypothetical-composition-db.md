
# Hypothetical Materiasl Composition Database
#### by Jianjun Hu

## Manual

### Background

Crystal structure and compound prediction is an essential step of computational materials
design.
Indeed, while many materials properties can be computed nowadays with _ab-initio_
computations.
Those computed properties are only relevant if they are evaluated on a compound (i.e., a
stoichiometry and crystal structure) stable enough to be formed.
Crystal structure prediction can be quite useful
for experimentalists too.
For instance, when only powder XRD experiments are available after synthesis of a new compound, a theoretical suggestion of a likely structure can tremendously help the structure refinement and determination for example.

The most common approach in the field of crystal structure prediction is to treat it as an optimization problem. [^1]
Researchers use optimization algorithms to search for the minimum of the relevant thermodynamic potential (e.g., the energy at 0 K, 0 atm) by varying the crystal's degrees of freedom (lattice constants, atomic positions).
This optimization is extremely challenging as the energy landscape is very rugged and full of local minima.
Very computationally expensive advanced optimization techniques (e.g., simulated annealing and genetic algorithm) are usually necessary to tackle this optimization problem.

In a departure to this traditional approach, the methods we have developed use a combination of data mining and _ab-initio_ computations in the density functional theory (DFT) framework to tackle this problem with a limited computational budget.
The basic idea is to learn the chemical rules governing phase stability from a database of experimentally known compounds.
Embedding those rules in a mathematical model, we can predict what are the most likely compounds to form in a given chemical system.
Finally, the last step consists of testing those candidates for stability using _ab-initio_ computations ([see Phase Diagram](phase-diagram.md)).

### The Generation of New Materials Recipes/Compositions Method

The compound prediction model available on the Materials Project now, through the structure predictor app, is based on our recent work on the data mining of ionic substitutions.
In this section we will briefly explain the idea of the approach and how to use the explorer.
More details can be found in Hautier et al.[^2]

### The basic idea

![substitution example](img/structure-predictor/substitution-example.png)
_Figure 1: An example of ionic substitution._



### The compound generation procedure

The product of our data mining approach is a probability function indicating how likely is a specific set of ionic substitutions.
The model we used was inspired by previous work in the field of machine translation.
In this field, it is the probability for a word in one language to be able to be substituted by a word in another language.
In our case, we substitute ions rather than words.
After we built this probability function, from a database of experimental data (here the ICSD), we can perform compound predictions.
Figure 3 illustrates the procedure for 4 ions (but this can be generalized to any number of species).
Targeting a specific combination of 4 ions (e.g., Ba<sup>2+</sup>, Fe<sup>3+</sup>, La<sup>3+</sup>, O<sup>2-</sup> ), we look for any substitution from known compounds (in the ICSD) that have a high enough probability to be likely to form a new stable compound.
If the substitution is higher than a certain threshold we keep it as a possible candidate, otherwise we discard it and go to the next ICSD compound.
There is also a check to make sure we do not form duplicate structures and only predict charge balanced compounds.

![substitution flowchart](img/structure-predictor/substitution-flowchart.png)
_Figure 3: Procedure for proposing new compound candidates in a quaternary system using the ionic substitution probability._

From this procedure, we can see that the threshold set is quite important.
A higher threshold will give you less false positives (suggested compounds that are not stable), but also less true positives.
On the other hand, too low a threshold will give more true positives, but consequently, more false positives.
There is a compromise to find between how exhaustive you want to be and how many candidates you can have, in terms of computational budget (that you will have to test down the road for stability using DFT).

### Performance and Limitations

### Using the Structure Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Pick elements: Select on the periodic table what constituent elements comprise the chemical space you are interested in.
   For instance if you want to make predictions for battery materials based on Li, Mn and O, you should pick those three elements.

2. Pick oxidation states: The model uses the oxidation states to make predictions.
   V<sup>3+</sup> does not substitute with the same elements as V<sup>5+</sup>, so if you want to study Mn<sup>3+</sup> compounds, you should pick +3 for Mn, +1 for Li (no other choices anyway) and -2 for O.
   Sometimes you do not know what oxidation states you are interest in.
   Let say you want all Li-Mn-O compounds regardless of the oxidation state of Mn.
   Then, I would suggest running the model several times, one for Mn<sup>2+</sup>, one for Mn<sup>3+</sup>, and lastly one for Mn<sup>4+</sup>.
   This should cover all the chemical space you are looking at.

3. Start the prediction: click 'Predict Structure' to begin the prediction.
   Predictions are not immediately available and will require some time to complete.
   You can monitor the status of your request in the [dashboard](https://materialsproject.org/dashboard).

4. Examine results: Upon completion of the task, you will be given a link to a landing page providing details on the candidate structures.
   We also provide cif files for the predicted compounds as well as VASP files ready to be run with standard parameters.
   We do not provide any DFT results due our limited computational budget for the moment.
   It is the responsibility of the user to run the predictions.
   Also, as the pseudopotentials are proprietary in VASP (POTCARs) we do not provide those but a script is sent along that can be run to make sure the POTCARs are built from a directory containing all pseudopotentials.

#### Interpreting the Results



### Future features

To add more information to the hypothetical materials compositions, machine learning models of materials properties will be applied to the data entries to calculate their computed physical and chemical properties.

### Citations

To cite the Structure Predictor App, please reference the following works:

- G. Hautier, V. Ehrlacher, C.C. Fischer, A. Jain, G. Ceder, Data Mined Ionic Substitutions for the Discovery of New Compounds, Inorganic Chemistry, vol. 50, 2011, pp. 656-663.
- A. Jain, G. Hautier, C. J. Moore, S. P. Ong, C. C. Fischer, T. Mueller, K. A. Persson, and G. Ceder, A high-throughput infrastructure for density functional theory calculations, Computational Materials Science, vol. 50, 2011, pp. 2295-2310.

[^1]: 10.1038/nmat2321
[^2]: 10.1021/ic102031h
[^3]: 10.1021/cm100795d
[^4]: 10.1038/nmat1691

### Authors

- Geoffroy Hautier
- Anubhav Jain
