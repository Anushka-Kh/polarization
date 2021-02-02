# Polarization
The degree and angle of polarization information of reflected light can be used to infer the normal map of the surface of reflection. This process has been outlined by Atkinson and Hancock (http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.478.2140&rep=rep1&type=pdf) and has been followed in this project to produce surface normal maps for various fruit. A disambiguation routine is then applied in the algorithm to obtain the physically correct, disambiguated surface normal maps.

Polarized.py is a Python module for generating a surface normal map given polarization images from 0, 45, 90 and 135 degree filters. These images are obtained from a single image displaying the four images from the different filters in quadrants. The instrument used was the FLIR Blackfly S Machine Vision camera. In order to calculate the surface normals, intermediate processes are done such as calculating angle and degree of linear polarization images, building an object mask, calculating ambiguous surface normals at four orientations, finding the coordinates for the line of ambiguity, building masks for hemispheres separated by the line of ambiguity and finally producing a fully disambiguated surface normal map. 

## Structure Overview
The zip file called Polarization contains all the relevant information required to run the code. It has the following structure.\
-lib\
The lib folder contains the module Polarized.py. \
-bin\
The bin folder contains Execute.py which is the main program to be run which will produce the required outputs. \
-test data\
The input images that are required by Execute.py are in the test data folder.\
-requirements.txt\
This contains the version of the libraries that need to be installed.

## Dependencies
The following modules and packages need to be installed as they are used by Polarized.py.

-numpy\
-opencv-python\
-scipy\
-Pillow\
-matplotlib

The Python version used is 3.8.6.

## Configuration
In order for the bin file to import the Polarized.py module, the path that Polarized.py exists in needs to be added to the site-packages directory. This is because this is one of the directories python searches to import modules. 

1) In order to add the path to the site-packages directory, first create a .pth file which includes the address of the directory that Polarized.py exists in. A .pth file is a txt file with a .pth extension in its name.

2) Secondly, find the address of the site-packages directory. To do this, type the following commands in a python console.

```python
import sys
sys.path
```
A list of directory addresses should appear. Find the directory that ends with site-packages and move the .pth file created earlier in this directory. Now, typing sys.path should also show the contents of the .pth file in addition to the previous result. This completes the initial configuration.

## Usage
In order to run Polarization.py on a polarization image, enter the file address of the input quad polarization image when prompted. An example is shown below.


Enter File address for the input quad image : C:\\Users\\akharbanda\\.spyder-py3\\Asymmetrical Fruit\\quad3.tiff

## Output
There should be two figures produced as outputs. A continuos surface normal map and a discrete surface normal map with arrows.
 
    
