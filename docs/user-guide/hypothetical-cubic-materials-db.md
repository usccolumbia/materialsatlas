
# Hypothetical Cubic Materials Database

#### by Dr. Jianjun Hu

## Manual

### Background 
Cubic materials such as perovskites are playing a critical role in many applications such as batteries and electric vehicles. This database aims to collect hypothetical cubic crystal materials structures generated from our generative models of crystal structures.


### The Database Generation Method

We use both crystal structure generator algorithms such as CubicGAN [^1] or physics guided generator [^2], or composition generator such as MATGAN [^3] plus crystal structure prediction algorithms to generate new crystal mateials candidates. The algorithm is based on the generative adversarial network which learns a generator and a discriminator, both are convolution networks. The model is trained with the crystal structures from the materials project database. For the cubicGAN, we only consider three cubic space groups including 221, 225, 216. For the physics guided generator, we include 20 space groups [^2]. 


### Performance and Limitations

In our CubicGAN model, we only consider three space groups 221,225,216 and only consider crystal structures of which the fractional coordinates are the multiples of 0.25. For the physics guided generator, we include 20 space groups without the fractional coordinate constraints. Our CubicGAN has recovered most of known cubic structures after training. The performance is here: 

<img src="cubic.png" width=500>


### Using the cubic strucgture Search function

#### Entering Inputs

Practically, the procedure for getting predictions consists in 3 steps

1. Pick elements: Select on the periodic table what constituent elements comprise the chemical space you are interested in.
   For instance if you want to make predictions for battery materials based on Li, Mn and O, you should pick those three elements.
2. After the results are returned, you can further narrow down the search by typing in the top right input box with more specific partial formula, e.g. Li2
3. Interpret the results.
   

#### Interpreting the Results

The results pages provides a set of potential cubic compound materials. Users can also check the crystal structure using the built-in jmol viewer.
You can also download the cif files of the results or do some structure based property prediction using our other web apps. 


### Future features

In the future, we want to generate more cubic crystal materials candidates.

### Citations

To cite this App, please reference the following works:

- Zhao, Yong, Mohammed Al-Fahdi, Ming Hu, Edirisuriya Siriwardane, Yuqi Song, Alireza Nasiri, and Jianjun Hu. "High-throughput discovery of novel cubic crystal materials using deep generative neural networks." arXiv preprint arXiv:2102.01880 (2021).
- Hu, J., Stefanov, S., Song, Y., Omee, S. S., Louis, S. Y., Siriwardane, E., & Zhao, Y. (2021). MaterialsAtlas. org: A Materials Informatics Web App Platform for Materials Discovery and Survey of State-of-the-Art. arXiv preprint arXiv:2109.04007.

[^1]: Zhao, Yong, Mohammed Al-Fahdi, Ming Hu, Edirisuriya Siriwardane, Yuqi Song, Alireza Nasiri, and Jianjun Hu. "High-throughput discovery of novel cubic crystal materials using deep generative neural networks." arXiv preprint arXiv:2102.01880 (2021).
[^2]: Zhao, Yong, Edirisuriya Siriwardane, and Jianjun Hu. "Physics guided deep learning generative models for crystal materials discovery." arXiv preprint arXiv:2112.03528 (2021).
[^3]: Dan, Y., Zhao, Y., Li, X., Li, S., Hu, M., & Hu, J. (2020). Generative adversarial networks (GAN) based efficient sampling of chemical composition space for inverse design of inorganic materials. npj Computational Materials, 6(1), 1-7.




### Authors

- Jianjun HU


