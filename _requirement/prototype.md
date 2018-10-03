---
title: 'Prototype'
order: 5
---
After discussion, we decide to embed Python into C++ code and call Python interpreter from C++ and launch the setup process.
This Python setup process could potentially:<br/>
1.  Communicate with each SOMAR instance to provide the correct input parameters configuration
2.  Run mpipy to communicate among all Python process in each SOMAR instance to produce the correct input parameters files, which could be upload to SOMAR later to launch the computation

Prototype 1:

SOMAR -- SOMAR -- SOMAR -- SOMAR <br/><br/>
 each insance launches <br/><br/>
setup.py--setup.py--setup.py--setup.py <br/>
||<br/>
postprocess.py<br/>
||<br/>
output region01-integration.data<br/>