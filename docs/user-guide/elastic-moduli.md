
# Elastic Moduli Predictor
#### by Wei Lai

## Manual

### Background

Elasticity quantifies a material's resistance to non-permanent, or elastic, deformation. When under stress, materials will first exhibit elastic properties: the stress causes them to deform, but the material will return to its previous state after the stress is removed. After passing through the elastic region and through their yield point, materials enter a plastic region, where they exhibit permanent deformation even after the tensile stress is removed. Fast computational prediction of elastic property can be used to do large-scale screening of new elastic materials. Especially, since bulk modulus and shear modulus, two elastic property measurements can be used to calculate a material's hardness, elasticity prediction models have been widely used to find superhard materials 
[^2] [^7]. We have also used the 3d electronic cloud to predict elastic modulie in [^1].

### The Elastic Moduli Prediction method

We developed two prediction models for elasticity prediction using the known materials with elastic information in the MaterialsProject database. The number of training samples for predicting each of the properties of this module is given below: <br>
Bulk Mod - 13176 <br>
Shear Mod - 13176 <br>
Young's Mod - 12854 <br>
Poisson Ratio - 12858 

The element range for these training datasets are given below: <br>
Bulk Mod - 89 <br>
Shear Mod - 89 <br>
Young's Mod - 85 <br>
Poisson Ratio - 85 

#### The composition based Elastic Moduli prediction model

Our composition model is trained using the Magpie descriptors from the Matminer package [^4] together with the Roost neural network model [^5]. 
For this model, only the formula is needed. 

#### The deep graph neural network model for Elastic Moduli prediction

Our structure based Elastic Moduli prediction model is based on our latest work of DeeperGATGNN algorithm [^6], which is a global attention based scalable deep graph neural network model with the state-of-the-art performance for structure based materials property prediction. 

### Performance and Limitations
The MAE of our composition ML model on the hold-out test set is - <br>
Bulk Mod - 15.7 <br>
Shear Mod - 18.0 <br>
Young's Mod - 76.8 <br>
Poisson Ratio - 8.7 

The MAE of our structure ML model on the hold-out test set is - <br>
Bulk Mod - 13.4268 <br>
Shear Mod - 15.2374 <br>
Young's Mod - 55.335 <br>
Poisson Ratio - 0.0962

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

In the future, we want to generate more ECD data sets with more space groups to extend this method to more materials with diverse structures.

### Citations

To cite the LTC Predictor App, please reference the following works:

- Zhao, Y.; Yuan, K.; Liu, Y.; Louis, S. Y.; Hu, M.; Hu, J. Predicting Elastic Properties of Materials from Electronic Charge Density Using 3D Deep Convolutional Neural Networks. J. Phys. Chem. C 2020, 124 (31), 17262– 17273,  DOI: 10.1021/acs.jpcc.0c02348
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Zhao, Y.; Yuan, K.; Liu, Y.; Louis, S. Y.; Hu, M.; Hu, J. Predicting Elastic Properties of Materials from Electronic Charge Density Using 3D Deep Convolutional Neural Networks. J. Phys. Chem. C 2020, 124 (31), 17262– 17273,  DOI: 10.1021/acs.jpcc.0c02348
[^2]: Kvashnin, Alexander G., Zahed Allahyari, and Artem R. Oganov. "Computational discovery of hard and superhard materials." Journal of Applied Physics 126, no. 4 (2019): 040901.
[^4]: https://hackingmaterials.lbl.gov/matminer/matminer.featurizers.composition.html?highlight=magpie
[^5]: https://github.com/CompRhys/roost
[^6]:Omee, Sadeed, S., Louis, S.,  Fu, N., Wei,L., Dey,S., Dong, R.,  Li, Q., and  Hu. J., "Scalable deeper graph neural networks for high-performance materials property prediction." arXiv preprint arXiv:2109.12283 (2021).
[^7]: Chen, Wei-Chih, Joanna N. Schmidt, Da Yan, Yogesh K. Vohra, and Cheng-Chien Chen. "Machine learning and evolutionary prediction of superhard BCN compounds." npj Computational Materials 7, no. 1 (2021): 1-8.

### Authors

- Jianjun Hu
- Lai Wei
- Sadman Sadeed Omee
- Yuqi Song
