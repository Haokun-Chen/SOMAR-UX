---
title: 'Use Cases'
order: 6
---
Configuring and launching SOMAR: 
- in "LockExchange.cpp":
    - setICs() method: C++ code iterate each data points represented by Boxes Object, and **for each data point**, C++ launches python interpreters, and **pass in parameters to fill the Box object** including:
        - Lo and hi boundary of the region
        - Box length, self-facing vs.side-facing, isPeriodic domain
        - Dimension
        - Componenets vectors representing the properties of the Box object such as velocity
        - Physical position(coordinates) of the Box object
    - setup.py: Python interface that allows users to write Python code to configure initial conditions data
        - construct a numpy array that of the same dimensions to store initial componenets data
    - Compile SOMAR using make file
    - post-process.py: Python script that allows users to write Python code to subset, integrate, or filter output data from SOMAR