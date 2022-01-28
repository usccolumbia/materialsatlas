
# Materials Hardness Predictor


#### by Dr. Hu

## Manual

### Background

Hardness is a materials property with wide applications such as machine tools and electronics. A variety of machine learning models have been developed with both composition and structural desriptors for thermal conductivity prediction as reviewed in [^1]. However, the key challenge of thermal conductivity prediction is the limited number labelled data samples. Quite a few studies have used from 80 to <200 labelled samples and demonstrated good (over-estimated) performance, which only interploate well within their highly redundant data set. Here we trained  composition based and structure based (using graph neural networks) thermal prediction models using a dataset with ~2700 samples [^2] with calculated thermal conductivity. 


### The Materials Hardness Prediction methods



#### The composition based hardness prediction model

Our composition model is trained using the Magpie descriptors from the Matminer package [^3] together with the Roost neural network model [^4]. 

#### The deep graph neural network model for hardness prediction

Our structure based hardness prediction model is based on our latest work of DeeperGATGNN algorithm [^5], which is a scalable deep graph neural network model with the state-of-the-art performance for structure based materials property prediction. 

### Performance and Limitations

The MAE of our composition ML model on the hold-out test set is xxxxx. 
The MAE of our structure ML model on the hold-out test set is xxxxx. 

### Using the Hardness Predictor

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


[^1]: Mansouri Tehrani, Aria, Anton O. Oliynyk, Marcus Parry, Zeshan Rizvi, Samantha Couper, Feng Lin, Lowell Miyagi, Taylor D. Sparks, and Jakoah Brgoch. "Machine learning directed search for ultraincompressible, superhard materials." Journal of the American Chemical Society 140, no. 31 (2018): 9844-9853.
[^2]: http://www.materialsproject.org
[^3]: https://hackingmaterials.lbl.gov/matminer/matminer.featurizers.composition.html?highlight=magpie
[^4]: https://github.com/CompRhys/roost
[^5]:Omee, Sadman Sadeed, Steph-Yves Louis, Nihang Fu, Lai Wei, Sourin Dey, Rongzhi Dong, Qinyang Li, and Jianjun Hu. "Scalable deeper graph neural networks for high-performance materials property prediction." arXiv preprint arXiv:2109.12283 (2021).
[^6]: Avery, Patrick, Xiaoyu Wang, Corey Oses, Eric Gossett, Davide M. Proserpio, Cormac Toher, Stefano Curtarolo, and Eva Zurek. "Predicting superhard materials via a machine learning informed evolutionary structure search." npj Computational Materials 5, no. 1 (2019): 1-11.
[^7]: Mazhnik, Efim, and Artem R. Oganov. "Application of machine learning methods for predicting new superhard materials." Journal of Applied Physics 128, no. 7 (2020): 075102.


### Authors

- Jianjun Hu

