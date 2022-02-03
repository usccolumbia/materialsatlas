
# Ionic Conductivity Predictor



## Manual

### Background 

Ionic conducctivity prediction is an essential step of computational materials design for batteries. 


### The Ionic conductivity Prediction Method


### The compound prediction procedure



### Performance and Limitations

### Using the Structure Predictor

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Pick elements: Select on the periodic table what constituent elements comprise the chemical space you are interested in.
   For instance if you want to make predictions for battery materials based on Li, Mn and O, you should pick those three elements.

2. Pick oxidation states: The model uses the oxidation states to make predictions.
   V<sup>3+</sup> does not substitute with the same elements as V<sup>5+</sup>, so if you want to study Mn<sup>3+</sup> compounds, you should pick +3 for Mn, +1 for Li (no other choices anyway) and -2 for O.
   Sometimes you do not know what oxidation states you are interest in.
   Let say you want all Li-Mn-O compounds regardless of the oxidation state of Mn.
   Then, I would suggest running the model several times, one for Mn<sup>2+</sup>, one for Mn<sup>3+</sup>, and lastly one for Mn<sup>4+</sup>.
   This should cover all the chemical space you are looking at.

3. Start the prediction: click 'Predict Structure' to begin the prediction.
   Predictions are not immediately available and will require some time to complete.
   You can monitor the status of your request in the [dashboard](https://materialsproject.org/dashboard).

4. Examine results: Upon completion of the task, you will be given a link to a landing page providing details on the candidate structures.
   We also provide cif files for the predicted compounds as well as VASP files ready to be run with standard parameters.
   We do not provide any DFT results due our limited computational budget for the moment.
   It is the responsibility of the user to run the predictions.
   Also, as the pseudopotentials are proprietary in VASP (POTCARs) we do not provide those but a script is sent along that can be run to make sure the POTCARs are built from a directory containing all pseudopotentials.

#### Interpreting the Results




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

### Authors

- Jianjun Hu
