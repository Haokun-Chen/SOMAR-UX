---
title: 'User Stories'
order: 2
---
When researchers and scientists interested in modeling ocean:

- to launch SOMAR, they could either: <br/>
    - 1) User write C++ code in a setICs() method to configure starting parameters OR <br/>
    - 2) User provides a input text file that contains paramaters and set the file as argument to when launching SOMAR OR<br/>
    - 3) User write Python code in a predefined method or interface to provide or overwrite starting parameters.
- When they want to subset or integrate output data, they could:
    -  configure Python post-processing script to get preferred data

- SOMAR launches and simulate ocean behaviors given the parameters
- User will get output written in "hdf5_output" folders which contains multiple distributed hdf5 data files that represents specfic data values (velocity, etc.) in a certain region.
- Post Processing script execute to produce user-defined computation and output preferred data