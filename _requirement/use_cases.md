---
title: 'Use Cases'
order: 7
---
Configuring and launching SOMAR: 
- in "LockExchange.cpp":
    - setICs() method: C++ code to configure the initial conditions for launching SOMAR, which launches python interpreters, and pass in parameters including:
        - Lo and hi boundary of the region
        - Box length, self-facing vs. side-facing, isPeriodic domain
        - Dimension
        - Componenets vectors
    - setup.py: Python interface that allows users to write Python code to configure initial conditions data
        - construct a numpy array that of the same dimensions to store initial componenets data
    - Compile SOMAR using make file
    - post-process.py: Python script that allows users to write Python code to subset, integrate, or filter output data from SOMAR