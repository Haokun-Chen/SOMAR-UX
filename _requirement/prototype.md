---
title: 'Prototype'
order: 5
---
After careful discussion, we decide to embed Python into C++ code and call Python interpreter from C++ and launch the setup process.
This Python setup process could potentially:<br/>

1.  Each SOMAR instance launch a Python interpreter and call Python function inside C++ code
2.  User further customize the Python function by writing codes to fill actual data into the multi-dimentional array

Prototype:

SOMAR instance -- SOMAR instance -- SOMAR instance<br/><br/>
    **each insance launches Python interpreter and call** <br/><br/>
pyArray.py -- pyArray.py -- pyArray.py<br/>
||<br/>
output region01-integration-01.hdf5...<br/>