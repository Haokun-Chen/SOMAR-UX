---
title: 'Functional Specification'
order: 1
---
Initial requirements:
- Get mpipy/somar working with 1 MPI version. 
- Make a Boxlib-style data holder variant for mpipy that can be transferred among python / SOMAR. (See: LevelData class in Chombo documentation) 
- Launch the SOMAR C++ solver from the Python interface. 
- Make a python interface that takes charge of input file parameters. 
 

Stretch Goals: 
  
1.  Expand the python API to make domain decomposition simple. 
2.  Make the data holder work like a numpy array so that we can easily fill it with data. (Example: u = sin(x) where both x and u are the decomposed data holders.) 
3. run SOMAR just as we always have and give it the ability to call a python routine