
# Composition Enumerator
#### Dr. Hu

## Manual

### Background 

Tinkering and doping are two common ways to optimize an existing material or find a better alternative. This web app allow the users to generate all chemically valid compositions of a given chemical system defined by a materials formula or a set of elements. It outputs the formulas, corresponding oxidation states, electronegativity and a predicted formation energy so that you can rank the results by their chemical feasiblity.

### The composition enumeration Method

We use the composition enumeration algorithms as defined in the SMACT package [^1] to implement our app.  



### Performance and Limitations

For two complex chemical systems with large atom number or too many elements, the generation process may become very slow.

### Using the Similar structure Finder

#### Entering Inputs

Practically, the procedure consists in 3 steps

1. Input a set of elements seperated by space
2. inpuy the max no. of atoms for each element
3. choose all oxidation states or only commonly used oxidation states for all element (only first one implemented so far).
4. click "Explore now"
5. get results or download the result file.

#### Interpreting the Results

The result contains the all valid formulas along with the corresponding oxidation states, electronegativity and predicted formation energy.

### Future features

Commonly used oxidation states option will be implemented. 

### Citations

To cite the similar Structure finder App, please reference the following works:

- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).
- D. W. Davies et al, "SMACT: Semiconducting Materials by Analogy and Chemical Theory" JOSS 4, 1361 (2019)



[^1]: https://github.com/WMD-group/SMACT

### Authors

- Dr. Jianjun Hu
