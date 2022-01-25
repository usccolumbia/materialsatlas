
# Hypothetical 2D Materials (composition) Database
#### by Dr. Jianjun Hu

## Manual

### Background 



### The database generation Method

The compound prediction model available on the Materials Project now, through the structure predictor app, is based on our recent work on the data mining of ionic substitutions.
In this section we will briefly explain the idea of the approach and how to use the explorer.
More details can be found in Hautier et al.[^2]





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

The results pages provides a set of structure id's corresponding to the candidate structures.
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



### Future features

In the future, we want to generate more 2D materials candidates and also possibly predict their crystal structures using our crystal structure prediction algorithm.s

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
