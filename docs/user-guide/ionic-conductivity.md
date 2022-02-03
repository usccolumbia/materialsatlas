
# Ionic Conductivity Predictor



## Manual

### Background 

Ionic conducctivity prediction has big potential in computational design for battery materials, which is, however, an extremely challenging problem due to the lack of sufficient ion conductivity datas and the complex relationships from structure to this property. There are a few attempts for this problem. The most notable one is [^7], in which the authors first search for
materials satisfying several prerequisite requirements (i.e. other than ionic conductivity), and then utilize 40 experimental data samples to build a fast ionic conductivity classification model using 20 hand-crafted physical/structural descriptors (See below) and logistic regression classifer to look for the most likely superionic materials among these remaining candidates. Then used it for screening 12 000 candidates and billions of compositions [^8]. Another XGBoost model is develped in [^6] for ion conductivity prediction of perovskites. Trained with 7000 samples and a set of features including average ionic radius, minimum electronegativity, minimum atomic mass, minimum formation energy of oxides for all B-site, and B-site dopant ions of the perovskite as the crucial and relevant predictors for determining conductivity and the type of charge carriers. In [^3], Using primarily theoretical elemental feature descriptors derivable from tabulated information on the unit cell and the atomic properties of the components of a target compound on a limited dataset of 70 NASICON-examples, the authors  designed a logistic regression-based model capable of distinguishing between poor and good superionic conductors with a cross-validation accuracy of over 82%. Here the extremely limited ion conductivity data limits the application of powerful complex models such as graph neural networks. 

<img src="../img/ionic-features.png" width=600>



### The Ionic conductivity Prediction Method

In this app, we plan to implement two models including the the XGboost model for perovskite ion conductivity prediction and the logistic regression model for ionic conductivity of sodium and lithium-based SICON compounds. 

We will also implement a composition based ion conductivity predictor using the Roost model. 

### The ionic conductivity prediction procedure

The process includes 2 stages, including feature extraction from structures and machine learning prediction. 

### Performance and Limitations

Due to the extremely small dataset, the prediction performance may only be good for the specific subset of materials such as perovskites. The models trained with 70 or 40 samples cannot generalize well out of their training domain. 

### Using the Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Upload a cif structure file or a csv file or just input some formulas in the input text box.

2. Start the prediction: click 'Predict Now' to begin the prediction.
   
4. Examine results: Upon completion of the task, you will be given a link to download the results. 


#### Interpreting the Results

The users need to be cautious over the predicted results due to the uncertainy with the models trained with small dataset. 


### Future features

Due to the limited labelled data of ion conductivity, we will apply transfer learning and semi-supervised learning to improve our model performance. 

### Citations

To cite the ion conductivity Predictor App, please reference the following works:

- G. Hautier, V. Ehrlacher, C.C. Fischer, A. Jain, G. Ceder, Data Mined Ionic Substitutions for the Discovery of New Compounds, Inorganic Chemistry, vol. 50, 2011, pp. 656-663.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Wang, Chuhong, Koutarou Aoyagi, Pandu Wisesa, and Tim Mueller. "Lithium ion conduction in cathode coating materials from on-the-fly machine learning." Chemistry of Materials 32, no. 9 (2020): 3741-3752.
[^2]: Lv, Chade, Xin Zhou, Lixiang Zhong, Chunshuang Yan, Madhavi Srinivasan, Zhi Wei Seh, Chuntai Liu et al. "Machine Learning: An Advanced Platform for Materials Development and State Prediction in Lithium‐Ion Batteries." Advanced Materials (2021): 2101474.
[^3]: Xu, Yijie, Yun Zong, and Kedar Hippalgaonkar. "Machine learning-assisted cross-domain prediction of ionic conductivity in sodium and lithium-based superionic conductors using facile descriptors." Journal of Physics Communications 4, no. 5 (2020): 055015.
[^4]: Zhao, Qian, Maxim Avdeev, Liquan Chen, and Siqi Shi. "Machine learning prediction of activation energy in cubic Li-argyrodites with hierarchically encoding crystal structure-based (HECS) descriptors." Science Bulletin (2021).
[^5]: Shao, Hui, Jiansu Pu, Yanlin Zhu, Boyang Gao, Zhengguo Zhu, and Yunbo Rao. "Visual Analysis on Machine Learning Assisted Prediction of Ionic Conductivity for Solid-State Electrolytes." In 2021 IEEE 14th Pacific Visualization Symposium (PacificVis), pp. 1-5. IEEE, 2021.
[^6] Priya, Pikee, and N. R. Aluru. "Accelerated design and discovery of perovskites with high conductivity for energy applications through machine learning." npj Computational Materials 7, no. 1 (2021): 1-12. https://www.nature.com/articles/s41524-021-00551-3?proof=t%2Btarget%253D#data-availability
[^7]: Sendek, Austin D., Qian Yang, Ekin D. Cubuk, Karel-Alexander N. Duerloo, Yi Cui, and Evan J. Reed. "Holistic computational structure screening of more than 12000 candidates for solid lithium-ion conductor materials." Energy & Environmental Science 10, no. 1 (2017): 306-320.
[^8]: Cubuk, Ekin D., Austin D. Sendek, and Evan J. Reed. "Screening billions of candidates for solid lithium-ion conductors: A transfer learning approach for small data." The Journal of chemical physics 150, no. 21 (2019): 214701.
[^9]: 

### Authors

- Jianjun Hu
