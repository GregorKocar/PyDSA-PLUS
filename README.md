Spectrum Analyzer for the Rigol DS1000 series digital scopes  V1.1  
  
RF Spectrum Analyzer in Python. This is a modified version of PA2OHH's audio spectrum analyzer:  
http://www.qsl.net/pa2ohh/11sa.htm  
  
It is a fork project of Rich Heslip VE3MKC, https://github.com/rheslip/PyDSA
  
It uses National Instruments VISA driver to download samples from the scope, perform FFTs and show the results. I used the PyVISA 1.5 wrapper:  
http://pyvisa.readthedocs.org/en/latest/getting_nivisa.html  

It was adapted to work with Python 3.x

Dependencies:    
PyVISA  1.5
math  
numpy  
Tkinter  

Changelog:  
20. 9. 2015 - first release  
10. 5. 2019 - modifications by Gregor Kocar S53SL


Notes: 
Modifications by Gregor Kocar S53SL
 modified to work with Python3.0 and VISA1.5  
 This version has a modified Sweep()  
 adapted to be packaged as exe  
 added dynamic markers + peak value  
 added zoom function  
 added screenshot button  
 added navigation  
 resizable window    



Kerr Smith provided these step by step installation instructions:
(modifired by Gregor Kočar)

I first installed the latest National Instruments VISA runtime:

http://www.ni.com/download/ni-visa-run-time-engine-15.0/5379/en/NIVISA1500runtime.exe

Next I installed Python 3.x making sure Python was added to the path (this is so you can run python from the command line from any directory):

https://www.python.org/downloads/

Check if pip is installed:
pip -V
if not follow this instructions:
https://phoenixnap.com/kb/install-pip-windows


Next I updated pip and setuptools as well as installing wheel as recommend on:
http://python-packaging-user-guide.readthedocs.org/en/latest/installing/#install-pip-setuptools-and-wheel
pip3 install setuptools
pip3 install wheel
pip3 install mock

Next I installed pyvisa version 1.5 as recommend (the mock update above made this work):

pip3 install pyvisa==1.5


pip3 install numpy
pip install Pillow

Next I downloaded the PyDSA code from Github:

https://github.com/GregorKocar/PyDSA-PLUS

The file to run is in the PyDSA-PLUS directory and is called PyDSA.pyw

