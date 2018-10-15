---
title: 'Functional Specification'
order: 1
---
**Main project requirements:**
- The SOMAR backend is configured and launched with C++ code, the client wants to create a Python interface to allow users to configure and communicate with the backend and launch SOMAR.<br/>

**Additional project requirements:**
- Write a post processing script that allow users to filter, subset, integrate, or do other addtional operations on the output data.

Ohter functional requirements:
- Get mpipy/somar working with 1 MPI version.
- Make a Boxlib-style data holder variant for mpipy that can be transferred among python / SOMAR. 
    - (See: LevelData class in Chombo documentation) 

Stretch Goals: 
-  Expand the python API to make domain decomposition simple. 
- Make the data holder work like a numpy array so that we can easily fill it with data. 
    - (Example: u = sin(x) where both x and u are the decomposed data holders.) 