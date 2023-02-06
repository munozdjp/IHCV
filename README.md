<p align="center">

# HINNDy

## Hidden Identification of Nonlinear Normal form Dynamics 

A compilation of HINNDy Matlab implementations described in a research article. The implementation resembles those suggested in the paper. I've chosen to concentrate on having every implementation and detail correct.

* [Summary](#Summary)
* [Code](#Code)

# HINNDy Workflow

![Figure 1](https://user-images.githubusercontent.com/67231886/216912664-756a10b7-17a0-409c-a038-4d578cd2d85d.png)

# Summary

#### Authors
Juan Pablo Munoz Diaz,..., David Gomez Cabrero, Narsis Kiani, Jesper tegner

#### Abstract

Here we explore the idea of using normal forms as universal, scalable, and minimal dynamical building blocks to capture and model the system dynamics. Our method, called HINNDy, samples observations in the vicinity of a slow manifold and formulate the problem to a constrained opti- mization problem. We evaluate performance, robustness against noise, and data requirements by benchmarking HINNDy against standard bifurcation models (Saddle-node, Transcritical, Pitchfork, Hopf). Next, we tested HINNDy for the discovery of Lorentz, Van Der Pol, the Hodgkin-Huxley, and Fitzhugh-Nagumo dynamical systems from data generated by these models.

For additional information, please refer to the [Publication](https://github.com/munozdjp/HINNDY/tree/main/HINNDy__Code)

  
# Code
  
MATLAB-2020.

Download the [Folder](https://github.com/munozdjp/HINNDy-/tree/main/HINNDy__Code), run each script in the specific directory. 

```
# set working dir
cd HINNDy__Code/<script>
```

The scripts generates the results for: 
  * Prediction of Learned Variable: a figure including the learned variable and the ground truth. 
  * Noise analysis: a figure with the performance of HINNDy under the influence of noise with 5 different parameters. 

These are the following scripts that you can find on this GitHub:

1- [Saddle-node bifurcation:](https://github.com/munozdjp/HINNDy-/blob/main/HINNDy__Code/SaddleNodeLeft2Rigth.m): prediction for switching fix point. 
  
2- [Pithchfork-bifurcation:](https://github.com/munozdjp/HINNDy-/blob/main/HINNDy__Code/Hopf_fit_withobservedVariablesNonNormal.m): prediction for growing fix point dynamic.

3- [Hopf-Bifurcation:](https://github.com/munozdjp/HINNDy-/blob/main/HINNDy__Code/Hopf_fit_withobservedVariablesNonNormal.m): learned hidden variable on oscillator to fixpoint dynamic. 

4- [Hodgkin-Huxley](https://github.com/munozdjp/HINNDy-/blob/main/HINNDy__Code/hodg_Hux_fit_ObservedVariables.m): learned hidden variable on voltage discharge on neuron dynamic. 

5- [FitzHugh-Nagumo](https://github.com/munozdjp/HINNDy-/blob/main/HINNDy__Code/Fitz_Nagumo2th_fit_ObservedVariables.m): learned hidden variable on nerve cell resonant regime. 

# Contributing
Simply fork the repository and make the appropriate changes to contribute to HINNDy. Once complete, send a pull request and we will evaluate your contributions.

# License
HINNDy is the GOV License. Refer to LICENSE for additional details.



