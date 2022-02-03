
# Lattice Constants Predictor

## Manual

### Background

Given a material composition, predicting its unit cell lattice constants can help to determine its structures by human or they can be used as input to crystal structure prediction algorithm for prediction. 

### The Lattice Constants Prediction Method

The lattice constants (unit cell parameters) prediction model here is based on our recent work on composition based lattice parameter prediction. It uses the Magpie composition descriptors with deep neural networks for lattice constant predictions. In addition to the basic Magpie Features, we introduce a few global features to enhance Magpie descriptors. 
More details can be found in Y.Li et al.[^1]


### Performance and Limitations

<img src="../img/LTC-performance.png" width=900>

### Using the Lattice Constant Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Input a material formula in the input box  or upload a csv file with lists of formulas

2. Select the category of the input material (optional) 
   When the csv file is uploaded, then the predictor just uses the generic model.

3. Click "Predict Now"
4. collect the results by cliking the "Download the Results" Link.

#### Interpreting the Results

<img src='../img/LTC.png' width=800>

### Future features

We find that the prediction accuracy of lattice constants strongly depend on the crystal systems. More models over specialized categories of materials will be developed.

### Citations

To cite the Structure Predictor App, please reference the following works:

- Li, Yuxin, Wenhui Yang, Rongzhi Dong, and Jianjun Hu. "MLatticeABC: generic lattice constant prediction of crystal materials using machine learning." ACS omega 6, no. 17 (2021): 11585-11594.
- Liang, Haotong, Valentin Stanev, A. Gilad Kusne, and Ichiro Takeuchi. "CRYSPNet: Crystal structure predictions via neural networks." Physical Review Materials 4, no. 12 (2020): 123802.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Li, Yuxin, Wenhui Yang, Rongzhi Dong, and Jianjun Hu. "MLatticeABC: generic lattice constant prediction of crystal materials using machine learning." ACS omega 6, no. 17 (2021): 11585-11594.
[^2]: Liang, Haotong, Valentin Stanev, A. Gilad Kusne, and Ichiro Takeuchi. "CRYSPNet: Crystal structure predictions via neural networks." Physical Review Materials 4, no. 12 (2020): 123802.


### Authors

- Jianjun Hu
- Yuxin Li
