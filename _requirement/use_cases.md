---
title: 'Use Cases'
order: 6
---

For Common oceanographer and environmental fluid mechanic practitioners

1. To add a scalar component for the experiment
    - Change the number of scalar to a desired number
    - Add the new scalar component name in enum type 
    - Configure the scalar component data in Python script by selecting the corresponding sub-array of certain component and assign data to it
2. To change the dimension of the experiment
    - Open the input.basicTest3D.research1
    - Change DIM = 2 to 3 or vice versa
3. To set up x-velocity of a certain region
    - Select all coordinates and their x-velocity subarrays
    - Assign values to the x-velocity subarray
    - To set up tracers for further graphing need
4. Add the x/y/z-tracer scaler component for the experiment
    - Select all coordinates and assign initial physical position to their x/y/z-traver subarrays
5. Change the Python file name or function name
    - Update file or function name
    - Update the imported Python module name and function name in C++
