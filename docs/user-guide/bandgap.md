
# Bandgap Predictor

#### by Dr. Hu

## Manual

### Background

The bandgap is the energy difference between the valence band maximum (VBM) and the conduction band minimum (CBM) in the electronic band structure of a material. The bandgaps of the semiconductors are greater than the bandgap of metals (0 eV) and smaller than that of insulators (usually greater than 5 eV). The bandgap acts as an forbidned gap for electrons, which can not shift from VBM to CBM without enough external energy. The electrons in valence region are not contributing for electric current while the electrons in conduction bands are free to move.   Therefore, by modulating the external thermal energy, we can tune the electron flow of a semiconductor. 




### The LTC Prediction methods



#### The composition based LTC prediction model

Our composition model is trained using the Magpie descriptors from the Matminer package [^3] together with the Roost neural network model [^4]. 

#### The deep graph neural network model for LTC prediction

Our structure based LTC prediction model is based on our latest work of DeeperGATGNN algorithm [^5], which is a scalable deep graph neural network model with the state-of-the-art performance for structure based materials property prediction. 

### Performance and Limitations

The MAE of our composition ML model on the hold-out test set is xxxxx. 
The MAE of our structure ML model on the hold-out test set is xxxxx. 

### Using the LTC Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Input a material formula or a csv with a list of formulas. It will automatically use the composition machine learning model. You can also upload a structure cif file, it will select the graph neural network model accordingly. 

2. click "predict now"

3. collect the result or download the results csv file.



#### Interpreting the Results




### Future features

In the future, we want to further improve the performance of our model using transfer learning and semi-supervised learning. 

### Citations

To cite the LTC Predictor App, please reference the following works:

- Goodall, Rhys EA, and Alpha A. Lee. "Predicting materials properties without crystal structure: Deep representation learning from stoichiometry." Nature communications 11, no. 1 (2020): 1-9.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Ouyang, Y., Yu, C., Yan, G. & Chen, J. Machine learning approach for the prediction and optimization of thermal transport properties. Front. Phys. 16, 43200 (2021).
[^2]: https://tedesignlab.org/database/
[^3]: https://hackingmaterials.lbl.gov/matminer/matminer.featurizers.composition.html?highlight=magpie
[^4]: https://github.com/CompRhys/roost
[^5]:Omee, Sadman Sadeed, Steph-Yves Louis, Nihang Fu, Lai Wei, Sourin Dey, Rongzhi Dong, Qinyang Li, and Jianjun Hu. "Scalable deeper graph neural networks for high-performance materials property prediction." arXiv preprint arXiv:2109.12283 (2021).
[^6]:https://figshare.com/articles/dataset/Citrine_Thermal_Conductivity_Data/7231202

### Authors

- Jianjun Hu

