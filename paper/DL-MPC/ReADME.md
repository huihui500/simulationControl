# paper

## professinal
###  non-predictive control strategies:
- TODO
- question: cannot account for acuation constraints


###  end to end controller learning:
- TODO
- require large datasets to train and do not allow for tuning without costly retraining

### Learned Dynamics Models
> Model complex dynamics

### individual SQP(序列二次规划)

### Learned Controllers
> Although such approaches achieve high control frequencies, they require large datasets to train, do not allow for tuning without costly retraining, and inevitably discard optimality, robustness and generalizability of the MPC framework, especially when deployed on outof-distribution data

## Abstract
- key: 神经网络作为dynamics model;
- experiments: simulation and real world
- index: positional tracking error
  

## Introduction
## question
  - naive integration of neural network would lead to extensive optimization times
  - 适合　slow dynamic ma
  - 最近的研究:combine learned dynamics represented by Gaussian Processes (GP) with MPC: **poorly to large datasets**

## work
> Our work: replaces the Gaussian Process dynamics of [11], [12] with deep neural networks 

> uses gradient-based optimization as opposed to a sampling-based scheme [22]. 

> Compared to [23], locally approximate the learned dynamics using a second-order Taylor approximation, which allows scaling the learned dynamics model beyond simple two-layer MLPs without compromising accuracy.


- The framework allows the integration of **arbitrary neural network architectures as dynamics constraints(神经网络作为动力学约束)** into the MPC formulation by leveraging (GPU-)parallelized computation of Jacobians and Hessians provided by deep learning libraries.
- three keys:
  - formulate the computational paradigm(范例) for Neural-MPC
  - describe and provide an open, extensible and free-to-use implementation of the Neural-MPC paradigm 
  - evaluate our approach on multiple simulation-based and real-world experiments using a high speed quadrotor in aggressive and close-to-obstacle maneuvers
