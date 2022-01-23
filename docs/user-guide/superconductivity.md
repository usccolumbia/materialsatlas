
# Superconductivity Predictor

## Manual

### Background on Superconductivity Tc Prediction

Superconductors were typically discovered by trial-and-error aided by the knowledge and intuition of individual researchers. Machine learning based screening of known materials compositions and structures for high transition temperature (Tc) superconductors are highly desirable. Here we explore the capability of machine learning model for composition based superconductor Tc prediction. 

The Supercon database contains a variety of superconductors, including two large families of cuprates and iron-based (about 35% and 9%, respectively). The remaining set contains a mix of various materials, including conventional phonon-driven superconductors (e.g., elemental superconductors, A15 compounds), known unconventional superconductors like the layered nitrides and heavy fermions, and many materials with unknown mechanism of superconductivity (such as bismuthates and borocarbides). Graphene with magic angles are another category of superconductors.


### The Superconductor Critical Temperature Prediction Method

The current prediction model implemented here is based on the Random Forest regression model trained with the composition descriptors of the Supercon dataset [^2], which contains more than 25,000 compositions with experimental critical temperature labels. Only less than 200 of them have structure information, which it challenging to train structure based predictors for Tc. The composition descriptors are calculated using the MatMiner package [^3]. 

### The basic idea


<!-- ![ionic substitution correlations](img/structure-predictor/ions-correlation.png)
_Figure 2: Data mined tendency for ionic substitutions.
Red indicates high substitution tendency.
Blue indicates that the tow ions tend to not substitute._ -->

### The Tc prediction procedure



### Performance and Limitations

### Using the Structure Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 2 steps

1. Input the formula or upload a cif file

2. Start the prediction: click 'Predict Structure' to begin the prediction.
   
3. Examine results: 

#### Interpreting the Results



### Future features

In the future, we would like to introduce structure based Tc prediction model and use transfer learning strategy to deal with the small dataset issue. Unsupervised clustering methods will also be developed for small data based inference. Another possible extension is to use crystal structure prediction algorithms to predict coarse structures for the supercon database. 

### Citations

To cite the Structure Predictor App, please reference the following works:

- Dan, Yabo, Rongzhi Dong, Zhuo Cao, Xiang Li, Chengcheng Niu, Shaobo Li, and Jianjun Hu. "Computational Prediction of Critical Temperatures of Superconductors Based on Convolutional Gradient Boosting Decision Trees." IEEE Access 8 (2020): 57868-57878..
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).

[^1]: National Institute of Materials Science, Materials Information Station, SuperCon, http://supercon.nims.go.jp/index_en.html (2011).
[^2]: 10.1021/ic102031h
[^3]: Dan, Yabo, Rongzhi Dong, Zhuo Cao, Xiang Li, Chengcheng Niu, Shaobo Li, and Jianjun Hu. "Computational Prediction of Critical Temperatures of Superconductors Based on Convolutional Gradient Boosting Decision Trees." IEEE Access 8 (2020): 57868-57878.
[^4]: Li, Shaobo, Yabo Dan, Xiang Li, Tiantian Hu, Rongzhi Dong, Zhuo Cao, and Jianjun Hu. "Critical temperature prediction of superconductors based on atomic vectors and deep learning." Symmetry 12, no. 2 (2020): 262.

### Authors

- Jianjun Hu
