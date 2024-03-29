# Electronegativity Balance Check
#### by Dr. Hu

## Manual

### Background 

By assuming that all charge-neutral combinations of oxidation states are accessible, we can implement a chemical constraint based on the electronegativity
of the component elements. The empirical electronegativity (c) scale represents the ‘‘attraction’’ of a particular atom for electrons. For a stable compound, the relation $\chi$<sup>cation</sup> $\chi$< <sup>canion</sup> should be obeyed, i.e., the most electronegative element carries the most negative charge. Here electronegativity balance is used as a basic chemical validity test of hypothetical materials compositions. This criterion has been used in our recent study of generative design of new materials compositions [^2].


### The charge neutrality checking Method

We use the electronegativity balance check filter as implemented in the SMACT package [^3]. In this method, for a given composition, it firsts obtain the oxidation states of each element and then it exhaustively enumerate the possible oxidation states to see if all the elemental ratios weighted charges can be summed to 0 or below a threshold. The details are shown in [^1]. 



### Performance and Limitations

For complex composition with a large number of atoms, the calculation process may be slow.  

### Using the electronegativity balance checking tool

#### Entering Inputs

Practically, the procedure consists in 3 steps

1. input formula in the input box or upload a csv file with a list of materials formulas.
2. click "Check Now"
3. The app will show which formulas have passed the electronegativity balance check.

#### Interpreting the Results

The result will show if the material has passed the electronegativity balance check or not.



### Citations

If you use this app, please cite the web App, and reference the following works:

- D. W. Davies et al, "Computational screening of all stoichiometric inorganic materials" Chem 1, 617 (2016).
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: https://smact.readthedocs.io/en/latest/_modules/smact/screening.html#smact_filter
[^2]: Dan, Yabo, Yong Zhao, Xiang Li, Shaobo Li, Ming Hu, and Jianjun Hu. "Generative adversarial networks (GAN) based efficient sampling of chemical composition space for inverse design of inorganic materials." npj Computational Materials 6, no. 1 (2020): 1-7.
[^3]: https://github.com/WMD-group/SMACT

### Authors

- Dr. Jianjun Hu

