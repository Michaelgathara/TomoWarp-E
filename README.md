# SOFTX-D-17-00061
TomoWarp2: a local Digital Volume Correlation code. To cite this software publication: http://www.sciencedirect.com/science/article/pii/S2352711017300511

TomoWarp2 is a Python based code that allows full-field vector displacements to be measured between 2D or 3D image sets, based on a local approach of Digital Image Correlation. These displacements can be used to calculate the complete 2D or 3D strain tensor field to study, for example, heterogeneous deformation responses of materials during loading. The code is provided with a GUI, and can handle different input and output formats. Moreover, new features can be implemented with the flexible code architecture.

Send an email to erika.tudisco@construction.lth.se to report issues and bugs or if you want to receive updates.


WSL Install:
```tex
You can install this in WSL, I recommend a fresh distro of Ubuntu 20.04LTS which is available in the Microsoft Store. 

You can set this Ubuntu 20.04LTS to be for this program and have your own personal distro such as Ubuntu 22.xxLTS for other personal use
```

Install:

```tex
1. sudo apt install python2.7
2. sudo apt install python3-virtualenv
3. virtualenv tw2 -p python2.7
4. source tw2/bin/activate
5. pip install numpy scipy matplotlib pillow
5x sudo apt install python-imaging-tk
6. sudo apt install swig
7. Compile the c-code
    (a) Set path to the c_code folder
        cd pixel_search/c_code
    (b) Run command
        python setup.py build ext --inplace
If you get an error of missing Python.h you might need to install python-dev:
    sudo apt install python-dev
If you get the error ”unable to execute ’x86 64-linux-gnu-gcc’: No such file or directory” or similar you
need to install gcc:
    sudo apt install gcc
8. Compile the tifffile module:
    (a) Set path to the tools folder
        cd tools
    (b) Run command
        python setup tifffile c.py build ext --inplace
```