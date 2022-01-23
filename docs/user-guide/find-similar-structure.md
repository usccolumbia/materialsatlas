
# Find Similar Structure
#### Dr. Hu

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

### The Structure Similarity Calculation Method

The compound prediction model available on the Materials Project now, through the structure predictor app, is based on our recent work on the data mining of ionic substitutions.
In this section we will briefly explain the idea of the approach and how to use the explorer.
More details can be found in Hautier et al.[^2]

### The basic idea

![substitution example](img/structure-predictor/substitution-example.png)
_Figure 1: An example of ionic substitution._

It is common for chemists to propose new compounds from the substitution of
another, chemically similar, ion.
For instance, as illustrated in Figure 1, knowing that BaTiO<sub>3</sub> forms a perovskite structure,
one can deduct that it is likely for another chemically similar ion as Ca<sup>2+</sup> to form the same structure.
We have
implemented a mathematical model that learns these substitution rules from a database of experimentally
observed crystal structure (e.g., the ICSD).
Basically, what the model provides is a probability
distribution for any ionic substitution.
In Figure 2 we show the matrix indicating the data mined
substitution tendency for two ionic species obtained from this work.
The ions have been sorted by Mendeleev number and therefore groups of chemically similar ions (e.g., the transition metals) are grouped together.
Red colors indicate that two ions
tend to substitute while blue is associated with pair of species not substituting to each other.

![ionic substitution correlations](img/structure-predictor/ions-correlation.png)
_Figure 2: Data mined tendency for ionic substitutions.
Red indicates high substitution tendency.
Blue indicates that the tow ions tend to not substitute._

### The compound prediction procedure



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

In the future, we aim to develop faster approximate algorithm to significantly speed up the search process. Currently a query needs to calculate the structure similarity to ~100,000 to 250,000 existing structures, which is too slow. 

### Citations

To cite the Structure Search App, please reference the following works:

- G. Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: 10.1038/nmat2321
[^2]: 10.1021/ic102031h
[^3]: 10.1021/cm100795d
[^4]: 10.1038/nmat1691

### Authors

- Geoffroy Hautier
- Anubhav Jain
