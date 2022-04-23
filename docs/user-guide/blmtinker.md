

# BLMTinker
#### Dr. Hu

## Manual

### Background 

Tinkering and doping are two common ways to optimize an existing material or find a better alternative. This web app allows the users to mask a material formula and recommend substition elements. It can then be used as materials doping suggestion to tinkering materials design.

### The BLMM tinkering material design Method

We use the BLMM crystal transformer model as defined in our paper [^1] to implement our app.  



### Performance and Limitations



### Using the composition enumerator

#### Entering Inputs

Practically, the procedure consists in 3 steps

1. Input a material formula
2. mask one or more atoms in the formula
3. click "Predict/Fill blank"
4. predict the substitution elements for each positions
5. get the suggested formula and a probability distriution of possible substition elements for each masked position.

#### Interpreting the Results

The result contains the recommended element substitutions.

### Future features

TBD

### Citations

If you use this app, please reference the following works:

- Lai Wei, Qinyang Li, Yuqi Song, Stanislav Stefanov, Edirisuriya Siriwardane, and Jianjun Hu. "Crystal Transformer: Self-learning neural language model for Generative and Tinkering Design of Materials." arXiv preprint arXiv:2109.04007 (2022).



[^1]: https://www.materialsatlas.org/blmtinker

### Authors

- Dr. Jianjun Hu
