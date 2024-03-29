<p align="center">

[![DOI](https://zenodo.org/badge/340074964.svg)](https://zenodo.org/badge/latestdoi/340074964)

  
# IHCV

## Identification of Hidden Control Variables 


This repository contains the IHCV method applied to the different dynamical systems models.

* [Summary](#Summary)
* [Scripts](#Scripts)
* [Working example: saddle node](#Working-example-saddle-node)  
* [Contributing](#Contributing)
* [License](#License)



## Summary

#### Authors
Juan Pablo Munoz Diaz, Subash Balsamy, Juan P. Bernal, Ali Balubaid, Alberto Maillo, Vincenzo Lagani, David Gomez Cabrero, Narsis Kiani, Jesper Tegner

#### Abstract

Here we explore the idea of using normal forms as universal, scalable, and minimal dynamical building blocks to capture and model the system dynamics. Our method, called IHCV, samples observations in the vicinity of a slow manifold and formulate the problem to a constrained optimization problem. We evaluate performance, robustness against noise, and data requirements by benchmarking IHCV against standard bifurcation models (Saddle-node, Transcritical, Pitchfork, Hopf). Next, we tested IHCV for the discovery of Lorentz, Van Der Pol, the Hodgkin-Huxley, and Fitzhugh-Nagumo dynamical systems from data generated by these models.

For additional information, please refer to the [Publication](https://github.com/munozdjp/HINNDY/tree/main/IHCV__Code)

#### IHCV Workflow
![Figure 1](https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/IHCVWorkflow.png)


## Scripts
  
IHCV is entirely developed in MATLAB, tested version 2020. There is no limitation in OS and no specific computational requirement.

First, clone this repository and set the working directory:

```
#clone repository
git clone https://github.com/munozdjp/IHCV.git

# set working dir
cd IHCV__Code/<script>
```

Each script generates the results for:
  * Prediction of learned variable: a figure including the learned variable and the ground truth. 
  * Noise analysis: a figure with the performance of IHCV under the influence of noise with 5 different variances. 

The list of the scripts that you can find on this GitHub:

1- [Saddle-node bifurcation](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/SaddleNodeLeft2Rigth.m): prediction for switching fix point. 
  
2- [Pitchfork-bifurcation](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/Hopf_fit_withobservedVariablesNonNormal.m): prediction for growing fix point dynamic.

3- [Hopf-Bifurcation](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/Hopf_fit_withobservedVariablesNonNormal.m): learned hidden variable on oscillator to fixpoint dynamic. 

4- [Hodgkin-Huxley](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/hodg_Hux_fit_ObservedVariables.m): learned hidden variable on voltage discharge on neuron dynamic. 

5- [FitzHugh-Nagumo](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/Fitz_Nagumo2th_fit_ObservedVariables.m): learned hidden variable on nerve cell resonant regime. 

The extra scripts are complementary validation of IHCV method. 
  
Working example: saddle node 
----------------------------

The saddle node bifurcation is a dynamical system that shows a switching point dynamic, from a lower state to a high upper state. 

Here you can find the complete script of [saddle node](https://github.com/munozdjp/IHCV/blob/main/IHCV__Code/SaddleNodeLeft2Rigth.m) 
  
First, we need to define the static variables. We recommend using the default values:

```
%timestep
dt=0.1; 
%final time point
Initinterval = 16;
%initial time point
neg_inter = 0;
```  

The output is the following 5 figures:

**Fig 1:** shows the ground truth of the alpha polynomial dynamic.
  
<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig1_saddlenode.png" alt="My Image" style="width: 399px; height: 300px;">
    
**Fig 2:** state variable when a hidden variable changes over time.
  
<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig2_saddlenode.png" alt="My Image" style="width: 399px; height: 300px;">
  
**Fig 3:** state variable vs hidden variable, IHCV prediction. 
  
<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig3_saddlenode.png" alt="My Image" style="width: 646px; height: 300px;">

**Fig 4:** shows how IHCV works when there are different kinds of noise disturbances.
  
<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig4_saddlenode.png" alt="My Image" style="width: 619px; height: 300px;">
  
**Fig 5:** shows how one sample of noise was analyzed.    

<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig5_saddlenode.png" alt="My Image" style="width: 399px; height: 300px;">
  
**Fig 6:** error distribution for different noise samples.        

<img src="https://github.com/munozdjp/IHCV/blob/main/figures%20saddle%20node/fig6_saddlenodeV2.png" alt="My Image" style="width: 417px; height: 300px;">


## Contributing
Simply fork the repository and make the appropriate changes to contribute to IHCV. Once complete, send a pull request and we will evaluate your contributions.

## License
IHCV is licensed under the GNU License. Refer to LICENSE for additional details.
  

