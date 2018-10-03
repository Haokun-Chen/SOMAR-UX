---
title: 'Platform Analysis'
order: 4
---
SOMAR is written in C++ and uses mpi for parrallel computing, which depends on Chombo 3.1 for calculation and uses hdf5 1.8.10 data format. The project is going to write a Python interface, which includes potentially using mpipy or numpy package to communicate with the SOMAR backend to give user contorl of the input and also post-processing.