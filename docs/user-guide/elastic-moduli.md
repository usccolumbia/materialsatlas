
# Elastic Moduli Predictor
#### by Wei Lai

## Manual

### Background

Elascticity is a materials property representing how heat is transferred from one side of a material to the other when thermal energy is applied. We predict the elascticity of the materials based on our convolutional neural networks (CNNs) to learn physically meaningful features from the three-dimensional electronic charge density (ECD) of materials for elastic property prediction. We use electronic charge density (ECD) as a generic unified 3D descriptor for materials property prediction with the advantage of possessing close relation with the physical and chemical properties of materials. We developed an ECD-based 3D convolutional neural networks (CNNs) for predicting the elastic properties of materials, in which CNNs can learn effective hierarchical features with multiple convolving and pooling operations. This app can predict the elastic properties such as bulk/shear modulus and Poisson's ratio for a given crystal materials formula or structure. More details can be found in Yong Zhao et al.[^1].


### The Elastic Moduli Prediction method

We propose to use electronic charge density (ECD) as a generic unified 3D descriptor for materials property prediction with the advantage of possessing close relation with the physical and chemical properties of materials and developed an ECD-based 3D convolutional neural networks (CNNs) for predicting the elastic properties of materials, in which CNNs can learn effective hierarchical features with multiple convolving and pooling operations. Since physical and chemical properties of materials are related to the transferability between atoms (nuclei) and the presence of electronic charges or electronic multipoles on atoms or molecules, extraction of informative features from materials ECD can help predict materials properties. 

### Performance and Limitations

Table2: The results from fivefold cross validation on the whole data set with 2170 samples.
<img src="img/Elastic_1.png" width=800>

### Using the Elastic Moduli Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 4 steps

1. Provide a csv file of formulas or a cif file Or provide 1 or more material formulas separated by comma or space (no processing if file uploaded)
2. Select elastic properties by clicking Bulk mod, Shear mode, Young's mod, or Poisson ratio
3. Click "Check Now".
4. Collect the results by cliking the "Download Results" Link.

#### Interpreting the Results

The results contains Composition and Elastic Moduli Predicted (Pa).

### Future features

In the future, Currently, we want to generate more ECD data sets with more space groups to extend this method to more materials with diverse structures.

### Citations

To cite the LTC Predictor App, please reference the following works:

- Zhao, Y.; Yuan, K.; Liu, Y.; Louis, S. Y.; Hu, M.; Hu, J. Predicting Elastic Properties of Materials from Electronic Charge Density Using 3D Deep Convolutional Neural Networks. J. Phys. Chem. C 2020, 124 (31), 17262– 17273,  DOI: 10.1021/acs.jpcc.0c02348
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Zhao, Y.; Yuan, K.; Liu, Y.; Louis, S. Y.; Hu, M.; Hu, J. Predicting Elastic Properties of Materials from Electronic Charge Density Using 3D Deep Convolutional Neural Networks. J. Phys. Chem. C 2020, 124 (31), 17262– 17273,  DOI: 10.1021/acs.jpcc.0c02348
[^2]: https://tedesignlab.org/database/
[^3]: https://hackingmaterials.lbl.gov/matminer/matminer.featurizers.composition.html?highlight=magpie
[^4]: https://github.com/CompRhys/roost
[^5]:Omee, Sadman Sadeed, Steph-Yves Louis, Nihang Fu, Lai Wei, Sourin Dey, Rongzhi Dong, Qinyang Li, and Jianjun Hu. "Scalable deeper graph neural networks for high-performance materials property prediction." arXiv preprint arXiv:2109.12283 (2021).
[^6]:https://figshare.com/articles/dataset/Citrine_Thermal_Conductivity_Data/7231202

### Authors

- Jianjun Hu
- Lai Wei
