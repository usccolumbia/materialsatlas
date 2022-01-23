
# Lattice Constants Predictor

## Manual

### Background

Given a material composition, predicting its unit cell lattice constants can help to determine its structures by human or they can be used as input to crystal structure prediction algorithm for prediction. 

### The Lattice Constants Prediction Method

The compound prediction model available on the Materials Project now, through the structure predictor app, is based on our recent work on the data mining of ionic substitutions.
In this section we will briefly explain the idea of the approach and how to use the explorer.
More details can be found in Hautier et al.[^2]



![substitution example](img/structure-predictor/substitution-example.png)
_Figure 1: An example of ionic substitution._





### Performance and Limitations

### Using the Lattice Constant Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Input a material formula in the input box  or upload a csv file with lists of formulas

2. Select the category of the input material (optional) 
   When the csv file is uploaded, then the predictor just uses the generic model.

3. Click "Predict Now"

#### Interpreting the Results



### Future features

We find that the prediction accuracy of lattice constants strongly depend on the crystal systems. More models over specialized categories of materials will be developed.

### Citations

To cite the Structure Predictor App, please reference the following works:

- G. Hautier, V. Ehrlacher, C.C. Fischer, A. Jain, G. Ceder, Data Mined Ionic Substitutions for the Discovery of New Compounds, Inorganic Chemistry, vol. 50, 2011, pp. 656-663.
- A. Jain, G. Hautier, C. J. Moore, S. P. Ong, C. C. Fischer, T. Mueller, K. A. Persson, and G. Ceder, A high-throughput infrastructure for density functional theory calculations, Computational Materials Science, vol. 50, 2011, pp. 2295-2310.

[^1]: 10.1038/nmat2321
[^2]: 10.1021/ic102031h
[^3]: 10.1021/cm100795d
[^4]: 10.1038/nmat1691

### Authors

- Yuxin Li
- Jianjun Hu
