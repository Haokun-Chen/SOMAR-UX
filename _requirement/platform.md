---
title: 'Platform Analysis'
order: 4
---
- SOMAR is written in C++ and uses mpi for parrallel computing, which depends on Chombo 3.1 for calculation and uses hdf5 1.8.10 data format. 

- The project is going to write a Python interface. The Python interpreter is launched inside the C++ code in SOMAR and runs user-defined Python script. The return value will be passed back to C++ code to fill the actual data points and further launch SOMAR.