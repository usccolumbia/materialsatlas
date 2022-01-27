
# Similar Structure Finder
#### Dr. Hu

## Manual

### Background 

Tinkering and doping are two common ways to optimize an existing material or find a better alternative. This web app helps the users to find chemically and structurally similar materials for a query material. 

### The structure similarity search Method

We use the computed XRD diffraction vector as the descriptors for representing crystal structures and compute their similarity. This representation has been used to search new materials using clustering algorithm. 



### Performance and Limitations

For each query structure, the current algorithm needs to calcualte pairwise distance to almost 130,000 structures, which is too time-consuming. 

### Using the Similar structure Finder

#### Entering Inputs

Practically, the procedure consists in 3 steps

1. upload a cif structure file
2. inpuy how many top structures you want to return
3. click "search now" button
4. get results or download the result file.

#### Interpreting the Results

The result contains the returned top N formulas and the distance scores.

### Future features

New algorithms are being developed to significantly speed up the retrieval process. 

### Citations

To cite the similar Structure finder App, please reference the following works:

- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Zhang, Y., He, X., Chen, Z., Bai, Q., Nolan, A.M., Roberts, C.A., Banerjee, D., Matsunaga, T., Mo, Y. and Ling, C., 2019. Unsupervised discovery of solid-state lithium ion conductors. Nature communications, 10(1), pp.1-7.

### Authors

- Dr. Jianjun Hu
