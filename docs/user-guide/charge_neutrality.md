# Charge Neutrality Check
#### by Dr. Hu

## Manual

### Background 

The law of electron charge neutrality states that in any single ionic solution a sum of negative electrical charges attracts an equal sum of positive electrical charges. As stated in [^1], "Charge Neutrality Ions tend to combine into charge-neutral aggregates. The same thinking applies to both ionic solids and more covalently bonded semiconductors. Any periodic solid must be charge neutral; otherwise, it would have an infinite electrostatic potential. Balancing oxidation states and fulfilling the valence octet rule are equivalent, e.g., III–V semiconductors, such as GaAs, can be represented as Ga3+As3−. Charge neutrality contracts the compositional space by at least an order of magnitude for binaries, ternaries, and quaternaries".


Here charge neutrality is used as a basic chemical validity test of hypothetical materials compositions. This criterion has been used in our recent study of generative design of new materials compositions [^2].


### The charge neutrality checking Method

We use the charge neutrality check filter as implemented in the SMACT package. In this method, for a given composition, it firsts obtain the oxidation states of each element and then it exhaustively enumerate the possible oxidation states to see if all the elemental ratios weighted charges can be summed to 0 or below a threshold. The details are shown in [^1]. 



### Performance and Limitations

For complex composition with a large number of atoms, the calculation process may be slow. We limit the number of elements in the composition to be less than 9. 

### Using the charge neutrality checking tool

#### Entering Inputs

Practically, the procedure consists in 3 steps

1. input formula in the input box or upload a csv file with a list of materials formulas.
2. click "Check Now"
3. The app will show which formulas have passed the charege neutrality check.

#### Interpreting the Results

The result will show if the material has passed the charge neutrality check or not.

### Future features

New algorithms will be developed to significantly speed up the query process or complex formulas.

### Citations

If you use this app, please cite the web App, and reference the following works:

- D. W. Davies et al, "Computational screening of all stoichiometric inorganic materials" Chem 1, 617 (2016).
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: https://smact.readthedocs.io/en/latest/_modules/smact/screening.html#smact_filter
[^2]: Dan, Yabo, Yong Zhao, Xiang Li, Shaobo Li, Ming Hu, and Jianjun Hu. "Generative adversarial networks (GAN) based efficient sampling of chemical composition space for inverse design of inorganic materials." npj Computational Materials 6, no. 1 (2020): 1-7.

### Authors

- Dr. Jianjun Hu

