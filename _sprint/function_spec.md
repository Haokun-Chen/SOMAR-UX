---
title: 'Functional Specification'
order: 1
---
Initial functional requirements:
- Launch the Python interpreter and Python setup methods that user writes from C++ code to start SOMAR
- Get mpipy/somar working with 1 MPI version. 
- Make a Boxlib-style data holder variant for mpipy that can be transferred among python / SOMAR. 
    - (See: LevelData class in Chombo documentation) 

Stretch Goals: 
-  Expand the python API to make domain decomposition simple. 
- Make the data holder work like a numpy array so that we can easily fill it with data. 
    - (Example: u = sin(x) where both x and u are the decomposed data holders.) 