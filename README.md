# Physics Informed Neural Networks

## Solving Time Independent Schrodinger Equation (TISE) in 1D



### Team Members

* Harsh Vardhan Singh	EP23BTECH11012
* Jaideep Nirmal A J	EP23BTECH11013
* Sarang Gund		EP23BTECH11025

Course Project for **EP4210 Computational Physics** in **Spring 2025** @ **IITH**



### Problem Statement

To train a Neural Network to solve TISE for particle in a box, given the boundary conditions and eigen number. If the energy eigenvalues were not known, how would the neural network have to be changed to find the eigenvalues also?



### Files

* `solve\_PDE\_NN.ipynb` demonstrates neural network as a PDE solver
* `Pinns\_Cp.ipynb` trains a neural network to solve TISE for particle in a box, given the boundary conditions and energy eigen value
* `Pinn\_multiple\_n.ipynb` train neural network for a list of eigen values



### Utility

A direct inference call to a pre-trained PINEE on the x-space and the eigen number solves the TISE in an efficient manner (Matrix multiplication is $\\approx O(N^{2.7}$). Using a numerical approach like Crank Nicolson, the complexity would be $O(N^3)$. Additionally, the PINN can be trained on a certain degree of discretization $dx$ and be used to predict the TISE solution in a xspace of different $dx$. This is not possible in traditional numerical methods



### Follow-up

If energy eigen values were not known, the NN should take a guess value as an additional input. Loss functions must be defined appropriately to learn the eigen value too. Details in `PINN\_Presentation.pdf`



