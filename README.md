# Parallelized FDTD Computional Electromagnetics for 3-Dimensional Inverse Design Problems

## _Abstract_

As the increasing demand for highly efficient optical components for the optical communications as well as more complex optical systems for Augmented Reality(AR) and Virtual Reality(VR), using simple and intuitive geometries of nanophotonics designs or metasurface desgins to imporve the efficicency of optical components or to achieve specific funcationalies of opticl systems become very difficult since these approaches only explore a small fraction of the possible design. The inverse design problem using **_adjoint method_**[1], which uses gradient-based optimization methods, is a promising method that provides an efficient approach to explore the entire space of possible designs and has been used to demonstrate devices that have better efﬁciencies and novel functionalities. Although this method greatly reduces the computional expense of an electromagnetic simuation, _the entire parameter searching space is still large so that most of the current researches fixed the thickness of their designs to simplify their 3-dimensional problem to a 2-dimensional probelm or using a preodic boundary constraint to reduce their design space._ However, _fixing the thickness of a desgin or limiting a desgin to be a preodic nanostructure still limit the opportunity to explore more possible designs that might have higher efficiencies and more advanced functionalities._

In this proposal, the parallel computing technique will be applied on a general 3-dimensional FDTD electromagnetic inverse desgin problem. By doing the spatial decomposition on an inverse desgin probelm, the entire simulation can be divided into several subproblems, in which each subproblems can be solved parallely and might have enough computional resources to explore the thickness parameter in a 3-dimensional problem. In addition to a lower computional expense, notice that there is no preodic boundary constraint applied here indicating that an entire space of possible designs can be explored. 

This new application of parallel computing on a 3-dimensional FDTD electromagnetic inverse desgin problem can be applied to not only on the design of optical components for the optical communications, but also on the design of complex optical systems for Augmented Reality(AR) and Virtual Reality(VR). The previous undiscovered possible designs that might have higher efficiencies and more advanced functionalities can be explored after applying the parallel computing. A even larger scale electromagnetic inverse design probelm can also be explored by the combination of hybrid MPI, OpenMP, and CUDA.


![alt text]/Users/tsehsien/Desktop/Git_Repository/USC_CSCI596_Fall2020_Final_Project/Screen Shot 2020-11-21 at 9.37.10 PM.png

![alt text]https://support.lumerical.com/hc/article_attachments/360057318913/inverse_design_y_branch_initialshape.png

## _Specific Objectives:_
1. A series version of a 3-Dimensional Inverse Design Problems with adjoint method wriiten in C language.
2. The spatial decomposition of a series version problem, with the discuss of what cut-off length of each cell shoule be considered.
3. The variation of grib sizes on different simulation cells might be possible. (fine grib size for high reflective index materials and coarse grib size for low reflective index materials) 
   
 ## _Task List:_
   - [x] Working on a series version of a 3-Dimensional Inverse Design Problems with adjoint method wriiten in C language.
   - [ ] What cut-off length of each cell shoule be considered?
   - [ ] The variation of grib sizes on different simulation cells.

## _Reference:_



