
# Phonon Dispersion Prediction

## Manual

### Background
Phonons are massless quantum mechanical particles that are formed due to atomic vibrations within the crystal lattice. The importance of studying phonons is a significant number of physical properties, such as Raman scattering spectra, thermal expansion, and heat conduction can be explained using phonons [^1]. The phonon dispersion is the relationship between the k-space and the frequencies of normal modes for all the optical and acoustic branches of lattice vibrations in a selected direction in the crystal. The number of branches is equal to the number of degrees of freedom of the unit cell [^2]. Computational prediction of phonon dispersion patterns can help to evaluate the dynamic stability of a hypothetical material structure. Generally, the stability of a material in terms of the lattice dynamics is examined by verifying whether all the normal vibrational modes have a real and finite frequency within the first Brillouin zone [^3]. 

### Prediction method

Recently, we have developed a graph neural network based phonon Density of States(DOS) prediction algorithm using our recent scalalbe DeeperGATGNN algorithm.


### How to use the app:

1. Load a cif structure
2. click "Predict Now"
3. Collect the results


### Interpretion of results

TBD


### Citations

To cite the Phonons Predictor App, please reference the following works:



[^1]:   Phonons, Theory in CASTEP, BIOVIA Materials Studio, Retrieved January 30, 2022, from https://www.tcm.phy.cam.ac.uk/castep/documentation/WebHelp/content/modules/castep/thcastepphonon.htm
[^2]: K. Parlinski, Lattice Dynamics: Vibrational Modes, Elsevier, 2005, 98-102, ISBN 9780123694010, https://doi.org/10.1016/B0-12-369401-9/00509-X
[^3]: Lakdja, A. (2014). Structural and phonon dynamical stability of the hypothetical RBN and CSN compounds. Computational Materials Science, 89, 1–5. https://doi.org/10.1016/j.commatsci.2014.03.027 


### Authors

- Dilanga Siriwardane
