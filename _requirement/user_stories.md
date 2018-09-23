---
title: 'User Stories'
order: 2
---
- Currently user has two ways to launch SOMAR: <br/>
1) Configure a setICs() method in C++ code or <br/>
2) setup input paramaters in a file and upload the file to SOMAR

- Then user will get output written in hdf5_output folders which contains distrubuted hdf5 data files. 

This project aims to add a third way for users to configure and launch SOMAR:
<br/><br/>
After discussion, we decide to embed Python into C++ code and call Python interpreter from C++ and launch the setup process.
This Python setup process could potentially:<br/>
1.  Communicate with each SOMAR instance to provide the correct input parameters configuration
2.  Run mpipy to communicate among all Python process in each SOMAR instance to produce the correct input parameters files, which could be upload to SOMAR later to launch the computation

Before launching SOMAR, user could also configure a postprocessing script with Python to get the data they want in the right form.
This conclude the user flow