---
title: 'Platform Analysis'
order: 4
---
- SOMAR is written in C++ and uses mpi for parrallel computing, which depends on Chombo 3.1 for calculation and uses hdf5 1.8.10 data format. 

- The project is going to write a Python interface. The Python interpreter is launched inside the C++ code in SOMAR and runs user-defined Python script. This only requires the usage of Python-C API to create Python interpreter, configure Python parameters and call Python functions. **The integration of Python into C++ requires one to include the Python header file "Python.H" into C++ code.**