---
title: 'Project Concept'
order: 1
---
The purpose of this project is to improve user experience for SOMAR so that users are easier to configure and launch experiments with SOMAR. 

- Previously, to start the experiment, users need to configure the ocean region boundaries and other initial physical conditions such as velocity, pressure, buoyancy and etc. This configuration is done in two places: 
    - **The first place** is an input file determining some metadata about the experienment such as the dimension, ocean region boundaries, sizes, and other metadata to define the model. 
    - **The second place** is inside a setICs() function in SOMAR, which enables users to fill actual data points and properties for specific regions and positions in the pre-defined model. 

- This project aims to replace the **second place to setup data points with Python script**. This will require the C++ setICs() function to call a **Python interpreter**, and **pass relavant metadata as parameters** that users need to fill actual data points. The Python script will receive the metadata as parameters, **construct multi-dimentional arrays** to represent the model and hold data in specific regions. Then the user can write Python code to fill those data inside the arrays according to the conditions provided by the metadata and function parameters. Eventually, the data filled in Python is returned back to C++ to fill the global ocean model object. This completes the configuration and the C++ code continues to run to launch SOMAR.