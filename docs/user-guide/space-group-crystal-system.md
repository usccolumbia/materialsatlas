
# Space group and Crystal Systems Predictor

## Manual

### Background

Structural information of materials such as the crystal systems and space groups are highly useful for analyzing their physical properties. However, the enormous composition space of materials makes experimental X-ray diffraction (XRD) or first-principle-based structure determination methods infeasible for large-scale material screening in the composition space. This app provides a machine learning-based model for predicting space groups and crystal systems of inorganic materials, given only their compositional information. Such models allow us to conduct fast screening of millions of potential chemicals as done in [^4]. There are three popular types of features/descriptors: Magpie[^2] atom vector [^3] and one hot encoding (atom frequency) can be used as the inputs of the machine-learning algorithms. Neither XRD data nor DFT calculation is involved in feature calculations. Our related work include [^1] and [^6]. 

### The Space group and Crystal Systems Prediction Method

In this app, we used the CRYSPnet algorithm [^5] for space group and crystal system prediction. It is a multi-layer perceptron (MLP) neural network models based on Magpie Descriptors as computed using the Matminer package [^2]. 


### Performance and Limitations

Table2: Crystal system prediction performance

<img src="../img/Space_group_table2.png" width=800>

Table3: Space group prediction performance

<img src="../img/Space_group_table3.png" width=800>

Currently, we have only implemented the cubic crystal system option for space group prediction. Other options will be added soon.

### Using the Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Provide a csv file of formulas or provide 1 or more material formulas separated by comma or space (no processing if file uploaded).
2. Click "Check Now".
3. Collect the results by cliking the "Download the Results" Link.

#### Interpreting the Results

The result including: Formulas, Bravais System, Bravais System Prob, Spacegroups, Spacegroups Prob, a, b, c, Alpha(α), Beta(β), Gamma(γ) (Bravais Lattices) based on your input. You can download the csv file of the result by clicking "Download results". 


### Future features

In the future work, we may try to set a formation energy threshold to filter out those materials in the Materials Project dataset. In addition, our feature importance analysis shows that electronegativity, covalent radius, Mendeleev number, melting temperature, GAS volume pascal, and mean atomic weight are crucial factors for predicting the crystal system and space group for a given material composition. We also found that the ML performance for space group prediction is much lower than that of materials crystal system prediction given their composition. That is because the data is distributed more unevenly over 18 space groups in our study, which may call for more advanced techniques to address this issue.

### Citations

To cite the Predictor App, please reference the following works:

- Liang, Haotong, Valentin Stanev, A. Gilad Kusne, and Ichiro Takeuchi. "CRYSPNet: Crystal structure predictions via neural networks." Physical Review Materials 4, no. 12 (2020): 123802.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


### Authors
- Jianjun Hu
- Lai Wei


### References
[^1]: Zhao, Yong, et al. "Machine learning-based prediction of crystal systems and space groups from inorganic materials compositions." ACS omega 5.7 (2020): 3596-3606.

[^5]: Liang, Haotong, Valentin Stanev, A. Gilad Kusne, and Ichiro Takeuchi. "CRYSPNet: Crystal structure predictions via neural networks." Physical Review Materials 4, no. 12 (2020): 123802.

[^2]: Ward, L.; Agrawal, A.; Choudhary, A.; Wolverton, C. A general purpose machine learning framework for predicting properties of inorganic materials. npj Comput. Mater. 2016, 2, 16028.

[^6]: Li, Yuxin, Wenhui Yang, Rongzhi Dong, and Jianjun Hu. "MLatticeABC: generic lattice constant prediction of crystal materials using machine learning." ACS omega 6, no. 17 (2021): 11585-11594.

[^3]: Zhou, Q.; Tang, P.; Liu, S.; Pan, J.; Yan, Q.; Zhang, S.-C. Learning atoms for materials discovery. Proc. Natl. Acad. Sci. U.S.A. 2018, 115, E6411−E6417.

[^4]: Jha, D.; Ward, L.; Paul, A.; Liao, W.-k.; Choudhary, A.; Wolverton, C.; Agrawal, A. ElemNet: Deep Learning the Chemistry of Materials From Only Elemental Composition. Sci. Rep. 2018, 8, 17593.

