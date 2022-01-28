# Formation Energy and E-above-hull Check
#### by Dilanga Siriwardane

## Manual

### Background

The formation energy of a material defines the energy required to dissociate that material into its respective elements. Thus, it indicates the thermodynamic stability against the elements it consists of. Usually, the density functional theory (DFT) based first-principles calculations are performed to calculate the formation energy. It is required to identify the crystal structure data in advance for that purpose. However, the ground state structures are unknown for most of the compositions. Therefore, it is difficult to determine the formation energy of a new composition using DFT. Another disadvantage of the above method is that the first-principles calculation of formation energy is time-consuming and expensive [^1]. As a solution, machine learning models are trained based on the elemental and electronic properties of the available compositions in the materials databases. 

It should also be mentioned that a higher accuracy for predicting formation energy can be achieved based on the graph neural networks if the crystal structure is available. This is a very important tool if we want to find the formation energy of a material when the energy information is not accessible [^2]. 

Therefore, we provide both composition-based and structure-based options for predicting the formation energy using MaterialsAtals.org. You can submit either the cif file of the crystal structure or enter the chemical formula to perform the predictions.


### Citations
[^1] Mao, Y., Yang, H, Sheng, Y., Wang, J., Ouyang, R., Ye, C., Yang, J. and Zhang, W. Prediction and Classification of Formation Energies of Binary Compounds by Machine Learning: An Approach without Crystal Structure Information, ACS Omega 2021 6 (22), 14533-14541, DOI: 10.1021/acsomega.1c01517 

[^2] Xie, T. and Grossman, J., 2018. Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties. Physical Review Letters, 120(14).
           
           
           

