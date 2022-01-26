
## Composition based Machine Learning Predictor of Materials Properties
#### by Dr. Jianjun Hu

## Manual

### Background 

This web app aims to build a generic program for click-and-play training and testing a composition based machine learning predictor for any specified materials property of interest to the user (instead of us). This makes it easy for materials scientists to easy try the machine learning prediction models on their datasets without complicted programming. 




### The ML based property Prediction Method

The composition based machine learning prediction models on MaterialAtlas.com are classified into two categories: regression models which predict a real-value output, and classification models whict output a categorical output. A standard machine learning model is composed of the sample representation (features or descriptors) plus the machine learning algorithm. Here we have provided six different types of composition based descriptors including Magpie features, Matminer features, deml features, matscholar_el embedding features, megnet_el embedding features and user-defined features. The definition of these features can be found here at Matminer documentation website [^1] The machine learning models are implemented using the scikit-learn package [^2]. The implemented regression algorithms include RandomForest, Support Vector Machines (SVM), Neural networks, ADaboot, GradientBoosting, ElasticNet, Ridge Regression, BayesianRegression, ArdRegression. The classifiers include Random Forest, Neural network, SVM Adaboost, GradientBoosting, Ridge, Logistic Regression, BernouliRBM. 



### Performance and Limitations

The models are all trained with default hyparameters without parameter tuning, which may lead to non-optimal prediction performance. However, our research experience shows that usually there won't be significant difference in most cases.

### Using the Composition based Materials Property Predictors

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Select prediction type: regression (for real-value output) or classification (for categorical output)

2. select machine learning algorithm

3. select descriptors/features

4. upload the training set as a csv file, each row contains a material composition and its related property
e.g.

formula, piezoelectric-coefficient
SrTiO3, 0.23
Li2Co2, 0.15

5. upload the test file as a csv file. Each file has the same format but set the property as 0. 

6. click "Run Now"

8. Wait and then download results: 

#### Interpreting the Results




### Future features

More algorithms and descriptors can be added to this extensible modules.

### Citations

To cite the Structure Predictor App, please reference the following works:

- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).

[^1]: https://hackingmaterials.lbl.gov/matminer/featurizer_summary.html
[^2]: https://scikit-learn.org/stable/supervised_learning.html


### Authors

- Dr. Jianjun Hu
