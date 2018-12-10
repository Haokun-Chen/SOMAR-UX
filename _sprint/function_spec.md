---
title: 'Functional Specification'
order: 1
---
**Link to full functional Specification doc** <br/>
<a href="https://docs.google.com/document/d/17BHaBeJ_Pb-af8dnZlsvXlmJtmJX9mHQS7cUrUd8LsU/edit?usp=sharing">Full Functional Specification Doc Link<a/>

**Main project requirements:**

- The SOMAR backend is configured and launched with C++ code, the client wants to create a Python interface that allows users to configure relevant initial and boundary conditions.

**Requirement (Prioritized):**
1. Enable user to configure and supply initial conditions in Python script
2. Enable user to provide additional components to the experiment and set them in Python 
3. Flexible implementation that enables users to do customization on the configuration side (albe to use different kinds of calculation with the Python parameters provided)
4. Clean and easy-to-understand code that is reusable in the future
5. Post-processing script that filter, subset or further calculate on output data

**Requirement Details:**
- To use Python, we need to launch a Python interpreter from C++ to call Python script. 
    - This is done via Python/C API, and include the Python.H header file in C++
- To enable user to configure initial conditions, which is equivalent to assigning data into different components (velocity, pressure, etc.) of specific regions or coordinates, we need to pass relevant metadata as parameters to Python, so that users can use those parameters to define how they want to configure the initial conditions. These parameters include:
    - Dimensions, domain length
    - Physical coordinates
    - Boundaries, box sizes and number of components (represented by multi-dimensional arrays shape)
- Provide a general framework that users can follow to configure initial conditions. The frameworks should capture all the available or additional parameters mentioned above:
    - Global parameters (dimensions, domain sizes) should be only passed to Python once (from the input text file which further got processed in ParmParse in C++). This is parsed as a dictionary of key-value pairs of parameters
    - Box-specific parameters (boundaries, box sizes) are passed to Python instance call
- Provide a sample program that users can mimic and modify
- Clean structured, and easy-to-use implementation so that users can do further customization such as adding additional scalar component or update/add new Python functions