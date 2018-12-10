---
title: 'Project Concept'
order: 1
---
The purpose of this project is to improve user experience for SOMAR so that users are easier to configure and launch experiments with SOMAR. 

- Previously, to start the experiment, users need to configure the ocean region boundaries and other initial physical conditions such as velocity, pressure, buoyancy and etc. This configuration is done in two places: 
    - **The first place** is an input file determining some metadata about the experienment such as the dimension, ocean region boundaries, sizes, and other metadata to define the experiment. 
    - **The second place** is inside a setICs() function in SOMAR, which enables users to fill actual data and properties for specific regions or coordinates in the pre-defined experiment. 

- This project now aims to replace the **second place to configure initial data with Python script**. This will require the C++ setICs() function to call a **Python interpreter**, and **pass relavant metadata as parameters** that users need to fill actual data points. The Python script will receive the metadata as parameters, **construct multi-dimentional arrays** to share same memory space as the data strucutre in C++ to hold data in specific regions. Then the user can write Python code to fill those data inside the arrays according to the conditions provided by the metadata and function parameters. Eventually, the data filled in Python is directly filled in C++ Box object because they share same memory space. This completes the configuration and the C++ code continues to run to launch SOMAR.