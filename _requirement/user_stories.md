---
title: 'User Stories'
order: 3
---
When researchers and scientists interested in modeling ocean:

- Step 1: to configure SOMAR, users need to do the following <br/>
    - 1) User provides a input text file to set metadata about the models and pass in as command-line argument<br/>
    - 2a) User write C++ code in a setICs() method to configure starting parameters OR <br/>
    - 2b) User write Python code in a predefined method or interface to provide or overwrite starting parameters.
- Step 2: When they want to subset or integrate output data, they could:
    -  configure Python post-processing script to get preferred data

- Step 3: SOMAR launches and simulate ocean behaviors given the parameters
- Step 4: User will get output written in "hdf5_output" folders which contains multiple distributed hdf5 data files that represents specfic data values (velocity, etc.) in a certain region.
- Step 5: Post Processing script execute to produce user-defined computation and output preferred data