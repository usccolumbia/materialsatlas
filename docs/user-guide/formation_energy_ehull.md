# Formation Energy and E-above-hull Check
#### by Dilanga Siriwardane

# Manual
## Formation Energy 
### Background

The formation energy of a material defines the energy required to dissociate that material into its respective elements. Thus, it indicates the thermodynamic stability against the elements it consists of. Usually, the density functional theory (DFT) based first-principles calculations are performed to calculate the formation energy. It is required to identify the crystal structure data in advance for that purpose. However, the ground state structures are unknown for most of the compositions. Therefore, it is difficult to determine the formation energy of a new composition using DFT. Another disadvantage of the above method is that the first-principles calculation of formation energy is time-consuming and expensive [^1]. As a solution, machine learning models are trained based on the elemental and electronic properties of the available compositions in the materials databases. It should also be mentioned that a higher accuracy for predicting formation energy can be achieved using the graph neural networks if the crystal structure is available. This is a very important tool if we want to find the formation energy of a material when the energy information is not accessible [^2] [^3]. Therefore, we provide both composition-based and structure-based options for predicting the formation energy using MaterialsAtals.org. You can submit either the cif file of the crystal structure or the chemical formula to obtain the predictions.

### Composition-based Model
Our composition-based model is trained using the Magpie descriptors from the Matminer package[^4] together with the Roost neural network model [^5]. 

### Structure-based Model
Our structure based LTC prediction model is based on our latest work of DeeperGATGNN algorithm [^6], which is a scalable deep graph neural network model with the state-of-the-art performance for structure based materials property prediction.

### Using the Formation Energy Predictors

1. Upload the .cif file or enter the reduced chemical formula in the text box.
2. Press 'Check Now' button.


## Energy-Above-Hull

### Background

Formation energy indicates only whether the material is stable with respect to the parent materials of each element. However, after synthesizing the material, it can decompose to a combination of other competing phases. If the material is thermodynamically stable, the energy above the hull must be equal to zero. In MaterialsAtals.org, we provide a tool to compute energy above hull employing the DFT energies of the target material and competing phases. Here, we use the pymatgen code to compute energy-above-hull [^7][^8].

### Using the Energy-Above-Hull Calculator
1. Mention the formula and the corrected energy per atom obtained from DFT in the text box. Please refer ref. [^9] for more information. 
2. Press 'Check Now' button.


### Citations
[^1]: Mao, Y., Yang, H, Sheng, Y., Wang, J., Ouyang, R., Ye, C., Yang, J. and Zhang, W. Prediction and Classification of Formation Energies of Binary Compounds by Machine Learning: An Approach without Crystal Structure Information, ACS Omega, 2021 6 (22), 14533-14541, DOI: 10.1021/acsomega.1c01517 

[^2]: Xie, T. and Grossman, J., Crystal Graph Convolutional Neural Networks for an Accurate and Interpretable Prediction of Material Properties, Physical Review Letters,  2018, 120(14).
           
[^3]: Louis,S., Zhao, Y., Nasiri, A., Wang, X., Song, Y., Liu, F.  Hu, J., Royal Society of Chemistry (RSC), Physical Chemistry Chemical Physics, 2020, 18141-18148, DOI: 10.1039/d0cp01474e

[^4]: Ward, L., Dunn, A., Faghaninia, A., Zimmermann, N. E. R., Bajaj, S., Wang, Q., Montoya, J. H., Chen, J., Bystrom, K., Dylla, M., Chard, K., Asta, M., Persson,
K., Snyder, G. J., Foster, I., Jain, A., Matminer: An open source toolkit for materials data mining. Comput. Mater. Sci. 152, 60-69 (2018).

[^5]: Goodall, R.E.A., Lee, A.A. Predicting materials properties without crystal structure: deep representation learning from stoichiometry. Nat Commun 11, 6280 (2020). https://doi.org/10.1038/s41467-020-19964-7

[^6]: Omee, Sadman Sadeed, Steph-Yves Louis, Nihang Fu, Lai Wei, Sourin Dey, Rongzhi Dong, Qinyang Li, and Jianjun Hu. "Scalable deeper graph neural networks for high-performance materials property prediction." arXiv preprint arXiv:2109.12283 (2021).

[^7]: Ong, S. P.; Wang, L.; Kang, B.; Ceder, G. Li−Fe−P−O2 Phase Diagram from First Principles Calculations, Chem. Mater., 2008, 20, 1798–1807, doi:10.1021/cm702327g.

[^8]: Ong, S. P.; Jain, A.; Hautier, G.; Kang, B.; Ceder, G. Thermal stabilities of delithiated olivine MPO4 (M=Fe, Mn) cathodes investigated using first\ principles calculations, Electrochem. commun., 2010, 12, 427–430, doi:10.1016/j.elecom.2010.01.010.

[^9]: https://pymatgen.org/pymatgen.analysis.phase_diagram.html

           

