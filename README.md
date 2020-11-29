# Parallelized FDTD Computional Electromagnetics for 3-Dimensional Inverse Design Problems

## _Abstract_

As the increasing demand for highly efficient optical components for the optical communications as well as more complex optical systems for Augmented Reality(AR) and Virtual Reality(VR), using simple and intuitive geometries of nanophotonics designs or metasurface desgins, as figure 1 shown, to imporve the efficicency of optical components or to achieve specific funcationalies of opticl systems become very difficult since these approaches only explore a small fraction of the possible design.<sup>[1,2]</sup> The inverse design problem using **_adjoint method_**<sup>[3,4]</sup>, which uses gradient-based optimization methods, is a promising method that provides an efficient approach to explore the entire space of possible designs and has been used to demonstrate devices that have better efﬁciencies and novel functionalities. _Although this method greatly reduces the computional expense of an electromagnetic simuation, _the entire parameter searching space is still large so that most of the current researches **fixed the thickness of their designs to simplify their 3-dimensional problem to a 2-dimensional probelm<sup>[5,6]</sup> or using a preodic boundary constraint<sup>[7,8]</sup>** to reduce their design space._ _However, **fixing the thickness of a desgin, starting from a 2-dimensional reulst and exploring the same question in the third dimension, or limiting a desgin to be a preodic nanostructure still limit the opportunity to explore more possible designs** that might have higher efficiencies and more advanced functionalities._

![Figure 1](https://support.lumerical.com/hc/article_attachments/360057318913/inverse_design_y_branch_initialshape.png)

![alt text](https://www.lumerical.com/drive/uploads/2020/02/PID_03-600x363.png)

In this proposal, the parallel computing technique will be applied on a general 3-dimensional FDTD electromagnetic inverse desgin problem. By doing the spatial decomposition on an inverse desgin probelm, the entire simulation can be divided into several subproblems, in which each subproblems can be solved parallely and might have enough computional resources to explore the thickness parameter in a 3-dimensional problem. In addition to a lower computional expense, notice that there is no preodic boundary constraint applied here indicating that an entire space of possible designs can be explored. 

This new application of parallel computing on a 3-dimensional FDTD electromagnetic inverse desgin problem can be applied to not only on the design of optical components for the optical communications, but also on the design of complex optical systems for Augmented Reality(AR) and Virtual Reality(VR). The previous undiscovered possible designs that might have higher efficiencies and more advanced functionalities can be explored after applying the parallel computing. A even larger scale electromagnetic inverse design probelm can also be explored by the combination of hybrid MPI, OpenMP, and CUDA.


## _Specific Objectives:_
1. A series version of a 3-Dimensional Inverse Design Problems with adjoint method wriiten in C language.
2. The spatial decomposition of a series version problem, with the discuss of what cut-off length of each cell shoule be considered.
3. The variation of grib sizes on different simulation cells might be possible. (fine grib size for high reflective index materials and coarse grib size for low reflective index materials) 
   
 ## _Task List:_
   - [x] A series version of a 3-Dimensional Inverse Design Problems using adjoint method wriiten in C language.
   - [ ] What cut-off length of each cell shoule be considered?
   - [ ] The variation of grib sizes on different simulation cells.

## _Reference:_
[ [1] Inverse design in nanophotonics, Sean Molesky, Zin Lin, Alexander Y. Piggott, Weiliang Jin, Jelena Vučković, Alejandro W. Rodriguez. Nature Photonics volume 12, pages 659–670 (2018)](http://web.stanford.edu/group/nqp/jv_files/papers/molesky2018inverse.pdf)

[ [2] Nanophotonic Inverse Design with SPINS: Software Architecture and Practical Considerations, Logan Su, Dries Vercruysse, Jinhie Skarda, Neil V. Sapra, Jan A. Petykiewicz, Jelena Vučković](https://aip.scitation.org/doi/10.1063/1.5131263)

[ [3] Photonic Design: From Fundamental Solar Cell Physics to Computational Inverse Design, Owen Dennis Miller](http://optoelectronics.eecs.berkeley.edu/ThesisOwenMiller.pdf)

[ [4] Adjoint shape optimization applied to electromagnetic design, Christopher M. Lalau-Keraly, Samarth Bhargava, Owen D. Miller, and Eli Yablonovitch](https://www.osapublishing.org/oe/fulltext.cfm?uri=oe-21-18-21693&id=260994)

[ [5] Inverse Design and Demonstration of a Compact on-Chip Narrowband Three-Channel Wavelength Demultiplexer, Logan Su, Alexander Y. Piggott, Neil V. Sapra, Jan Petykiewicz, and Jelena Vučković](http://web.stanford.edu/group/nqp/jv_files/papers/su_acsphotonics_10_1021.pdf)

[ [6] Inverse design and demonstration of a compact and broadband on-chip wavelength demultiplexer, Alexander Y. Piggott, Jesse Lu, Konstantinos G. Lagoudakis, Jan Petykiewicz, Thomas M. Babinec and Jelena Vučković](http://web.stanford.edu/group/nqp/jv_files/papers/inverse_design_wdm.pdf)

[ [7] Periodic Dielectric Metasurfaces with High-Efficiency, Multiwavelength Functionalities, David Sell, Jianji Yang, Sage Doshay, and Jonathan A. Fan](https://fanlab.stanford.edu/wp-content/papercite-data/pdf/sell2017periodic.pdf)

[ [8] High-efficiency, large-area, topologyoptimized metasurfaces, Thaibao Phan, David Sell, Evan W. Wang, Sage Doshay, Kofi Edee, Jianji Yang and Jonathan A. Fan](https://fanlab.stanford.edu/wp-content/papercite-data/pdf/phan2019high.pdf)


