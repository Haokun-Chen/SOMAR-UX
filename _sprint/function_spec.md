---
title: 'Functional Specification'
order: 1
---
**Main project requirements:**
- The SOMAR backend is configured and launched with C++ code, the client wants to create a Python interface to allow users to configure and communicate with the backend and launch SOMAR.<br/>

**Requirement Details:**
- To use Python, we need to launch a **Python interpreter** from C++ to call Python script. This is done via **Python/C API**
- To enable user to fill actual data points into the model in specific regions, we need to pass in relavant metadata as **parameters** to Python. These parameters include:
    - Metadata such as **boundaries, dimentions, model sizes** (represented by multi-dimentioanl arrays sizes) and etc. These metadata can be obtained by **ParmParse** **in SOMAR C++** code. However, since we can only obtain these parameters concatinated as a long **string** instead of key-value pairs, we pass the **entire ParmParse String** to Python and **parse the string back** to key-value pairs in Python.
    - Each specific data point in the ocean model is represented with a **"Box" object** (see Chombo <a href="http://davis.lbl.gov/Manuals/CHOMBO-RELEASE-3.1/classBox.html">reference<a/>). Each Box can possibly encapsulate data in **various regions** and **locations**, and thus has different sizes and properties. To fill the actual data of a specific **Box**,we want to know the Box length, Box size, Box's **physical position(coordinates)** in the model, **levels** of the box, as well as other properties.
    - After passing the parameters into Python, users then write Python code instead of C++ to fill the actual data.
    - The data is returned back to C++ side and converted into corresponding C++ types and variables to get ready for launching the experiment

**Additional project requirements:**
- Write a post processing script that allow users to filter, subset, integrate, or do other addtional operations on the output data.

Ohter functional requirements:
- Get mpipy/somar working with 1 MPI version.
- Make a Boxlib-style data holder variant for mpipy that can be transferred among python / SOMAR. 
    - (See: LevelData class in Chombo documentation) 

Stretch Goals: 
- Expand the python API to make domain decomposition simple. 
- Make the data holder work like a numpy array so that we can easily fill it with data. 
    - (Example: u = sin(x) where both x and u are the decomposed data holders.) 