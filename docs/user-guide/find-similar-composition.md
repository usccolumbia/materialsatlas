
# Find similar compositions

## Manual

### Background 

Tinkering and doping are two common ways to optimize an existing material or find a better alternative. This web app helps the users to find chemically similar compositions for a query composition. 

### The composition similarity search Method

We use the Element Move Distance (ElMD) to calculate the similarity of the query formula and the 130,000 formulas of the Materials Project database and return the top most similary compositions. The ElMD distance is defined based on atomic chemical similarity as discussed in [^1] and here [^2].



### Performance and Limitations

For each query composition, the current algorithm needs to calcualte pairwise distance to almost 130,000, which is too time-consuming. So we have limited it to limited no. of checked samples. 

### Using the Similar composition Finder

#### Entering Inputs

Practically, the procedure consists in 4 steps

1. input formula
2. select database
3. select similarity metric
4. get results or download the result file.

#### Interpreting the Results

The result contains the returned top N formulas and the distance scores.

### Future features

New algorithms are beining developed to significantly speed up the query process. 

### Citations

To cite the Structure Predictor App, please reference the following works:

- Hargreaves, Cameron J., Matthew S. Dyer, Michael W. Gaultois, Vitaliy A. Kurlin, and Matthew J. Rosseinsky. "The earth mover’s distance as a metric for the space of inorganic compositions." Chemistry of Materials 32, no. 24 (2020): 10610-10620.
- Hu, Jianjun, Stanislav Stefanov, Yuqi Song, Sadman Sadeed Omee, Steph-Yves Louis, Edirisuriya Siriwardane, and Yong Zhao. "MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art." arXiv preprint arXiv:2109.04007 (2021).


[^1]: Hargreaves, Cameron J., Matthew S. Dyer, Michael W. Gaultois, Vitaliy A. Kurlin, and Matthew J. Rosseinsky. "The earth mover’s distance as a metric for the space of inorganic compositions." Chemistry of Materials 32, no. 24 (2020): 10610-10620.

[^2]: https://github.com/lrcfmd/ElMD
[^3]: 10.1021/cm100795d
[^4]: 10.1038/nmat1691

### Authors

- Dr. Jianjun Hu
