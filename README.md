# Parallelized FDTD Computional Electromagnetics for 3-Dimensional Inverse Design Problems

## _Abstract_

As the increasing demand for highly efficient optical components for the optical communications as well as more complex optical systems for Augmented Reality(AR) and Virtual Reality(VR), using simple and intuitive geometries of nanophotonics designs or metasurface desgins to imporve the efficicency of optical components or to achieve specific funcationalies of opticl systems become very difficult since these approaches only explore a small fraction of the possible design. The inverse design problem using **_adjoint method_**[1], which uses gradient-based optimization methods, is a promising method that provides an efficient approach to explore the entire space of possible designs and has been used to demonstrate devices that have better efﬁciencies and novel functionalities. Although this method greatly reduces the computional expense of an electromagnetic simuation, the entire parameter searching space is still large so that most of the current researches fixed the thickness of their designs to simplify their 3-dimensional problem to a 2-dimensional probelm or using a preodic boundary constraint to reduce their design space. However, fixing the thickness of a desgin or limiting a desgin to be a preodic nanostructure might limit the opportunity to explore more possible designs that might have higher efficiencies and more advanced functionalities. 

In this proposal, I aim to utilize what I have learned in CSCI 596 to do the parallel computing on a 3-dimensional FDTD electromagnetic inverse desgin problem. By doing the spatial decomposition on an inverse desgin probelm, the entire simulation can be divided into several subproblems, in which each subproblems can be solved parallely and might have enough computional resources to explore the thickness parameter in a 3-dimensional problem. In addition to a lower computional expense, notice that there is no preodic boundary constraint applied here indicating that an entire space of possible designs can be explored. 

This new application of parallel computing on a 3-dimensional FDTD electromagnetic inverse desgin problem can be applied to not only on the design of optical components for the optical communications, but also on the design of complex optical systems for Augmented Reality(AR) and Virtual Reality(VR). The previous undiscovered possible designs that might have higher efficiencies and more advanced functionalities can be explored after applying the parallel computing. 

> Specific Objectives:
1. A series version of a 3-Dimensional Inverse Design Problems with adjoint method wriiten in C language.
2. Spatial decomposition of a series version problem, with the discuss of what cut-off length of each cell shoule be considered.


~~The world is flat.~~
